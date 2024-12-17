**PROJECT: CI/CD PIPELINE FOR VERA AIDOO - PORTFOLIO WEBSITE**

I developed a CI/CD pipeline for my portfolio website using GitHub Actions and integrated it with Amazon S3 for automated deployment. 
This workflow streamlined the process of syncing website updates to the hosting environment directly from my GitHub repository.

**KEY FEATURES AND WORKFLOW:**

**Repository Integration**: The pipeline is triggered upon every code push to the main branch, ensuring that the latest changes are deployed immediately.

**AWS Integration**: Configured GitHub Secrets to securely manage AWS credentials for seamless interaction with the S3 bucket.
Custom Actions: Installed and utilized the AWS CLI to automate the synchronization of repository files with an S3 bucket (gracit.click) located in the eu-west-2 region.
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
