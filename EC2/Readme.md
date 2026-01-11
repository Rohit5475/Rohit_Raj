☁️ AWS EC2 (Elastic Compute Cloud)

This project demonstrates the creation, configuration, and management of an AWS EC2 instance to deploy and host applications on the cloud. It covers core concepts such as instance launch, security groups, key pairs, and web server deployment.

📌 What is AWS EC2?

Amazon Elastic Compute Cloud (EC2) provides scalable virtual servers (instances) in the cloud. It allows users to run applications with full control over computing resources.

🛠️ Services & Tools Used

AWS EC2

Amazon Linux / Ubuntu

SSH (Key Pair Authentication)

Security Groups

Elastic IP

Apache / Nginx Web Server

AWS Management Console

⚙️ Project Objectives

Launch an EC2 instance

Configure security groups

Connect to EC2 using SSH

Deploy a web application

Host a website on EC2

Understand cloud infrastructure basics

🚀 Steps to Create an EC2 Instance
1️⃣ Launch Instance

Login to AWS Console

Go to EC2 → Launch Instance

Choose AMI (Amazon Linux / Ubuntu)

Select instance type (t2.micro – Free Tier)

2️⃣ Configure Settings

Create or select a Key Pair

Configure Security Group

Allow SSH (22)

Allow HTTP (80)

3️⃣ Connect to Instance
ssh -i key.pem ec2-user@<public-ip>

🌐 Web Server Deployment
Install Apache (Amazon Linux)
sudo yum update -y
sudo yum install httpd -y
sudo systemctl start httpd
sudo systemctl enable httpd

Install Nginx (Ubuntu)
sudo apt update
sudo apt install nginx -y

🖼️ Architecture Overview
User → Internet → AWS EC2 Instance → Web Server → Application

📂 Project Structure (Example)
ec2-project/
│
├── screenshots/
│   ├── ec2-instance.png
│   ├── security-group.png
│   ├── website-running.png
│
├── deployment-notes.md
└── README.md

🔐 Security Best Practices

Use key-based authentication

Restrict inbound rules in security groups

Disable root login

Use Elastic IP for stable access

Regularly update instance packages

🎯 Use Cases

Website hosting

Backend server

Dev/Test environment

Learning AWS Cloud

Portfolio cloud project

📈 Future Enhancements

Add Load Balancer (ELB)

Auto Scaling Group

HTTPS using SSL (ACM)

Dockerized deployment

CI/CD with GitHub Actions

👨‍💻 Author

Rohit Raj
🎓 Cloud & Web Development Learner
📍 India

⭐ Conclusion

This EC2 project provides hands-on experience with cloud computing fundamentals and helps build a strong foundation for AWS, DevOps, and Cloud Engineer roles.
