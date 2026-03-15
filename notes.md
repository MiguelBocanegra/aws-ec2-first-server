# Notes and Troubleshooting

## Problem

SSH connection refused.

## Cause

Port 22 was not open in the security group.

## Solution

Edit the security group and allow inbound SSH traffic.

---

## Lesson Learned

Always verify security group rules before connecting to EC2.
