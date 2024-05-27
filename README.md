![Designer (3)](https://github.com/martaldsantos/AIAppsOpenHack/assets/44229401/d197b4df-986c-4952-bf44-699f2315ab3f)

# Open Hack: Innovating Apps with Azure AI Studio

This OpenHack is an integration between Azure and OpenAI's large language models. It leverages Azure AI Search for data retrieval and ChatGPT-style Q&A interactions. Using the Retrieval Augmented Generation (RAG)
design pattern with Azure Open AI's GPT models, it provides a natural language interaction to discover relevant responses to user queries. Azure AI Search simplifies data ingestion, transformation, indexing, and multilingual translation. The OpenHack includes sample data so it's ready to try end to end.

## About the Hack

The Innovating Apps with Azure OpenAI OpenHack will take you on a series of challenges to develop an end-to-end solution using Microsoft’s Generative AI offering. 
The OpenHack consists of a series of challenges, in which your team must use the guidance and resources provided to implement intelligent search solutions on Azure. These challenges will increase in complexity as you progress through the OpenHack, staring from the creation of a project in Azure AI Studio to the deployment of our desired solution into a web app.
The goal of this OpenHack is to provide you the ability to work as a team, learn from each other, with greater knowledge retention as each team will have to “figure out” how to reach the success criteria. The coaches provide technical guidance, but not answers to the 
squads. 
In the beginning of each challenge one of the coaches will be providing lectures, demos to setup challenges and review the previous challenge’s solutions.

Get to know more about the OpenHack format on [What The Hack](https://github.com/microsoft/WhatTheHack)

## Challenges

- **Challenge 1: Creation of the Project in Azure AI Studio**
- **Challenge 2: Deploy and test a chat model without your data**
- **Challenge 3: Add your Data to your project**
- **Challenge 4: Orchestrate and customize the set up with Prompt Flow**
- **Challenge 5: Evaluate the chat performance**
- **Challenge 6: Deploy your WebApp**
- **Challenge 7: LLMOps in Visual Studio Code**


## Development Environment

[![Open in GitHub Codespaces](https://img.shields.io/static/v1?style=for-the-badge&label=GitHub+Codespaces&message=Open&color=brightgreen&logo=github)](https://github.com/codespaces/new?hide_repo_select=true&machine=basicLinux32gb&repo=790752905&ref=main&devcontainer_path=.devcontainer%2Fdevcontainer.json&geo=EuropeWest&machine=standardLinux32gb)
[![Open in Dev Containers](https://img.shields.io/static/v1?style=for-the-badge&label=Dev%20Containers&message=Open&color=blue&logo=visualstudiocode)](https://vscode.dev/redirect?url=vscode://ms-vscode-remote.remote-containers/cloneInVolume?url=https://github.com/martaldsantos/AIAppsOpenHack)

The repository is instrumented with a [DevContainer](./.devcontainer/devcontainer.json),  configuration that can provide you with a _pre-built_ environment that can be launched locally, or in the cloud [GitHub Codespaces](https://docs.github.com/en/codespaces/overview). You can also elect to do a _manual_ environment setup locally, if desired. Here are the three options in increasing order of complexity and effort on your part. **Pick one!**

 1. **Pre-built environment, in cloud** with GitHub Codespaces
 1. **Pre-built environment, on device** with Docker Desktop
 1. **Manual setup environment, on device** with Anaconda or venv

The first approach is _recommended_ for minimal user effort in startup and maintenance. The third approach will require you to manually update or maintain your local environment, to reflect any future updates to the repo.

To setup the development environment you can leverage either GitHub Codespaces, a local Python environment (using Anaconda or venv), or a VS Code Dev Container environment (using Docker).

###  Pre-Built Environment, in cloud (GitHub Codespaces)

**This is the recommended option.**
 - Fork the repo into your personal profile.
 - In your fork, click the green `Code` button on the repository
 - Select the `Codespaces` tab and click `Create codespace...` 
 
This should open a new browser tab with a Codespaces container setup process running. On completion, this will launch a Visual Studio Code editor in the browser, with all relevant dependencies already installed in the running development container beneath. **Congratulations! Your cloud dev environment is ready!**

### Manual Setup Environment, on device (Anaconda or venv)

1. Clone the repo

    ```bash
    git clone https://github.com/martaldsantos/AIAppsOpenHack
    ```

1. Open the repo in VS Code

    ```bash
    cd AIAppsOpenHack
    code .
    ```

1. Install the [Prompt Flow Extension](https://marketplace.visualstudio.com/items?itemName=prompt-flow.prompt-flow) in VS Code
      - Open the VS Code Extensions tab
      - Search for "Prompt Flow"
      - Install the extension

1. Install the [Azure CLI](https://learn.microsoft.com/cli/azure/install-azure-cli) for your device OS

1. Create a new local Python environment using **either** [anaconda](https://www.anaconda.com/products/individual) **or** [venv](https://docs.python.org/3/library/venv.html) for a managed environment.

    1. **Option 1**: Using anaconda

        ```bash
        conda create -n my-sample python=3.11
        conda activate my-sample
        pip install -r requirements.txt
        ```

    1. **Option 2:** Using venv

        ```bash
        python3 -m venv .venv
        source .venv/bin/activate
        pip install -r requirements.txt
        ```
