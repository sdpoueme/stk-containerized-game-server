# Welcome to the containerized Super Tux Kart CDK sample

This is a CDK TypeScript project to deploy a CI/CD pipeline for [Super Tux Kart](https://github.com/supertuxkart) containerized game servers. 

To get started with this project. 

* Clone the repo
* Run `cdk deploy --parameters notificationEmail=xxx@yyy.com --parameters notifyPhone=+9999999999 —parameters gitRepoName=myDemo`

The stack deploys the following resources:

* Git repository to store the Super Tux Kart Dockerfile
* ECR registry to store the Super Tux Kart game server image
* CodeBuild project to build Super Tux Kart images on ARM
* SNS Notifications to update end users on the status of the build
* CodePipeline to perform the build stages and release to production
