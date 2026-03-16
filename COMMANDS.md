# 📋 Project Commands Reference

This document summarizes all the commands used to configure and manage the EC2 instance in this project.

---

## 1. Local Security Configuration
Before connecting, the private key file must have restrictive permissions to be accepted by the SSH client.

```bash
# Set read-only permissions for the owner (required for SSH)
chmod 400 /path/to/your-key-pair.pem
```
2. Remote Connection
Establish a secure shell session with the Amazon Linux instance using the default user.
```bash
# Connect to the instance using the identity file (.pem)
ssh -i /path/to/your-key-pair.pem ec2-user@instance-public-ip
```
