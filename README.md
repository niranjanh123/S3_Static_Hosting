# S3 Static Website Hosting with Terraform

This repository provides Terraform configurations to set up a static website hosted on Amazon S3.

## Prerequisites

- **Terraform**: Ensure Terraform is installed on your system. [Installation Guide](https://learn.hashicorp.com/tutorials/terraform/install-cli)
- **AWS Account**: An active AWS account with necessary permissions to create S3 buckets and manage related resources.
- **AWS CLI**: Installed and configured with your AWS credentials. [AWS CLI Installation](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html)

## Repository Structure

- `main.tf`: Contains the main Terraform configuration for the S3 bucket and its settings.
- `providers.tf`: Specifies the AWS provider configuration.
- `variables.tf`: Defines variables used in the Terraform configurations.
- `index.html`: The main HTML file for your static website.
- `error.html`: Custom error page displayed for 404 errors.
- `.gitignore`: Specifies files and directories to be ignored by Git.

## Setup Instructions

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/niranjanh123/S3_Static_Hosting.git
   cd S3_Static_Hosting
   ```

2. **Initialize Terraform**
   ```bash
   terraform init
   ```

3. **Review and Apply Configuration**
   ```bash
   terraform plan
   terraform apply
   ```

**NOTE**
Create your own index.html file and error.html for testing the website.
The main.tf file configures an S3 bucket with public read access and enables static website hosting.
Ensure that your AWS credentials are configured correctly and have the necessary permissions to create and manage S3 resources.
