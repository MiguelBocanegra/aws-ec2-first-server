# AWS EC2 First Server

## Project Description

This project demonstrates how to create and connect to a Linux server using Amazon EC2 in AWS.

The goal of this project is to understand the fundamentals of cloud infrastructure such as virtual machines, SSH access, and basic server management.

## Architecture

Local Computer
|
SSH
|
Amazon EC2 Instance

<img src="./ec2-images/infra.png" width="600">

## AWS Services Used

* Amazon EC2
* AWS Security Groups
* Key Pair Authentication

## Prerequisites

Before starting this project you need:

* AWS account
* Basic Linux knowledge
* SSH client
* AWS Console access

## Steps Overview

1. Create an EC2 instance
2. Configure a security group
3. Download the key pair
4. Connect using SSH
5. Run basic Linux commands


## Implementation Steps

1. Log in to the AWS Management Console and navigate to the EC2 service
<img src="./ec2-images/step1.png" width="600">
2. Click the **Launch Instance** button to start creating a new instance.
<img src="./ec2-images/step2.png" width="600">
3. In the **Name** field, enter a name for the server.
<img src="./ec2-images/step3.png" width="600">
4. Select the required **Operating System (AMI)** for the instance.
<img src="./ec2-images/step4.png" width="600">
5. Choose the **Instance Type** according to the project requirements.
<img src="./ec2-images/step5.png" width="600">
6. In the **Key Pair** section, you can either select an existing key pair or create a new one.  
   In this case, a new key pair is created.
<img src="./ec2-images/step6.png" width="600">
7. Provide a name for the key pair and choose the key pair type and format.  
   - If you plan to connect from a Linux or macOS machine, select the **.pem** format.  
   - If you plan to connect using **PuTTY** on Windows, select the **.ppk** format.
<img src="./ec2-images/step7.png" width="600">
8. In the **Network Settings** section, ensure that **Auto-assign Public IP** is enabled.  
   Create a **Security Group** that allows inbound traffic on **port 22 (SSH)**.
<img src="./ec2-images/step8.png" width="600">
9. Click **Launch Instance** to create the EC2 instance.
<img src="./ec2-images/step9.png" width="600">
10. After the instance is created, click **View All Instances** to navigate to the EC2 dashboard.
<img src="./ec2-images/step10-1.png" width="600">
<img src="./ec2-images/step10-2.png" width="600">
11. Wait until the **Status Check** shows that all system checks have passed.  
    Once the checks are completed, the instance will be ready to connect.
<img src="./ec2-images/step11.png" width="600">
12. To connect to the server, copy the **Public IP Address** of the instance.
<img src="./ec2-images/step12.png" width="600">
13. Open a terminal and run the following command: ssh -i /path/key-pair-name.pem instance-user-name@instance-public-dns-name This command will allow you to connect to the EC2 instance via SSH.
<img src="./ec2-images/step13.png" width="600">
14. Once connected to the server, you can test the connection by updating the system packages:sudo yum update -y
<img src="./ec2-images/step14.png" width="600">


## Connect to the Server

Example connection command:

ssh -i mykey.pem ec2-user@YOUR_PUBLIC_IP

## What I Learned

* How to create a virtual machine in AWS
* How SSH authentication works
* Basic Linux server management
* Cloud infrastructure fundamentals

## Future Improvements

* Install a web server (Nginx or Apache)
* Automate instance creation using AWS CLI
* Add monitoring with CloudWatch

## Author

Miguel Bocanegra
