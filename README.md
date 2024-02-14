# CI/CD Pipeline Documentation

## Overview
I create CICD pipeline in AWS environment with blue/green deployment stratey using cloudformation. The whole infrastructure created in AWS Cloudformation.

## Pipeline Diagram
![CI/CD Pipeline Diagram](https://github.com/ehtishamasghar13/AWS-cloudformation-vikunja/blob/main/cicd.png)

## Stages of the Pipeline
The CI/CD pipeline consists of several key stages, each facilitated by AWS services:

1. **AWS CodeCommit (Source)**
   - I use as SCM with two repositories for frontend and backend.

2. **AWS CodeBuild (Build)**
   - I create CodeBuild stage to get code from Codecommit and build it. 

3. **AWS CodeDeploy (Deploy)**
   - The build artifact get from CodeBuild is deployed to AWS ECS using AWS CodeDeploy.

4. **AWS ECS**
   -  The AWS ECS Cluster with Fargate launch type is created using AWS CloudFormation.

## Infrastructure Management
- The entire infrastructure, including VPC, subnets, security groups, and AWS service resources, is defined and provisioned using AWS CloudFormation.

## Security and Best Practices
- IAM roles and policies are carefully crafted to provide necessary permissions to each service.
- Security groups are configured to enforce the principle of least privilege.

---

