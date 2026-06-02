# EC2 Provisioning Assignment

## 1. Instance Details
**AMI**: Ubuntu Server 22.06 LTS
**Instance Type**: t3.micro
**Region**: us-east-1 
**Public IP**: 32.196.145.117
**Private IP**: 172.31.15.109


## 2. Launch Steps
Created key pair `ec2-assignment-key.pem` and downloaded to my folder
Configured Security Group with inbound rules:
TCP 22 (SSH) from 0.0.0.0/0
TCP 80 (HTTP) from 0.0.0.0/0
Launched t3.micro instance with Ubuntu 22.06 LTS
Verified instance state = running and Status Checks = 3/3 passed

## 3. SSH Connection
Connected from Windows WSL to EC2 instance:
```bash
cd Downloads
chmod 400 ec2-assignment-key.pem
ssh -i ec2-assignment-key.pem ubuntu@32.196.145.117

## 4. **Nginx Setup**
updated apt
installed Nginx
enabled Nginx
started Nginx
check Nginx status and it was active and running
