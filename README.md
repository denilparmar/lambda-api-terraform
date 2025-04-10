# AWS Lambda Deployment with Terraform and GitHub Actions

This project demonstrates how to automate the deployment and management of **AWS resources** using **Terraform** and **GitHub Actions**. The infrastructure includes **AWS Lambda**, **API Gateway**, and **IAM roles**. The goal of this project is to showcase my learning of **Infrastructure as Code (IaC)** and **CI/CD** practices with real-world cloud services.

## **Overview**

This project uses **Terraform** to define and provision AWS resources, including an **AWS Lambda function**, **API Gateway**, and the necessary **IAM roles**. The entire deployment process is automated with **GitHub Actions**, enabling Continuous Integration (CI) and Continuous Deployment (CD).

### **Key Technologies Used**
- **Terraform**: Infrastructure as Code (IaC) tool for provisioning and managing AWS resources.
- **AWS Lambda**: Serverless compute service for running code without provisioning or managing servers.
- **AWS API Gateway**: Fully managed service for creating and publishing REST APIs that route HTTP requests to AWS Lambda functions.
- **GitHub Actions**: Automation tool for setting up CI/CD pipelines to deploy infrastructure and manage deployments.

---

## **How It Works**

### **Terraform Configuration**

In this project, Terraform is used to define, provision, and manage the following AWS resources:

- **IAM Role**: A role that grants AWS Lambda the necessary permissions to execute.
- **Lambda Function**: A simple Node.js Lambda function deployed from a `.zip` file.
- **API Gateway**: Exposes the Lambda function as an HTTP endpoint.
- **Lambda Permissions**: Allows API Gateway to invoke the Lambda function.

### **Deployment Pipeline with GitHub Actions**

The deployment process is fully automated using **GitHub Actions**. Upon pushing changes to the `master` branch, the following steps are executed:

1. **Checkout Code**: The repository code is pulled from GitHub.
2. **Zip Lambda Code**: The Lambda function code is zipped into a `.zip` file.
3. **Terraform Init**: Initializes the Terraform working directory.
4. **Terraform Plan**: Prepares a deployment plan to apply any changes.
5. **Terraform Apply**: Applies the plan to create or update the AWS resources.

