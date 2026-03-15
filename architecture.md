Architecture

This project uses a simple cloud architecture:

User Computer
|
SSH Connection
|
Amazon EC2 Instance (Linux Server)

Components:

User Computer
Used to connect to the server via SSH.

Security Group
Allows inbound SSH traffic (port 22).

EC2 Instance
Virtual Linux server running in AWS.
