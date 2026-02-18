# aws-ec2-basic-setup
AWS EC2 Basic Setup Guide
Step 1: Launch EC2 Instance

Go to AWS Console

Select EC2 → Launch Instance

Choose Amazon Linux 2 AMI

Instance type: t2.micro (Free Tier)

Create/Select Key Pair

Configure Security Group:

Allow SSH (Port 22)

Allow HTTP (Port 80)

Step 2: Connect to EC2 (Linux/Mac)
chmod 400 key.pem
ssh -i key.pem ec2-user@<public-ip>

Step 3: Update Packages
sudo yum update -y

Step 4: Install Nginx
sudo yum install nginx -y
sudo systemctl start nginx
sudo systemctl enable nginx

Step 5: Verify

Open browser → http://<public-ip>

Concepts Learned

EC2 instance lifecycle

Security groups & networking

SSH access

Basic server configuration
