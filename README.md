**PROJECT: CI/CD PIPELINE FOR VERA AIDOO - PORTFOLIO WEBSITE**

I developed a CI/CD pipeline for my portfolio website using GitHub Actions and integrated it with Amazon S3 for automated deployment. 
This workflow streamlined the process of syncing website updates to the hosting environment directly from my GitHub repository.

**KEY FEATURES AND WORKFLOW:**

**Repository Integration**: The pipeline is triggered upon every code push to the main branch, ensuring that the latest changes are deployed immediately.

**AWS Integration**: Configured GitHub Secrets to securely manage AWS credentials for seamless interaction with the S3 bucket.

**Custom Actions:** Installed and utilized the AWS CLI to automate the synchronization of repository files with an S3 bucket (gracit.click) located in the eu-west-2 region.
Infrastructure as Code: Built the workflow using a YAML configuration file that ensures consistency, repeatability, and transparency in deployment processes.

**YAML Workflow Highlights:**
Checked out the repository using the actions/checkout GitHub Action.
Installed the AWS CLI directly on the runner to interact with the S3 bucket.
Utilized the aws s3 sync command to upload website files efficiently, preserving directory structure and updating only modified files.
This project showcases my ability to:

1. Implement CI/CD pipelines using GitHub Actions.
2. Configure secure integrations between GitHub and AWS services.
3. Automate and streamline deployment workflows for scalable and efficient delivery of web applications.
By creating this pipeline, I enhanced the reliability and speed of website updates while applying best practices in DevOps automation.

**Explanation of the GitHub Actions Workflow**
This GitHub Actions workflow automates the process of syncing the contents of the repository with an Amazon S3 bucket. Here's a breakdown of its key components:


**Workflow Name: Sync with S3**

The workflow is named Sync with S3 to describe its primary purpose: syncing the repository files with an S3 bucket.

**Trigger Event: push**

The workflow triggers automatically when changes are pushed to the main branch. This ensures the S3 bucket is always up-to-date with the latest changes in the repository.

**Job: sync**

A single job named sync is defined, which runs on the latest Ubuntu runner (ubuntu-latest).
Steps:

**Checkout Repository:**
The first step uses the actions/checkout@v2 action to clone the repository into the workflow runner. This allows access to the repository files during the workflow execution.

**Install/Update AWS CLI:**

The AWS Command Line Interface (CLI) is essential for interacting with AWS services.
The script downloads and installs the latest version of the AWS CLI using the official installer.
The --update flag ensures compatibility by updating any preexisting AWS CLI installation on the runner.
A verification command (aws --version) confirms successful installation.

**Sync with S3:**

This step uses the aws s3 sync command to upload the repository files to the specified S3 bucket (s3://gracit.click/).
Environment variables (AWS_ACCESS_KEY_ID, AWS_SECRET_ACCESS_KEY, AWS_DEFAULT_REGION) securely provide the necessary AWS credentials and region. These values are stored as GitHub Secrets for security.
Skills Demonstrated

**DevOps Practices:**

Automation of tasks using GitHub Actions to enhance efficiency and reliability.
Continuous Deployment principles by keeping the S3 bucket updated with repository changes.

**Cloud Skills:**

Proficiency in AWS services, particularly Amazon S3 and AWS CLI.
Understanding of secure access management using AWS credentials stored as GitHub Secrets.

**Linux Command Line:**

Usage of commands like curl, unzip, and sudo to install and manage software on Linux-based systems.

**Problem-Solving:**

Addressing issues like preinstalled AWS CLI conflicts by using the --update flag.

**How This Workflow Benefits Employers**

**Automation:** Reduces manual effort and ensures the deployment process is consistent and error-free.

**Security:** Demonstrates secure handling of sensitive credentials using GitHub Secrets.

**Scalability:** Provides a foundation for more complex workflows involving additional AWS services or deployment scenarios.

**Reliability:** Ensures files are always synced to the cloud, minimizing downtime and ensuring real-time updates for users.
