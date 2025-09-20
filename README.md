# ☁️ AWS Hands-on Labs

This repository contains my AWS practical labs and projects where I implement real-world scenarios to strengthen my cloud skills.  
Each task is documented with steps, architecture diagrams, and screenshots for clarity.  

---

## 🚀 Task 1: Secure Web Server Deployment

**Objective:**  
Deploy a secure web server on an EC2 instance with IAM role, EBS volume, and S3 integration.  

**Services Used:**  
- IAM (Role with S3 ReadOnly Access)  
- EC2 (Ubuntu Instance)  
- EBS (Extra 5GB Volume)  
- S3 (Image storage for website)  
- Security Groups  

**Implementation Steps:**  
1. Created an IAM Role with `AmazonS3ReadOnlyAccess` and attached it to EC2.  
2. Launched EC2 instance with security groups (SSH + HTTP).  
3. Added extra EBS volume (5GB), formatted and mounted it at `/mnt/data`.  
4. Installed Apache web server and hosted a simple website.  
5. Pulled an image from S3 bucket using AWS CLI (thanks to IAM Role) and displayed it on the website.  

**Architecture:**  
![Architecture](Task-1-Secure-Web-Server/architecture.png)  

**Output:**  
![Output](Task-1-Secure-Web-Server/screenshots/website.png)  

---

## 📌 Next Planned Labs
- **Task 2:** Backup & Recovery using EBS Snapshots  
- **Task 3:** Multi-User Access with IAM Policies  
- **Task 4:** Cost Optimization with Spot Instances  
- **Task 5:** Deploy WordPress Blog with Auto Scaling  

---

## 👨‍💻 Author
**[shivraj]** – AWS Enthusiast | B.Tech (IT) | Cloud Learner  
