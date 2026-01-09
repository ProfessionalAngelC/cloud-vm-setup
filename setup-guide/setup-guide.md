# AWS EC2 VM Setup Guide

## 1. EC2 Instance Creation
1. Log in to AWS Management Console
2. Navigate to EC2 → Launch Instance
3. Choose AMI (Ubuntu 22.04 LTS or Windows Server 2022)
4. Choose Instance Type (t2.micro for free tier)
5. Configure Network & Security
   - Security group rules: SSH (22) for Linux / RDP (3389) for Windows
   - Optional: HTTP (80) for web server
6. Add storage: 8GB default, optional 10GB extra
7. Add tags: `Name: Portfolio-VM`
8. Launch instance → Create new key pair (download `.pem` or `.ppk`)

## 2. Connecting to VM
- Linux (SSH):
```bash
chmod 400 mykey.pem
ssh -i "mykey.pem" ubuntu@<Public-IP>

