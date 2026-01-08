# 🚀 Automating EC2 Start–Stop Using AWS Lambda & Amazon EventBridge

## 📌 Overview
This project demonstrates how to automatically start and stop Amazon EC2 instances at scheduled times using AWS Lambda and Amazon EventBridge.  
It helps reduce AWS costs by ensuring EC2 instances run only when required.

---

## 🎯 Use Case
- Start EC2 instances during working hours
- Stop EC2 instances after business hours
- Automate EC2 management
- Reduce unnecessary cloud costs

---

## 🛠️ AWS Services Used
- AWS Lambda (Python 3.10)
- Amazon EventBridge (Scheduled Rules)
- Amazon EC2
- AWS IAM
- Amazon CloudWatch

---

## 🧩 Architecture Flow
1. Amazon EventBridge triggers the Lambda function using a cron schedule (UTC)
2. Lambda checks the EC2 instance state
3. Lambda starts or stops the EC2 instance
4. Multiple EventBridge rules can be used for different schedules

---

## ⚙️ Prerequisites
- AWS Account
- Basic knowledge of:
  - EC2
  - AWS Lambda
  - IAM roles
  - Cron expressions
- EC2 Instance ID

---

## 🧪 Implementation Steps

### 1️⃣ Create Lambda Function
- Runtime: Python 3.10
- Paste EC2 start–stop logic
- Deploy the function

---

### 2️⃣ Configure Lambda Settings
- Increase timeout to 30 seconds
- Add Environment Variable:
  - Key: `TZ`
  - Value: `UTC`

---

### 3️⃣ Create EventBridge Scheduled Rules
- Go to Amazon EventBridge → Rules
- Create a Scheduled rule
- Define cron expression (UTC)
- Select Lambda as target
- Create a new IAM role

> Repeat these steps to create multiple rules if required

---

### 4️⃣ Add EventBridge Triggers to Lambda
- Open Lambda → Configuration → Triggers
- Select EventBridge (CloudWatch Events)
- Attach created rules

---

## 📈 Benefits
- Cost optimization
- Fully automated EC2 scheduling
- No manual intervention
- Serverless architecture
- Beginner-friendly AWS project

---

## 📂 Repository Structure
.
├── lambda_function.py
├── README.md
└── screenshots/

---

## 🧠 Key Learnings
- AWS Lambda automation
- Event-driven scheduling using EventBridge
- IAM role usage
- EC2 lifecycle management
- Cloud cost optimization

---

## 🏷️ Tags
aws, aws-lambda, amazon-eventbridge, ec2, serverless, devops, cloud-automation, python

---

## 🤝 Connect
Feel free to fork this repository and use it for learning or practice.

