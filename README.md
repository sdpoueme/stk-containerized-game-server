# Welcome to the containerized Super Tux Kart CDK sample

This is a CDK TypeScript project that packages [Super Tux Kart](https://github.com/supertuxkart) into a container. Containers are a great fit for game server’s workload because they’re lightweight, start quickly, and optimize the utilization of the underlying instance. The Super Tux Kart container can be deployed on kubernetes to run game sessions. In this sample, we  use Docker multi-stage builds to package our SuperTuxKart binaries and assets.

 

To get started with this project. 

* Clone the repo
* Install CDK `npm install aws-cdk-lib`
* Bootstrap cdk `cdk bootstrap`
* Run `npm install`
* Run `cdk deploy --parameters notificationEmail=xxx@yyy.com --parameters notifyPhone=+9999999999 —parameters gitRepoName=myDemo`

The stack deploys the following resources:

* Git repository to store the Super Tux Kart Dockerfile
* ECR registry to store the Super Tux Kart game server image
* CodeBuild project to build Super Tux Kart images on ARM
* SNS Notifications to update end users on the status of the build
* CodePipeline to perform the build stages and release to production
