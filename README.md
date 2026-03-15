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

![aws-ec2-first-server](EC2 imagenes"/Infra EC2.png)
<img src="./Infra EC2.png" alt="Infraestructura AWS" width="600">

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

<img src="./Step 1" alt="Infraestructura AWS" width="600">

4. Click the **Launch Instance** button to start creating a new instance.

5. In the **Name** field, enter a name for the server.

6. Select the required **Operating System (AMI)** for the instance.

7. Choose the **Instance Type** according to the project requirements.

8. In the **Key Pair** section, you can either select an existing key pair or create a new one.  
   In this case, a new key pair is created.

9. Provide a name for the key pair and choose the key pair type and format.  
   - If you plan to connect from a Linux or macOS machine, select the **.pem** format.  
   - If you plan to connect using **PuTTY** on Windows, select the **.ppk** format.

10. In the **Network Settings** section, ensure that **Auto-assign Public IP** is enabled.  
   Create a **Security Group** that allows inbound traffic on **port 22 (SSH)**.

11. Click **Launch Instance** to create the EC2 instance.

12. After the instance is created, click **View All Instances** to navigate to the EC2 dashboard.

13. Wait until the **Status Check** shows that all system checks have passed.  
    Once the checks are completed, the instance will be ready to connect.

14. To connect to the server, copy the **Public IP Address** of the instance.

15. Open a terminal and run the following command: ssh -i /path/key-pair-name.pem instance-user-name@instance-public-dns-name This command will allow you to connect to the EC2 instance via SSH.

16. Once connected to the server, you can test the connection by updating the system packages:sudo yum update -y



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
