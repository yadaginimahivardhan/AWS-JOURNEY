# CODE IQ HUB  

## AWS Cloud Services – Day 2  

### AWS Account Setup + Free Tier Exploration  
- **AWS Free Tier overview** (Always Free vs 12 Months Free vs Trials)  
- **Billing Dashboard overview** & setting up billing alerts  
- **AWS Organizations** (high-level overview)  

### Hands-on Lab  
- Create an AWS Free Tier Account  
- Set up a Billing Alarm in CloudWatch  

---

## 1. AWS Free Tier Overview  

- **Always Free**  
  - Services always free within limits.  

- **12-Month Free Tier**  
  - Valid for 12 months from account creation.  

- **Short-Term Trials**  
  - Limited-time trials (e.g., Amazon Lightsail 750 hours for 1 month).  

---

## 2. Billing Dashboard Overview  

- Found in **AWS Management Console → Billing & Cost Management**  
- Shows:  
  - Current month charges  
  - Free Tier usage alerts  
  - Linked accounts (if using AWS Organizations)  

**Key Features:**  
- **Budgets** → Set spending limits  
- **Cost Explorer** → Visualize where money is spent  
- **Alerts** → Get notified via email when usage / cost crosses a threshold  

---

## 3. AWS Organizations (High-Level Overview)  

- **What It Is:**  
  - A service for managing multiple AWS accounts under one billing account.  

- **Benefits:**  
  - Centralized billing  
  - Service Control Policies (SCPs) for governance  
  - Easier management for teams/companies  

---

## Hands-On Labs: Step by Step  

### Create an AWS Free Tier Account  

1. Go to AWS Free Tier  
   - [AWS Sign Up](https://signin.aws.amazon.com/signup?request_type=register)  
2. Enter Account Information  
   - Provide a new email address  
   - Create a strong password  
   - Choose an AWS account name  
3. Choose Account Type  
   - Select **Personal**  
   - Enter Your Name, Contact Details, and Region  
4. Payment Information  
   - Enter a credit/debit card (needed for identity verification)  
   - AWS may charge ₹2 (refunded) to verify the card  
5. Phone Verification  
   - Enter your phone number  
   - Receive OTP via SMS or call  
   - Enter the code on the AWS page  
6. Choose a Support Plan  
   - Select **Basic Plan (Free)**  
7. Navigate to Console Page  

✅ Now your AWS account is ready!  

**YouTube Video Link:** [Watch Here](https://youtu.be/ne8LrbCzW0Q?si=my8bYKqu3UodhoYC)  

---

### How to Set Up a Billing Alarm in AWS CloudWatch  

> **Note:** Billing alarms only work in the **US East (N. Virginia) Region (us-east-1)** regardless of your account’s home region.  

#### Step 1: Enable Billing Alerts  
1. Log in to the AWS Management Console  
2. Search for **Billing**  
3. In the left menu, click **Billing Preferences**  
4. Under Billing preferences:  
   - ✅ Check **Receive Free Tier usage alerts**  
   - ✅ Check **Receive Billing Alerts**  
5. Click **Save Preferences**  

#### Step 2: Create an SNS Topic (for Email Notifications)  
1. In the AWS Console, search for **SNS (Simple Notification Service)**  
2. Click **Topics → Create Topic**  
3. Select **Standard**  
4. Enter Topic Name → `BillingAlerts`  
5. Click **Create Topic**  
6. On the new topic page, click **Create Subscription**  
7. Set Protocol → **Email**  
8. Set Endpoint → Enter your email address  
9. Click **Create Subscription**  
10. Open your email inbox and **Confirm Subscription** from the AWS email you receive  

#### Step 3: Create a Billing Alarm in CloudWatch  
1. In the AWS Console, search for **CloudWatch**  
2. In the left menu, select **Alarms → Create Alarm**  
3. Click **Select metric**  
4. In the metrics list:  
   - Choose **Billing → Total Estimated Charges → Currency: USD**  
5. Click **Select metric**  

#### Step 4: Configure the Alarm  
1. Under **Conditions**:  
   - Threshold type → **Static**  
   - Define the alarm as → **Greater than**  
   - Threshold value → e.g., **1 (for $1)**  
2. Click **Next**  
3. Under **Notification**, choose:  
   - Send a notification to an existing SNS topic  
   - Select your topic: **BillingAlerts**  
4. Name your alarm → `Billing-Alarm-1USD`  
5. Review the settings  
6. Click **Create Alarm**  

---

## ✅ Result  
You will now get an **email notification** if your AWS monthly charges cross the amount you set.  

**YouTube Video Link:** [Watch Here](https://youtu.be/f6QutICa_BY?si=fGk_500oozAYmdQD)  
