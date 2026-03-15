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
