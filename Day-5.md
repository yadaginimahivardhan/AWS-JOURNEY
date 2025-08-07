# CODE IQ HUB

## AWS Cloud Services

---

## Day 5: AWS Well-Architected Framework & Case Studies

---

###  AWS Well-Architected Framework – 5 Pillars

The AWS Well-Architected Framework provides a set of best practices to build **secure, high-performing, resilient, and efficient infrastructure** for cloud applications.

---

### 1. Operational Excellence  
**Focus:** Run and monitor systems to deliver business value and continually improve processes.

**Best Practices:**
- Automate deployments using **Infrastructure as Code (IaC)** (AWS CloudFormation, Terraform).
- Monitor and log using **Amazon CloudWatch**.
- Regularly update operational procedures.

---

### 2. Security  
**Focus:** Protect data, systems, and assets while delivering business value.

**Best Practices:**
- Use **IAM** with **least privilege access**.
- Enable **Multi-Factor Authentication (MFA)**.
- Encrypt data in transit (TLS) and at rest (KMS, S3 SSE).
- Use **AWS Security Hub** and **GuardDuty** for threat detection.

---

### 3. Reliability  
**Focus:** Ensure workloads perform correctly and consistently.

**Best Practices:**
- Design with **Multi-AZ / Multi-Region** for high availability.
- Use **Auto Scaling** to manage variable loads.
- Perform regular backups with **AWS Backup**.

---

### 4. Performance Efficiency  
**Focus:** Use resources efficiently and scale with demand.

**Best Practices:**
- Use **AWS Compute Optimizer** to choose the right instance types.
- Deploy **Amazon CloudFront** for low latency.
- Implement **serverless computing (AWS Lambda)**.

---

### 5. Cost Optimization  
**Focus:** Avoid unnecessary costs and invest wisely.

**Best Practices:**
- Track spend with **AWS Cost Explorer** and **Budgets**.
- **Right-size** resources and use **Reserved Instances/Savings Plans**.
- Use **S3 lifecycle policies** to move data to lower-cost storage.

---

##  Case Studies on Best Practices

---

###  Case Study 1: **Netflix (Scalability & Reliability)**  
**Challenge:** Stream millions of videos globally.  
**Best Practices Used:**
- Multi-Region deployment for reliability.  
- **Auto Scaling** & **Elastic Load Balancing** for traffic spikes.  
- **CloudFront** for faster content delivery.

---

###  Case Study 2: **Airbnb (Cost Optimization & Performance)**  
**Challenge:** Handle millions of bookings without high cost.  
**Best Practices Used:**
- **Serverless** backend using **AWS Lambda**.  
- **DynamoDB** for fast database queries.  
- **Spot Instances** to save on compute costs.

---

###  Case Study 3: **Capital One (Security & Compliance)**  
**Challenge:** Meet strict security requirements for financial data.  
**Best Practices Used:**
- Strong **IAM controls**, **MFA**, and role-based access.  
- Encryption using **AWS KMS**.  
- Threat monitoring with **GuardDuty** and **Security Hub**.

---

###  Case Study 4: **NASA (Operational Excellence)**  
**Challenge:** Process large volumes of space mission data.  
**Best Practices Used:**
- **Automated data pipelines** using **Lambda** + **S3**.  
- Use **CloudWatch** for monitoring.  
- **Auto Scaling** to handle variable workloads.

---
