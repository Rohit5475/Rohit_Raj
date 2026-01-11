🌐 AWS VPC (Virtual Private Cloud)

This project demonstrates the creation and configuration of an AWS Virtual Private Cloud (VPC) to build a secure, isolated networking environment for cloud resources such as EC2 instances.

🔍 What is AWS VPC?

A Virtual Private Cloud (VPC) is a logically isolated virtual network in Amazon Web Services that allows you to launch AWS resources in a custom-defined network with complete control over IP addressing, subnets, routing, and security.

🖼️ VPC Architecture Overview
4
🛠️ AWS Services Used

Amazon VPC

Subnets (Public & Private)

Internet Gateway (IGW)

NAT Gateway

Route Tables

Security Groups

Network ACLs

Amazon EC2

🎯 Project Objectives

Create a custom VPC

Design public and private subnets

Configure route tables

Enable internet access using IGW

Provide outbound internet access using NAT Gateway

Secure resources using Security Groups & NACLs

🧱 VPC Components Explained
🔹 VPC

CIDR Block (example): 10.0.0.0/16

Provides isolated networking environment

🔹 Subnets

Public Subnet: Resources accessible from the internet

Private Subnet: Resources isolated from direct internet access

🔹 Internet Gateway (IGW)

Allows communication between VPC and the internet

🔹 NAT Gateway

Enables private subnet instances to access the internet securely

🔹 Route Tables

Controls traffic routing within the VPC

🗺️ Network Flow Example
User → Internet → Internet Gateway → Public Subnet (EC2)
                         ↓
                    NAT Gateway
                         ↓
                  Private Subnet (EC2)

📂 Project Structure (Example)
aws-vpc-project/
│
├── diagrams/
│   ├── vpc-architecture.png
│   ├── public-private-subnet.png
│
├── notes.md
└── README.md

🔐 Security Best Practices

Use private subnets for databases

Allow minimum inbound traffic

Separate public and private workloads

Use Security Groups as firewalls

Apply Network ACLs for additional security

🧠 Key Learnings

Cloud networking fundamentals

Subnet design & IP planning

Secure internet access patterns

AWS networking best practices

📈 Future Enhancements

Multi-AZ architecture

VPC Peering

Transit Gateway

VPN / Direct Connect integration

Infrastructure as Code (Terraform / CloudFormation)

👨‍💻 Author

Rohit Raj
🎓 Cloud & DevOps Learner
📍 India

⭐ Conclusion

This project builds a strong foundation in AWS networking, which is essential for Cloud Engineers, DevOps Engineers, and Solutions Architects.

🌐 AWS VPC – Networking & Subnetting

This project demonstrates how to design and configure an AWS Virtual Private Cloud (VPC) with proper networking and subnetting, enabling secure and scalable cloud infrastructure.

🔍 What is AWS VPC?

A Virtual Private Cloud (VPC) is a logically isolated virtual network in Amazon Web Services that allows you to launch AWS resources in a controlled networking environment.

You can define:

IP address ranges (CIDR)

Subnets

Route tables

Internet & NAT gateways

Network security

🖼️ VPC Architecture with Networking
4
🛠️ AWS Services Used

Amazon VPC

Public & Private Subnets

CIDR Blocks

Internet Gateway (IGW)

NAT Gateway

Route Tables

Security Groups

Network ACLs

Amazon EC2

🎯 Project Objectives

Understand networking basics

Design IP addressing using CIDR

Implement subnetting

Create public & private subnets

Configure routing & gateways

Secure network traffic

🌍 Networking Basics
🔹 IP Addressing

AWS VPC uses IPv4 CIDR notation to define IP ranges.

Example:

10.0.0.0/16


/16 → Network bits

Allows 65,536 IP addresses

🧮 Subnetting in AWS VPC

Subnetting divides a large network into smaller networks for better organization and security.

Example Subnet Design
Subnet Type	CIDR Block	AZ	Purpose
Public Subnet	10.0.1.0/24	AZ-1	Web servers
Private Subnet	10.0.2.0/24	AZ-1	App servers
Private DB Subnet	10.0.3.0/24	AZ-2	Databases
🧱 Public vs Private Subnets
🔓 Public Subnet

Connected to Internet Gateway

Used for:

Web servers

Bastion hosts

🔒 Private Subnet

No direct internet access

Uses NAT Gateway for outbound traffic

Used for:

Databases

Backend services

🌐 Internet Gateway (IGW)

Enables inbound & outbound internet access

Attached directly to the VPC

Required for public subnets

🔁 NAT Gateway

Allows private subnet instances to access the internet

Prevents inbound internet access

Placed inside a public subnet

🗺️ Route Tables

Route tables control how traffic flows within the VPC.

Example Routes
Destination	Target
10.0.0.0/16	Local
0.0.0.0/0	Internet Gateway (Public)
0.0.0.0/0	NAT Gateway (Private)
🔐 Network Security
🔹 Security Groups

Instance-level firewall

Stateful

Allows inbound & outbound rules

🔹 Network ACLs

Subnet-level firewall

Stateless

Controls traffic at subnet boundary

🧭 Network Flow Diagram
User → Internet → Internet Gateway
                   ↓
              Public Subnet (EC2)
                   ↓
              NAT Gateway
                   ↓
              Private Subnet (EC2 / DB)

📂 Project Structure (Example)
aws-vpc-networking/
│
├── diagrams/
│   ├── vpc-architecture.png
│   ├── subnetting-diagram.png
│
├── notes.md
└── README.md

🧠 Key Learnings

Cloud networking fundamentals

CIDR & subnet calculations

Public vs private architecture

Secure network design

AWS routing mechanisms

📈 Future Enhancements

Multi-AZ high availability

VPC Peering

Transit Gateway

VPN / Direct Connect

Infrastructure as Code (Terraform)

👨‍💻 Author

Rohit Raj
🎓 Cloud & DevOps Learner
📍 India

⭐ Conclusion

This project builds strong foundations in AWS networking and subnetting, which are critical skills for Cloud Engineers, DevOps Engineers, and AWS Solutions Architects.
