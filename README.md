# Basic AWS CloudFormation Template

This project contains a CloudFormation template for deploying a basic web application infrastructure on AWS.

## Project Components

- **EC2 Instance:** Runs a basic web server.
- **S3 Bucket:** Stores static files.

## How to Use

1. **Deploy the CloudFormation Template:**
   - Go to the [AWS CloudFormation Console](https://console.aws.amazon.com/cloudformation).
   - Click "Create stack" and upload the `cloudformation-template.yml` file.
   - Follow the prompts to create the stack.

2. **Access the Web Application:**
   - Once the stack is created, find the EC2 instance's public IP address in the AWS Management Console under EC2 instances.

## License

This project is licensed under the GNU General Public License v3. See the [LICENSE](LICENSE) file for details.
