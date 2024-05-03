# Open Hack - Challenge 6: Deploy your WebApp

This challenge is about deploying your WebApp to Azure based on the prompt flow previously created. You will learn how to containerized and deploy your WebApp to any Azure Service that supports a containerized application, like Azure App Services, Container Apps, Kubernetes, or other.

We will not deploy the webapp application using a devops pipeline, since the focus of this challenge is to create the webapp and not about all the CI/CD process. You can use Microsoft documentation with all the steps to create a pipeline to deploy your application, using Azure Devops or even Github.

## Prerequisites

1. Docker Desktop installed on your machine.
2. Azure CLI installed on your machine.
3. Azure Subscription.
4. Visual Studio Code installed on your machine.
5. PromptFlow extension installed on your Visual Studio Code.
6. Conda installed on your machine.
7. Python 3.9 installed on your machine.
8. promptflow, azure.ai.ml and promptflow-tools installed on your machine.

## Instructions

1. On your visual studio code, create a new folder called `dist` inside the `src` folder.
2. Download the promptflow code from AI Studio and extract it to the `src` folder.
    2.1. Unzip the `YourFlow.zip` file
    ```bash	
    tar -xf YourFlow.zip -C src
    ```

3. Open the `src` folder in Visual Studio Code.
    ```bash	
    code src
    ```
    3.1. Create a new conda environment with the following command:
    ```bash
    conda create --name pf python=3.9
    ```
    3.2. Activate the conda environment with the following command:
    ```bash
    conda activate pf
    ```
    3.3. Install the required packages with the following command:
    ```bash
    pip install promptflow promptflow-tools azure.ai.ml
    ```


4. Go to the `Prompt Flow Extension` and click on `Connections`.

</br>

5. Set the connection provider to `Azure AI Connection for local connections` and create an AzureML connection string.
</br>

6. Save the connection and refresh the page.
</br>

7. Open the flow and set the connection to `Default_AzureOpenAI` and the deployment name to `gpt-35-turbo`.
</br>

8. Save the flow.
</br>

9. Go to the `Flows` folder and click on `src`.
</br>

10. Click on `Build` and then click on `Build as docker`.
</br>

11. Select the `dist` folder and click on `Create Dockerfile`.

**Note**: if this step fails do it with pf cli (vscode somehow doesn't show errors, but the cli does)
```bash
    pf flow build --source src --output dist --format docker
```
12. Open the `dist` folder in Visual Studio Code.
</br>

13. Edit the `flow/requirements.txt` file and add the following lines:
</br>
    ```
    promptflow
    promptflow-tools
    ```
</br>

14. Save the file.
</br>
15. Update the `Dockerfile` to use the old version of the promptflow code.
</br>
    15.1. Add the following lines to the `Dockerfile`:

    ```
    RUN wget -O /opt/conda/envs/promptflow-serve/lib/python3.9/site-packages/promptflow/_sdk/_serving/static/index.js https://raw.githubusercontent.com/microsoft/promptflow/ffa78b411ccedd42e95bb412d2d2e83afa6addc0/src/promptflow/promptflow/_sdk/_serving/static/index.js && wget -O /opt/conda/envs/promptflow-serve/lib/python3.9/site-packages/promptflow/_sdk/_serving/static/index.html https://raw.githubusercontent.com/microsoft/promptflow/ffa78b411ccedd42e95bb412d2d2e83afa6addc0/src/promptflow/promptflow/_sdk/_serving/static/index.html
    ```
</br>

16. Run the following command to build the docker image, using docker desktop (on dist directory):
    ```
    docker build -t Yourflow .
    ```
</br>

17. Go to Azure Portal and under your Azure AI resource, hit the Show Keys and then copy the Key 1 value, since we will use it as environment variable to deploy the container.
</br>

18. Run the following command to run the docker image:
    ```
    docker run -e DEFAULT_AZUREOPENAI_API_KEY=<key1> -p 8080:8080 Yourflow
    ```
**Note:** If you need more environment variables, you can add them using the `-e` flag (like for instance the CosmosDB key, or the SearchAI key).

e.g.:
```bash
docker run -e AOAI-CONNECTION_API_KEY=yourkey1 -e CONTOSO-COSMOS_KEY=yourkey2 -e CONTOSO-SEARCH_API_KEY=yourkey3 -p 8080:8080 yourImageName
``` 
</br>

19. Test the containerized application by running on browser:
    ``` 
    http://localhost:8080
    ```
</br>

20. Deploy the containerized application to service of your choice like Azure App Services, Container Apps, Kubernetes, or other.


## Success Criteria

You will know you are successful when you have deployed your WebApp to Azure and you can access it locally through the browser.

## Resources

- [Azure CLI](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli)
- [Docker Desktop](https://www.docker.com/products/docker-desktop)
- [Visual Studio Code](https://code.visualstudio.com/)
- [PromptFlow Extension](https://marketplace.visualstudio.com/items?itemName=Microsoft.promptflow)
- [Azure AI](https://azure.microsoft.com/en-us/services/machine-learning/)
- [Azure AI Search](https://azure.microsoft.com/en-us/services/search/)
- [Azure App Services](https://azure.microsoft.com/en-us/services/app-service/)
- [Azure Container Apps](https://azure.microsoft.com/en-us/services/container-app/)
- [Azure Kubernetes Service](https://azure.microsoft.com/en-us/services/kubernetes-service/)
- [Azure DevOps](https://azure.microsoft.com/en-us/services/devops/)
- [GitHub Actions](
https://docs.github.com/en/actions)
- [Microsoft Documentation](https://docs.microsoft.com/en-us/)
- [PromptFlow](https://github.com/microsoft/promptflow)
