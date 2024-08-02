# Project Name

This project automates the deployment of a Django application using CircleCI and Docker, with the final Docker image being pushed to AWS ECR.

## Prerequisites

- **CircleCI account**: Ensure you have an active CircleCI account connected to your GitHub repository.
- **AWS Account**: Ensure you have an AWS account with access to ECR.
- **Environment Variables**: Configure the following environment variables in your CircleCI project settings:
  - `AWS_ECR_REGISTRY_ID`: Your AWS ECR registry ID.
  - `AWS_DEFAULT_REGION`: The AWS region where your ECR registry is located.

## Workflow Steps
- Build: Performs the following steps:
- Checkout: Checks out the latest code from the main branch.
- Install Dependencies: Installs Python dependencies from requirements.txt.
- Build Docker Image: Performs the following steps:
- Checkout: Checks out the latest code from the main branch.
- Setup Remote Docker: Enables Docker layer caching for faster builds.
- Install AWS CLI: Installs the AWS CLI on the CircleCI runner.
- Build and Push Docker Image to AWS ECR: Builds the Docker image and pushes it to AWS ECR with a unique tag based on the build number.


## How to Use
- Fork the repository: Fork this GitHub repository to your own account.
- Configure CircleCI: Link your GitHub repository to CircleCI.
- Set environment variables: Add the required environment variables (AWS_ECR_REGISTRY_ID and AWS_DEFAULT_REGION) in CircleCI project settings.
- Commit changes: Push your changes to the main branch to trigger the pipeline.
