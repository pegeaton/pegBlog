# Part 2: Dive Deeper into GitHub Actions

Let's take a hands-on approach and walk-through creating the hello world program and GitHub Actions workflow together.  
The GitHub documentation (https://docs.github.com/) is available as a reference as needed.

In this exercise you will create a GitHub repository containing three files: README.md, hello.go, and hello-action.yml.  The file structure is shown in the following diagram:

<img src="../images/part2-samples.png" alt="directory structure" title="Samples Repository Structure">


## 1. Create a GitHub Account
Create a GitHub account, if you have not done so already.  

In our example, the account is **pegeaton**

## 2. Create a repository 
Create a **samples** repository within your GitHub account.  The repository is used to store your files.

## 3. Create a README.md within the repository 
Create a *README.md* file (we will use this later) in the repository containing the following:

		# Samples Repository
		This repository contains examples:
		* hello.go code example
		* hello-action.yml example

## 4. Create a simple test program written in go
Create a file called *hello.go* within your samples repository containing the following code:

   		package main
			import (
				"fmt"
			)

			func main() {
				fmt.Println("Hello, world.")
			}

This code will be run by the GitHub Action workflow on a push operation.

## 5. create directory to contain the GitHub Actions
Create a workflow directory within your repository called *.github/workflows*

## 6. create a simple GitHub Actions workflow
Create a file called *hello-action.yml* within the workflows directory (.github/workflows/hello-action.yml)
containing the following code:

	name: hello-sample
	on: [push]
	  jobs:
  	    echo-hello:
    	      runs-on: ubuntu-latest
    		steps:
      		- uses: actions/checkout@v2
      		- uses: actions/setup-node@v1
      		- run: echo "Hello code"
      		- run: go run hello.go    

Your workflows directory may look like the following after creating the file:

<img src="../images/workflow-dir.png" alt="workflow dir">

Remember this action runs on *any* push within the repository therefore the commit of the file triggered the workflow! Let's take a look at the run in the next section and be sure to **disable the workflow** since this is only a demonstration and you don't really want it to run with every push. 

## 7. Reviewing GitHub Actions Activity

Select the Actions tab in the samples repository.

<img src="../images/actions-tab.png" alt="actions tab">

Then select the *hello-action.yml* link to display the results of running the action.

The job name is *echo-hello*

<img src="../images/echo-hello-job.png" alt="echo hello job">

Notice the *on: [push]* indicates the action will be run on a push event within the repository. The commit of the hello-action.yml is a push event that triggered the action.  

The runner is an application that executes the jobs as defined in the GitHub Actions workflow. In this case, the runner is hosted (by GitHub) and the runner runs-on an ubuntu environment. (See the GitHub documentation for self-hosted runner.) 

The following image shows the execution of the steps in the workflow. Troubleshooting is facilitated by walking through the steps as execution occurs.
<img src="../images/bash-go-run.png" alt="bash go run">

A badge can be created and used to watch the status of workflow runs.  For our example, let's add the badge to the samples/README.md page indicating the status of the excution of the workflow. 

**1. Generate a badge and copy the graphic.**
<img src="../images/status-badge-create.png" alt="status-badge-create">

**2. Copy the graphic link**

<img src="../images/copy-status-badge.png" alt="copy-status-badge">

**3. Paste the graphic link into the README.md file**
Note:  the change to the README.md file will kickoff the workflow and update the status badge on the README.md page.
<img src="../images/readme-edit.png" alt="edit readme">

**4. Resulting README.md page with the status badge**

<img src="../images/readme-result.png" alt="readme with status badge">

### Disable the workflow.
Disable the workflow as shown in the following graphic to avoid running it on every push event:
<img src="../images/disable-workflow.png" alt="disable workflow">

## Summary

Part 2 is focused on hands-on experience; creating GitHub Actions, understanding the structure and elements of workflows, and workflow execution.  In Part 3 of the series we explore more complex examples of GitHub Actions used in the Modern Apps Ninja Repository. 

### Topics to Explore:

* Handling Secrets: documentation on encrypted secrets (https://docs.github.com/en/actions/reference/encrypted-secrets)
* Versioning: Use tags on actions are the recommend way for versioning actions.  See the documentation *Using release management for actions* (https://docs.github.com/en/actions/creating-actions/about-actions#using-release-management-for-actions)
* Troubleshooting: enhance troubleshooting GitHub Actions by enabling debug logging (https://docs.github.com/en/actions/managing-workflow-runs/enabling-debug-logging)
* GitHub Guides: learning path for a variety of tasks. (https://docs.github.com/en/actions/guides)

### Additional Exercise
Here is a small problem for you to consider and to provide some practice with GitHub Actions.

*Scenario - assignment grading*
	Members taking a course will work on an assignment based upon a file stored in the Modern Apps Ninja repository. 
	When the assignment is completed it needs to be graded automatically and the results provided back to the member and to the Ninja administrators. 

	How would you tackle this automation? Remember, a key principle is to encourage following GitOps principles.

	Create a solution within your own repository.  
	Submit a link to your solution as a feedback issue on the samples project.

There are many different solutions with varying degrees of complexity.  Give the exercise a try and discover even more interesting features of GitHub Actions!


