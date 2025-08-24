# AWS Resource Lister

A simple Bash script to automate listing of AWS resources across multiple services.  
This script uses the **AWS CLI** and allows you to quickly query resources in a given region.

---

## 📌 Features
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

---

## ⚙️ Prerequisites
Before using this script, ensure the following:

1. **AWS CLI Installed**  
   - [Install AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)  
   - Verify installation:  
     ```bash
     aws --version
     ```

2. **AWS CLI Configured**  
   - Configure credentials and default settings:  
     ```bash
     aws configure
     ```

3. **Execution Permission**  
   Make the script executable:
   ```bash
   chmod +x aws_resource_list.sh
````

---

## 🚀 Usage

```bash
./aws_resource_list.sh <aws_region> <aws_service>
```

### Example:

```bash
./aws_resource_list.sh us-east-1 ec2
```

This will list all **EC2 instances** in the `us-east-1` region.

---

## 📝 Supported Service Commands

Here are some examples of usage:

```bash
./aws_resource_list.sh us-east-1 ec2        # List EC2 Instances
./aws_resource_list.sh us-east-1 rds        # List RDS Instances
./aws_resource_list.sh us-east-1 s3         # List S3 Buckets
./aws_resource_list.sh us-east-1 cloudfront # List CloudFront Distributions
./aws_resource_list.sh us-east-1 vpc        # List VPCs
./aws_resource_list.sh us-east-1 iam        # List IAM Users
./aws_resource_list.sh us-east-1 route53    # List Route53 Hosted Zones
./aws_resource_list.sh us-east-1 cloudwatch # List CloudWatch Alarms
./aws_resource_list.sh us-east-1 lambda     # List Lambda Functions
./aws_resource_list.sh us-east-1 sns        # List SNS Topics
./aws_resource_list.sh us-east-1 sqs        # List SQS Queues
./aws_resource_list.sh us-east-1 dynamodb   # List DynamoDB Tables
./aws_resource_list.sh us-east-1 ebs        # List EBS Volumes
```

---

## ⚠️ Notes

* Ensure you have the necessary IAM permissions for the services you are trying to list.
* Some services (like **S3**) are global but still require a region parameter.
* If an invalid service is provided, the script will exit with an error.

---

## 📌 Version

* **v0.0.1** (2025-08-24)

---

## 👨‍💻 Author

**Shoaib Ismail**
