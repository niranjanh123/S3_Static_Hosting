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


# Terraform S3 Static Website Hosting

This Terraform configuration sets up an S3 bucket to host a static website with public access and error handling.

## Resources

### `aws_s3_bucket`
- Creates an S3 bucket for static website hosting.

### `aws_s3_bucket_ownership_controls`
- Ensures objects in the S3 bucket are owned by the bucket owner.

### `aws_s3_bucket_public_access_block`
- Allows public access by disabling default AWS restrictions.

### `aws_s3_bucket_acl`
- Grants `public-read` access to the S3 bucket.

### `aws_s3_bucket_object`
- Uploads `index.html` and `error.html` to the S3 bucket.

### `aws_s3_bucket_website_configuration`
- Configures the bucket for static website hosting, specifying the index and error documents.

### `output`
- Displays the static website URL after the deployment is completed.

## Example Output

![S3 static 1](https://github.com/user-attachments/assets/fd0f1b61-9c2d-4ee2-a8f0-bd6fcbb15cc7)

![S3 static 2](https://github.com/user-attachments/assets/ee3b1cdd-781e-4c7d-a381-a944af2ed494)



