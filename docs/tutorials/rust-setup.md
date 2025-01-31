# Setting up a dev container for Rust

Primary author: [Aastha Sharma](https://github.com/aasthasharm)
## Prerequisites:
To be able to set up a dev container, we must first ensure we have the following installed:

* Docker (for running containers)

* Visual Studio Code (for an IDE)

* The Dev Containers Extension (to create a container)

!!! info

    If you do not already have these installed, please visit the following pages for more information:

    [Docker Installation](https://docs.docker.com/engine/install/)
    
    [Visual Studio Code Installation](https://code.visualstudio.com/download)
    
    [Dev Containers Extension Installation](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

## Initializing Git
First, we must create a directory and git repository to house our new project. You can either open Visual Studio Code and create a directory there, or open the terminal and execute the following commands:

```
mkdir rust-dev-container 
cd rust-dev-container
git init
```

