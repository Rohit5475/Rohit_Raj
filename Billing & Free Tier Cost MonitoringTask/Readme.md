💰 AWS Billing & Free Tier Cost Monitoring

This project explains how to monitor AWS billing, track Free Tier usage, and prevent unexpected charges using AWS Billing Dashboard, Cost Explorer, and Budgets.

📌 Project Overview

AWS provides a Free Tier that allows new users to access selected services at no cost for a limited time. This project focuses on monitoring usage, setting alerts, and controlling costs to stay within Free Tier limits.

🛠️ AWS Services Used

AWS Billing Dashboard

AWS Free Tier

AWS Cost Explorer

AWS Budgets

Amazon CloudWatch (Billing Alarms)

IAM (Billing Access)

🎯 Project Objectives

Understand AWS Free Tier limits

Enable billing access

Monitor service usage

Track monthly AWS costs

Set budget alerts

Avoid unexpected charges

🆓 AWS Free Tier Types
1️⃣ 12-Month Free Tier

EC2 (t2.micro / t3.micro)

S3 (5 GB)

RDS

CloudWatch

2️⃣ Always Free

AWS Lambda

DynamoDB (limited usage)

SNS

3️⃣ Trials

Short-term free usage for specific services

📊 Billing Dashboard

The Billing Dashboard provides:

Month-to-date spend

Forecasted cost

Service-wise usage

Free Tier usage status

📍 Path:

AWS Console → Billing → Billing Dashboard

📈 AWS Cost Explorer

Cost Explorer helps visualize:

Daily & monthly costs

Service-wise billing

Usage trends

📍 Enable from:

Billing → Cost Explorer → Enable

🚨 Setting Up Budget Alerts
Steps:

Go to Billing → Budgets

Create a Cost Budget

Set monthly limit (e.g. $1 or $5)

Add email alerts at:

50%

80%

100%

⏰ Billing Alarm Using CloudWatch

Create a billing alarm

Set threshold (e.g. $1)

Receive email notifications via SNS

This ensures real-time cost monitoring.

🔐 Security Best Practices

Enable IAM billing access

Restrict admin privileges

Monitor unused resources

Delete idle EC2 instances

Remove unattached EBS volumes

📂 Project Structure (Example)
aws-billing-monitoring/
│
├── screenshots/
│   ├── billing-dashboard.png
│   ├── free-tier-usage.png
│   ├── cost-explorer.png
│   ├── budget-alert.png
│
├── notes.md
└── README.md

🧠 Key Learnings

AWS Free Tier limits awareness

Cost tracking & forecasting

Budget creation & alerts

Cloud cost optimization basics

📈 Future Enhancements

Multi-account billing setup

Cost anomaly detection

Automated resource cleanup

Integration with AWS Organizations

👨‍💻 Author

Rohit Raj
🎓 Cloud Computing & DevOps Learner
📍 India

⭐ Conclusion

This project helps build strong knowledge of AWS cost management, which is essential for cloud engineers, DevOps professionals, and AWS beginners.
