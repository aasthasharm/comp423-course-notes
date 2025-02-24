# Setting up a dev container for Go

## Prerequistes 
Primary author: [Aditi](https://github.com/aditivn12)

Before we start, make sure you have the following:
- 
- A GitHub account: If you don't have an account, make sure to create one.
- Git installed: Make sure to install[Git](https://github.com/).
- Visual Studio Code (VS Code): [Download](https://code.visualstudio.com/download) it if you haven't already.
- Docker installed: This is a required to run a dev container. Download it [here](https://www.docker.com/products/docker-desktop/).
- Command-line basics: You should know the basics!

### Step 1: Initialize a New Project

1. Make a new directory:
```bash
    mkdir comp-423-Go-Tutorial
    cd comp423-Go-Tutorial
```

2. Open a terminal in an empty directory.
3. Initialize a Git repository:
```bash
   git init
   echo "# Go Dev Container Project" > README.md
   git add README.md
   git commit -m "Initial commit with README" 
```
### Step 2: Set up a remote repository
Part 1:

1. Create a New Repository page in GitHub.

2. Fill in this:

    - Repository Name: comp423-Go-Tuturial
    - Description: "Setting up Go."
    - Visibility: Public

3. Do not initialize README, .gitignore, or license.

4. Create Repository.

Part 2: 
Link your Local Repository to GitHub

1. Make sure you add the GitHub repository as a remote by doing this:


```bash
git remote add origin https://github.com/your-username/comp423-Go-Tutorial.git
```
Replace your-username with your GitHub username.

2. Make sure the default branch is named main. 

3. Push any of the local commits to the GitHub repository by using this:
``` bash
git push --set-upstream origin main
```

### **Step 3: Set Up the Dev Container**
What is a dev container? 
A dev container is a prefined workspace. It uses docker to make reproducable and isolated work environemnts. 

- Create a .devcontainer folder:
``` bash
    mkdir -p .devcontainer
```

- Create a devcontainer.json file and add configurations:
``` json
{
    "name": "Go Dev Container",
    "image": "mcr.microsoft.com/devcontainers/go:1.20",
    "customizations": {
        "vscode": {
            "extensions": ["golang.go"]
        }
    }
}
```
1. name: A name for the dev container.
2. image: The docker image for Go.
3. customizations.vscode.extensions: This is the custimatizations for VS Code in the Go language..

### Step 4: "Hello COMP423" Program
- Now that you are inside the container, make sure to create a new Go file:
!!!note
    A good idea would be to name it hello.go

- Add the code:
``` go
    package main

    import "fmt"

    func main() {
        fmt.Println("Hello COMP423")
    }
```
- Run the program:
``` bash 
    go run .
```
### **Step 5: Commit changes**
``` bash
git add .
git commit -m "Tutorial for Go setup"
git push -u origin
```