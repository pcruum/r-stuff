# How to use devcontainers

For a detailed description of the devcontainer, please visit the [documentation](https://code.visualstudio.com/docs/devcontainers/containers).

## Prerequisites

- [Docker](https://www.docker.com/)
- [Remote - Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

## Getting Started

1. Clone this repository
2. Open the repository in Visual Studio Code
3. Click on the green button in the bottom left corner of the window
4. Select "Reopen in Container"

## Version Control

It might happen on Windows computers, that the ssh key is not available within the container. To fix this, open powershell as administrator and run the following commands:

```powershell
Set-Service -StartupType Automatic
Start-Service ssh-agent
Get-Service ssh-agent
ssh-add $HOME/.ssh/id_rsa
```

For more information visit the [documentation](https://code.visualstudio.com/remote/advancedcontainers/sharing-git-credentials).
