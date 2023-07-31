## Lab: Introduction to Amazon VPC (Virtual Private Cloud)

**Objective**: In this lab, you will get hands-on experience setting up a basic Amazon Virtual Private Cloud (VPC) and launching an EC2 instance within that VPC.

**Prerequisites**:
- An AWS account with appropriate permissions to create VPC resources and EC2 instances.

**Step 1: Log in to the AWS Management Console**
1. Open your web browser and go to the [AWS Management Console](https://console.aws.amazon.com/).
2. Sign in using your AWS account credentials.

**Step 2: Access VPC Dashboard**
1. Once logged in, click on "Services" in the top navigation bar.
2. In the "Networking & Content Delivery" section, click on "VPC" to access the VPC Dashboard.

**Step 3: Create a VPC**
1. In the VPC Dashboard, click on "Create VPC."
2. Provide a name tag and specify the IPv4 CIDR block (e.g., 10.0.0.0/16) for your VPC.
3. Click on "Create VPC" to create the VPC.

**Step 4: Create a Subnet**
1. In the VPC Dashboard, click on "Subnets" in the left sidebar.
2. Click on "Create Subnet."
3. Choose the VPC you created in Step 3.
4. Specify the IPv4 CIDR block for the subnet (e.g., 10.0.0.0/24).
5. Click on "Create."

**Step 5: Create an Internet Gateway (IGW)**
1. In the VPC Dashboard, click on "Internet Gateways" in the left sidebar.
2. Click on "Create Internet Gateway."
3. Provide a name tag and click on "Create."

**Step 6: Attach IGW to VPC**
1. In the Internet Gateways section, select the IGW you just created.
2. Click on "Actions" and choose "Attach to VPC."
3. Select the VPC you created earlier and click on "Attach."

**Step 7: Configure a Route Table**
1. In the VPC Dashboard, click on "Route Tables" in the left sidebar.
2. Select the default route table and click on "Edit Routes."
3. Add a new route with destination "0.0.0.0/0" and target as the IGW you attached in Step 6.
4. Save the changes.

**Step 8: Launch an EC2 Instance Inside the VPC**
1. Go to the EC2 Dashboard as described in Lab 1.
2. Click on "Launch Instance."
3. Choose an AMI, instance type, and other configurations as desired.
4. In the "Configure Instance Details" step, choose the VPC and subnet you created earlier.
5. Complete the instance launch process following the steps provided in Lab 1.

**Step 9: Access and Connect to the EC2 Instance**
1. Follow Step 4 in Lab 1 to access and connect to the EC2 instance launched inside the VPC.

**Step 10: Terminate the EC2 Instance and Clean Up**
1. Once you have finished testing the VPC and EC2 instance, return to the EC2 Dashboard and terminate the instance as shown in Lab 1.
2. You can also delete the VPC, subnets, and internet gateway to clean up the resources created during the lab.