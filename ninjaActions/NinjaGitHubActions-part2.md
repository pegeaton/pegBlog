# Part2: Dive Deeper into GitHub Actions -- Work in Progress

Let's take a hands-on approach and walk-through creating the hello world program and GitHub Actions workflow together.  The GitHub documentation (https://docs.github.com/) is available as a reference as needed throughout the exercise.

In this excercise you will create a GitHub repository containing three files: README.md, hello.go, and hello-action.yml.  The files are structured as shown in the following diagram:

<img src="../images/modernapps-top-level.png" height="350" width="600" alt="hello-action">

## 1. Create a simple test program written in go

1. Create a GitHub account (https://github.com) (if you have not done so already.)

2. Create a *samples* repository 

2. Create a *README.md* file (we will use this later) for the repository.

3. Create a file called *hello.go* within your samples repository containing the following code:

   		package main
			import (
				"fmt"
			)

			func main() {
				fmt.Println("Hello, world.")
			}

This code will be run by the workflow on a push operation.

## create a simple GitHub Action
1. Create a workflow directory within your repository called *.github/workflows*

1. Create a file called *hello-action.yml* within the workflows diretory (.github/workflows/hello-action.yml)

1. show screen shot 



## Examples: Modern Apps Ninja GitHub Actions
* Workflow Runner
* Handling Secrets
* Versioning
* Troubleshooting GitHub Actions
* Testing GitHub Actions
* Testing considerations


## Automated Assignment Evaluation
1. Contributor completes assignment file
2. Contributor submits a pull request for assignment file to the Modern Apps Ninja course repository
3. GitHub Action verify-assignment is triggered to run
3.1 If assignment results are correct the pull request is closed
3.2 If the assignment results are incorrect the error is posted to the pull request for modification.

3-4 graphics


