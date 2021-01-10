# Part 1: GitHub Actions and the Modern Apps Ninja Repository
In this blog, we explore GitHub Actions and GitHub Actions in the Modern Apps Ninja community repository:
* Modern Apps Ninja Community and Repository
* GitHub Actions
* GitHub Actions Marketplace: An Ecosytem of GitHub Actions

## Modern Apps Ninja Community and Repository
The [Modern Apps Ninja](https:https://modernapps.ninja/) learning community consists of students and professional cloud native practitioners, learning and working together to apply new cloud native technologies skills. A collaborative, community-driven approach to developing and curating content is fundamental to the program mission.  Community members develop the key content, including: courses, labs and hackathons focused on modern applications and application platforms.  Experiential learning opportunities are provided through [GitOps](https://www.youtube.com/watch?v=r50tRQjisxw) methodologies embedded throughout courses and on-going administration of the program.

### GitHub 
[GitHub](https://github.com) is more than a source code control system, it is truly a collaboration platform. GitHub is well documented and there are many different tutorials to help you get started.  One of my favorites is the [GitHub Learning Lab](https://lab.github.com/). Check it out and join the [Modern Apps Ninja](https:https://modernapps.ninja/) community!

### Modern Apps Ninja GitHub repository
The content, membership, and overall [Modern Apps Ninja](https:https://modernapps.ninja/) program is supported through GitHub.  The [Modern Apps Ninja GitHub repository](https://github.com/ModernAppsNinja/modernappsninja.github.io) is a public repository available for anyone to view; the repository contains lab guides, course content, and admnistrative materials.

![Modern Apps Ninja Repository](../images/modernapps-top-level.png)

In addition, the [modernapps.ninja](https://lms.modernapps.ninja/) learning management system (edX platform) is also used for delivering free courses.

### The need for automated workflows
Automation is necessary to ensure consistent operations and rapid delivery of software supporting the program. Workflows are used to improve quality and efficiency when delivering code to production. For example, the site https://modernapps.ninja/ is fully automated and automatically generated from GitHub. The automation helps with standarization efforts and testing. While there are many CI/CD supporting technologies (Tekton pipelines, Jenkins, etc.) the use of GitHub Actions has a number of benefits, even at the most basic, free subscription level, including: 
* 2,000 Actions minutes/month are free for public repositories
* 500MB of GitHub Packages storage free for public repositories
* fully integrated into GitHub
* GitHub Actions workflow run on GitHub hosted virtual machines or self-hosted machines

## GitHub Actions
[GitHub Actions](https://docs.github.com/en/free-pro-team@latest/actions) are powerful workflow tools built right into GitHub. GitHub Actions workflows are used to automate tasks within the repository and execution is triggered by events. GitHub Actions support many different types of event which trigger workflows, including push, pull_request, issues, etc. 

To use GitHub Actions, create a .github/workflows directory in your repository and create a YAML file containing GitHub Actions workflow descriptions using YAML syntax.

Let's take a look at the anatomy of a simple GitHub Action.

![hello-action.yml](hello-action.png)

This GitHub Actions workflow runs a bash command to echo the classic "Hello World!" statement and then runs a go program to display "Hello World!".

 
The file contains:
* the name of the GitHub Action
* the event type (in this case, a push event)
* jobs -- these are the items that will be queued for execution 
* each job is given a name

### Simple GitHub Actions

flowchart -- show diagram

spin up ubuntu system
check out repository
load file??

load any packages needed (npm ... xxx)
run code




### Event triggers
There are lots of defined event types to trigger the execution of the actions and the documenta 


* GitHub Actions
* GitHub Actions in the Modern Apps Ninja repository
* Benefits for contributors and administrators

Graphics — ninja program
existing actions — graphics

flowchart showing action need/sequence


## GitHub Marketplace: An Ecosytem of GitHub Actions
The GitHub Marketplace provides a venue for creators to share GitHub Actions with the GitHub community, 

* Advantages and Disadvantages of using ecosystem workflows
* GitHub Actions used in the Ninja repository
* Recommendations for repository administrators
marketplace graphic — show secrets

The following list provides and example of GitHub Actions for secrets:
* Vault Secrets by hashicorp
* Secrets Sync Action by google
* Azure key vault - Get Secrets by Azure
* Get Secret Manager secrets by google-github-actions
* Nightfall DLP Action by nightfallai

