## Lab: Basics of EC2 - Creating Your First EC2 Instance

**Objective**: In this lab, you will learn the basics of Amazon Elastic Compute Cloud (EC2) and how to create an EC2 instance using the AWS Management Console.

**Prerequisites**:
- An AWS account with appropriate permissions to create EC2 instances.

**Step 1: Log in to the AWS Management Console**
1. Open your web browser and go to the [AWS Management Console](https://console.aws.amazon.com/).
2. Sign in using your AWS account credentials.

**Step 2: Access EC2 Dashboard**
1. Once logged in, click on "Services" in the top navigation bar.
2. In the "Compute" section, click on "EC2" to access the EC2 Dashboard.

**Step 3: Launch an EC2 Instance**
1. In the EC2 Dashboard, click on "Launch Instance."
2. Choose an Amazon Machine Image (AMI) - Select the desired operating system for your instance (e.g., Amazon Linux, Ubuntu, Windows, etc.).
3. Choose an Instance Type - Select the instance type based on your requirements (e.g., t2.micro for a free-tier eligible option).
4. Configure Instance Details - Set configurations for your instance (e.g., number of instances, VPC settings, subnet, etc.).
5. Add Storage - Configure the storage settings for your instance (e.g., storage type, size).
6. Add Tags (optional) - Add any tags to easily identify your instance.
7. Configure Security Group - Set up the security group to control inbound and outbound traffic to your instance.
8. Review - Review all the configurations and click on "Launch."

**Step 4: Access and Connect to Your EC2 Instance**
1. Select the newly created instance from the Instances list in the EC2 Dashboard.
2. Click on "Connect" to view the instructions on how to connect to your instance using SSH or RDP, depending on your chosen operating system.

**Step 5: Terminate the EC2 Instance**
1. After exploring and testing your instance, return to the EC2 Dashboard.
2. Select the instance you created and click on "Instance State" in the top menu.
3. From the dropdown, select "Terminate Instance" to delete the instance and associated resources.

