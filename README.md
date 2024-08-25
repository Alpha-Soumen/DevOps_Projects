# AWS Resource Lister

A simple Bash script to automate the process of listing resources in an AWS account. This script supports various AWS services and allows users to quickly retrieve information about their AWS resources.

## Supported Services

The script currently supports listing resources for the following AWS services:
- EC2
- RDS
- S3
- CloudFront
- VPC
- IAM
- Route53
- CloudWatch
- CloudFormation
- Lambda
- SNS
- SQS
- DynamoDB
- EBS

## Usage

To use the script, you need to have the AWS CLI installed and configured. The script takes two arguments:
1. **aws_region**: The AWS region where you want to list the resources.
2. **aws_service**: The AWS service for which you want to list the resources.

### Example

```bash
./aws-resource-lister.sh us-east-1 ec2
