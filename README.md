# OpenHackAIApps

This repository contains the content for the Microsoft AI OpenHack. 

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
