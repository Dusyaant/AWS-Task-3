# AWS Scalable & Secure Infrastructure Project

## 📌 Project Overview
This project demonstrates the deployment of a secure and highly available web infrastructure on AWS. It covers two primary tasks:

- **Secure Storage & Logging** – Implementing a private Amazon S3 bucket with CloudTrail and CloudWatch for activity monitoring.
- **Scalable Web Hosting** – Deploying multiple EC2 instances behind an Application Load Balancer (ALB) to ensure high availability and efficient traffic distribution.

---

# 🏗️ Architecture

The infrastructure consists of the following AWS services:

- **Amazon S3**
  - Configured with **Block All Public Access**
  - Used to securely store scripts and logs

- **AWS CloudTrail & CloudWatch**
  - Tracks S3 API activities such as `PutObject`
  - Provides real-time monitoring and audit logging

- **Amazon EC2**
  - Two `t3.micro` instances
  - Running Apache Web Server

- **Application Load Balancer (ALB)**
  - Distributes incoming traffic between EC2 instances
  - Ensures scalability and high availability

---

# 📸 Deployment Proof

## 🔐 Task 1 – Secure Logging

### Bucket Privacy
- `01-S3-Private-Access.png`
  - Confirms that public access is completely blocked

### S3 Activity
- `02-S3-File-Upload.png`
  - Shows successful upload of the test file into the S3 bucket

### CloudWatch Evidence
- `04-CloudWatch-JSON-Proof.png`
  - Displays JSON audit logs confirming the upload event was successfully tracked

---

## ⚖️ Task 2 – Load Balancing & Availability

### Instance Status
- `05-EC2-Instances-Running.png`
  - Shows both EC2 instances in healthy running state

### ALB Configuration
- `06-ALB-State-Active.png`
- `07-ALB-Listener-Rules.png`
  - Confirms the ALB is active and routing traffic correctly

### High Availability
- `08-Target-Group-Healthy.png`
  - Shows both backend servers passing health checks

### Technical Verification
- `10-ALB-DNS-Lookup-Proof.png`
  - Displays `nslookup` results proving that the public-facing IP belongs to the Load Balancer rather than individual EC2 instances

---

# 🚀 How to Access

The live application can be accessed using the Application Load Balancer DNS:

```bash
http://My-Project-ALB-1944781244.us-east-1.elb.amazonaws.com
```

---

# 🛠️ Skills Demonstrated

## 🔒 Security
- IAM
- Security Groups
- S3 Bucket Policies

## 📊 Monitoring
- AWS CloudTrail
- CloudWatch Log Groups

## 🌐 Networking
- Application Load Balancer (ALB)
- Target Groups
- DNS & `nslookup`

## 💻 Compute
- EC2 Provisioning
- User Data Scripts
- Apache Web Server Configuration

---

# 📚 Technologies Used

- Amazon EC2
- Amazon S3
- AWS CloudTrail
- Amazon CloudWatch
- Application Load Balancer
- Apache HTTP Server
- Linux

---

# ✅ Project Outcome

Successfully deployed a secure, monitored, and scalable AWS infrastructure capable of:

- Preventing unauthorized public access to cloud storage
- Monitoring and auditing storage activity in real time
- Hosting a highly available web application
- Automatically distributing traffic across multiple servers

---

# 👨‍💻 Author

**Dusyaant**  
