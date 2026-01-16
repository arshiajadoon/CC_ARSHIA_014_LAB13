# Lab 13: Terraform IAM Management and S3 Backend

## Project Overview
This project demonstrates the use of **Terraform** to automate the creation of AWS IAM resources and manage the infrastructure state using a **Remote S3 Backend**.

## Tasks Completed

### 1. AWS CLI Configuration
* Installed and configured AWS CLI in GitHub Codespaces.
* Verified credentials using `aws configure` and set the `AWS_SESSION_TOKEN` for AWS Academy.

### 2. Infrastructure Setup (Terraform)
* Configured S3 as a remote backend to store the `terraform.tfstate` file.
* Successfully initialized the backend using `terraform init -reconfigure`.
* Created 7 IAM resources including users, groups, and policies.

### 3. IAM User Verification
* Created an IAM user with a login password.
* Verified the login process and password reset prompt in the AWS Console.

### 4. Cleanup and State Management
* Executed `terraform destroy` to remove all resources.
* Verified that the S3 state file was removed and the bucket is empty for Task 6.

## Screenshots
All required lab screenshots are stored in the `/screenshots` directory:
* `task4_aws_cli_verify.png`
* `task4_aws_console_login.png`
* `task4_aws_console_password_reset.png`
* `task6_s3_tfstate_destroyed.png`

## How to Run
1. Update `main.tf` with your unique bucket name (e.g., `arshia014`).
2. Run `terraform init -upgrade`.
3. Run `terraform apply -var="iam_password=YourPassword!"`.
