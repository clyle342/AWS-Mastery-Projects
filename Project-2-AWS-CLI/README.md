# Project 2: Command-Line Mastery with AWS CLI for Ndombson & Co.

## Objective
Installed and configured the AWS CLI to manage S3 buckets and objects programmatically for Ndombson & Co., enabling efficient cloud resource management.

## AWS Services Used
- AWS CLI
- Amazon S3

## Steps
1. **Installed AWS CLI**: Installed AWS CLI v2 on my laptop and verified with `aws --version`.
2. **Configured AWS CLI**: Created an IAM user (`Ndombson-CLI-User`) with `AmazonS3FullAccess` and configured CLI with access keys.
3. **Managed S3 Buckets**:
   - Created a bucket: `ndombson-co-freewater-254>`.
   - Uploaded a `water.txt` file and set public-read access.
   - Listed and downloaded the file to verify functionality.
4. **Completed Quiz**: Answered 5 questions on CLI setup and S3 commands.
5. **Cleaned Up**: Deleted the S3 bucket and deactivated IAM user access keys.

## Screenshots
- AWS CLI Version
- CLI Configuration
- S3 Bucket Creation
- S3 File Upload
- S3 Bucket Listing

## Code Snippets
```bash
#!bin/bash
# This script contains commands to interact with AWS S3 using the AWS CLI.
# Ensure AWS CLI is installed and configured with appropriate permissions
# List all S3 buckets
aws s3 ls
# Create a new S3 bucket
aws s3 mb s3://ndombson-co-freewater-254 --region us-east-1 # Upload a file to the S3 bucket
aws s3 mb s3://ndombson-co-freewater-254 --region us-east-1 
aws s3 cp C:\Users\Kali\Desktop\AWS-Mastery-Projects\Project-2-AWS-CLI\water.txt s3://ndombson-co-freewater-254/ # List contents of the S3 bucket
aws s3 ls s3://ndombson-co-freewater-254/ # Download a file from the S3 bucket
aws s3 cp s3://ndombson-co-freewater-254/water.txt C:\Users\Kali\Desktop\AWS-Mastery-Projects\Project-2-AWS-CLI\water_downloaded.txt # Delete a file from the S3 bucket
aws s3 rm s3://ndombson-co-freewater-254/water.txt # Sync a local directory with the S3 bucket