# AWS Solutions Architect Portfolio

Welcome to my AWS Solutions Architect Portfolio! This repository showcases a collection of hands-on projects designed to demonstrate my expertise in designing and deploying scalable, secure, and highly available cloud solutions using AWS services.

## Projects Included

### 1. Highly Available Web Application
- **Services:** EC2, Elastic Load Balancing, Auto Scaling, RDS
- **Highlights:** Scalability, Fault tolerance, and Cost optimization using AWS Free Tier.

### 2. Serverless Application
- **Services:** AWS Lambda, API Gateway, DynamoDB, S3
- **Highlights:** Event-driven design, automated scaling, and reduced infrastructure overhead.

### 3. Infrastructure as Code (IaC)
- **Tools:** AWS CloudFormation, Terraform
- **Highlights:** Infrastructure automation, repeatability, and environment consistency.

### 4. Data Pipeline for Analytics
- **Services:** AWS Glue, S3, Redshift
- **Highlights:** Data extraction, transformation, and loading (ETL) pipeline.

### 5. Basic AWS CloudFormation Template
- **Components:**
  - **EC2 Instance:** Runs a basic web server.
  - **S3 Bucket:** Stores static files.

#### How to Use:
1. **Deploy the CloudFormation Template:**
   - Go to the [AWS CloudFormation Console](https://console.aws.amazon.com/cloudformation).
   - Click "Create stack" and upload the `cloudformation-template.yml` file.
   - Follow the prompts to create the stack.

2. **Access the Web Application:**
   - Once the stack is created, find the EC2 instance's public IP address in the AWS Management Console under EC2 instances.

## AWS Disaster Recovery Plan

### Project Overview

This project demonstrates a disaster recovery plan for a critical application running on EC2 with data stored in EBS volumes and an RDS database. It includes the setup of AWS Backup for daily backups and the process for restoring from backups.

### Setup Instructions

#### 1. Create EC2 Instance

1. Go to the [EC2 Console](https://console.aws.amazon.com/ec2/).
2. Launch an EC2 instance with your preferred AMI (Amazon Linux, Ubuntu, etc.).
3. Configure the instance settings as needed and launch the instance.
4. Install a sample application on the instance.

#### 2. Attach EBS Volumes

1. Go to the [EC2 Console](https://console.aws.amazon.com/ec2/).
2. Create and attach one or more EBS volumes to the EC2 instance.
3. Format and mount the volumes on the instance.

#### 3. Create RDS Database

1. Go to the [RDS Console](https://console.aws.amazon.com/rds/).
2. Launch an RDS instance (e.g., MySQL, PostgreSQL).
3. Configure the database and create a sample schema and data.

#### 4. Configure AWS Backup

**Create Backup Plan:**

1. Go to the [AWS Backup Console](https://console.aws.amazon.com/backups/).
2. Create a backup plan with a daily backup schedule.
3. Include EC2 instances, EBS volumes, and RDS databases in the backup plan.

**Create Backup Vault:**

1. In the AWS Backup Console, create a backup vault.
2. Configure encryption and access policies for the vault.

**Set Up IAM Roles:**

1. Create IAM roles with permissions for AWS Backup to access EC2, EBS, and RDS resources.
2. Attach the roles to your AWS Backup plan.

**Configure Alerts:**

1. Set up CloudWatch alarms or SNS notifications for backup issues.

### Recovery Process

#### Simulate Data Loss

- Terminate the EC2 instance or delete EBS volumes to simulate data loss.
- Alternatively, delete the RDS instance for testing.

#### Restore from Backup

**EC2 Instance:**

1. Use AWS Backup to restore the EC2 instance from the latest backup.
2. Verify the instance is restored and the application is running.

**EBS Volumes:**

1. Restore EBS volumes from the backup vault.
2. Attach the restored volumes to a new EC2 instance and verify data integrity.

**RDS Database:**

1. Restore the RDS database from the backup.
2. Verify the database schema and data.

## Key Skills Demonstrated
- **AWS Best Practices:** Security, Cost Management, High Availability, and Performance Optimization.
- **Networking:** VPC setup, Subnet configurations, and Load Balancing.
- **Automation:** Deploying resources with AWS CloudFormation and Terraform.
- **Monitoring and Logging:** Using CloudWatch for logs and monitoring.
- **Database Management:** Utilizing RDS and DynamoDB for database solutions.

## Documentation

- Detailed backup and restore process is included in the [Backup and Restore Instructions](./docs/backup_restore_instructions.md).

## License

This project is licensed under the [MIT License](./LICENSE).

---

Feel free to explore the projects and replicate them to enhance your understanding of AWS cloud solutions!
