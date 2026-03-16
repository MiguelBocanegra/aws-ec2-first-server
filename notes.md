# Troubleshooting Notes

This document contains issues encountered while deploying and connecting to the EC2 instance and how they were resolved.

---

## Issue 1 — SSH Connection Refused

### Problem
Unable to connect to the EC2 instance using SSH.

### Error Message
Connection refused

### Root Cause
Port **22 (SSH)** was not allowed in the Security Group inbound rules.

### Solution

1. Navigate to the EC2 Dashboard
2. Select the instance
3. Click the **Security Group**
4. Edit **Inbound Rules**
5. Add the following rule:

| Type | Protocol | Port | Source |
|-----|------|------|------|
| SSH | TCP | 22 | My IP |

### Verification

Test the connection again using:

```bash
ssh -i mykey.pem ec2-user@YOUR_PUBLIC_IP
