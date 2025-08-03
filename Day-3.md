# CODE IQ HUB  

## AWS Cloud Services – Day 3  

### Topics Covered  
- IAM Users, Groups, Policies, MFA  
- Hands-on: Create IAM user with MFA enabled  

---

## What is IAM?  

- **AWS IAM (Identity and Access Management)** is a service provided by Amazon Web Services (AWS) that helps you manage access to your AWS resources.  
- It acts as a **security system** for your AWS account.  
- With IAM you can:  
  - Create and manage **users, groups, and roles**  
  - Control and define permissions through **policies** (in JSON format)  
  - Enforce the **principle of least privilege**  
  - Use **Multi-Factor Authentication (MFA)** for stronger security  
  - Track user activity and permission changes with **audit trails**  

**Key Benefits of IAM:**  
- Granular access control  
- Enhanced security with MFA  
- Reduced risk of unauthorized access  
- Centralized management for identities  

---

## Components of IAM  

### Users  
- Represent individual people or entities (such as apps or services).  
- Each user has a **unique name and credentials** (password or access keys).  

### Groups  
- Collections of users with similar access requirements.  
- Permissions can be assigned at the group level.  
- Users can be added or removed as needed.  

### Roles  
- Provide **temporary access** to AWS resources.  
- Commonly used by **applications or external services**.  
- Have associated **policies** defining allowed actions.  

### Policies  
- JSON documents that define permissions.  
- Specify **actions** and **resources** they apply to.  
- Can be attached to **users, groups, or roles**.  
- Types:  
  - **AWS managed policies** (predefined by AWS)  
  - **Customer managed policies** (created by you)  

### Multi-Factor Authentication (MFA)  
- Adds an extra layer of security:  
  - **Password** + **One-time code** from an authenticator app/device.  
- Can be:  
  - **App-based** (Google Authenticator, Authy, AWS Virtual MFA)  
  - **Hardware-based**  

---

## Hands-On Lab: Create IAM User with MFA Enabled  

**Goal:** Create a new user with limited permissions and enable MFA.  

### Step 1: Sign in as Root or Admin  
- Log in to **AWS Management Console**  
- Ensure you’re in your **preferred region**  

### Step 2: Create an IAM Group  
1. Navigate to **IAM → User groups → Create group**  
2. Name it: `DevelopersGroup`  
3. Attach Policy: `AmazonS3ReadOnlyAccess` (or another of your choice)  
4. Click **Create group**  

### Step 3: Create IAM User  
1. Go to **IAM → Users → Add users**  
2. Enter Username: `dev-user01`  
3. Select **Provide user access to the AWS Management Console**  
4. Set console password (auto-generated or custom)  
5. Add user to group → select **DevelopersGroup**  
6. Click **Create user**  

✅ User is created with group permissions.  

### Step 4: Enable MFA  
1. Go to **IAM → Users → dev-user01 → Security credentials**  
2. In **Multi-factor authentication (MFA)** section → Click **Assign MFA device**  
3. Choose **Virtual MFA device**  
4. Open Authenticator app (Google Authenticator, Authy, etc.)  
5. Scan the **QR code** provided by AWS  
6. Enter two consecutive codes from the app  
7. Click **Assign MFA**  

✅ MFA is now enabled.  

### Step 5: Test the Login  
1. Sign out from the **root/admin account**  
2. Log in as `dev-user01` → Enter username & password  
3. You’ll be prompted for the **MFA code**  
4. Enter code → ✅ Success  

---

## ✅ What You Learned  
- Created **IAM Group** for permissions  
- Added **IAM User** with secure login  
- Attached **policy for least privilege**  
- Enabled **MFA for enhanced security**  

---

## Interview Questions  

**Q1: What is AWS IAM, and why is it important?**  
A: AWS IAM is a service that helps you control access to your AWS resources. It manages user identities, permissions, and policies. IAM is important because it ensures **only authorized entities have access**, enforces the **principle of least privilege**, and helps maintain a secure environment.  

**Q2: What is the difference between IAM users and IAM roles?**  
A:  
- **IAM Users** → Represent individuals needing access, with long-term credentials.  
- **IAM Roles** → Provide **temporary access**, usually for applications or external services.  

**Q3: What are IAM policies, and how do they work?**  
A: IAM policies are **JSON documents** that define permissions. They specify what actions are allowed or denied on AWS resources. If a requested action matches an allowed action, access is granted; otherwise, it’s denied.  

**Q4: What is the principle of least privilege, and why is it important in IAM?**  
A: It means giving users only the permissions they need to do their job — no more. This minimizes risks of unauthorized access and limits potential damage from compromised accounts.  

**Q5: What is an AWS managed policy?**  
A: An **AWS managed policy** is a predefined policy created and updated by AWS. They cover common use cases and stay updated with new services and features. They can be attached to users, groups, or roles.  
