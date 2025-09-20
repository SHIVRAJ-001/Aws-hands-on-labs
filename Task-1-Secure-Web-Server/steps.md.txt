# Task 1: Secure Web Server Deployment (Step-by-Step)

## 1. Create IAM Role
- IAM → Roles → Create Role → Service: EC2  
- Attach Policy: `AmazonS3ReadOnlyAccess`  
- Name: `EC2-S3ReadRole`

## 2. Launch EC2 Instance
- AMI: Ubuntu 22.04 LTS  
- Type: t2.micro (Free Tier)  
- IAM Role: `EC2-S3ReadRole`  
- Security Groups: Allow SSH (22-my IP) + HTTP (80-everywhere)  
- Add extra EBS volume: 5GB

## 3. Attach & Mount EBS Volume
```bash
lsblk
sudo mkfs -t ext4 /dev/xvdf
sudo mkdir /mnt/data
sudo mount /dev/xvdf /mnt/data
echo '/dev/xvdf /mnt/data ext4 defaults 0 0' | sudo tee -a /etc/fstab
