### 🛡️ IAM Security Infrastructure – Mini Project

A mini project to implement a secure IAM (Identity and Access Management) model on AWS.
The project demonstrates how to use Users, Groups, Roles, and Policies to provide controlled access for different teams in an organization.

### 🚀 Project Overview

Implemented IAM security model with multiple teams: Developers, Database Admins, and Security Auditors.

Applied least privilege principle for each group.

Configured MFA (Multi-Factor Authentication) for additional security.

Added role assumption via STS for temporary permissions.

### 🏗️ Architecture
<p align="center"> <img width="500" alt="IAM Architecture" src="https://github.com/sayaliparhar/IAM-Miniproject/blob/master/Architecture/IAM-Architecture.png?raw=true" /> </p>


### 👥 Teams & Permissions

**👨‍💻 Developers Team**

EC2 → start/stop/describe instances.

S3 → read & write access.

**🗄️ Database Admins Team**

Full access to RDS.

❌ No access to IAM resources.

**🔒 Security Auditors Team**

Read-only access to IAM roles, policies, and CloudTrail logs.

### 🔐 Security Enhancements

Enforced MFA for all IAM users.

Used TOTP-based virtual MFA for secure logins.

Implemented custom IAM policies for least privilege.

### ✅ Test Cases

EC2 instance access.

S3 → upload, download, delete.

RDS → full access verified.

IAM → restricted & read-only actions.

CloudTrail → read-only access.

🗂️ **Note:** All detailed screenshots for the test cases are available in the [TestCases](./TestCases) folder of this repository.  


### ⚡ Advanced Challenge

Created S3ReadOnlyRole with read-only access to S3.

Used STS AssumeRole to allow developers temporary access.

Tested using both AWS Console and AWS CLI.

🗂️ **Note:** All detailed screenshots for advanced challenge are available in the [TestCases](./TestCases/Role) folder of this repository.  

### 📝 Conclusion

✔️ Successfully implemented a secure IAM model with:

Controlled team-based access.

MFA for strong authentication.

Role assumption for temporary permissions.

This ensures security, scalability, and least privilege access across the organization.

👉 Note: This was a demo project for learning IAM.
All IAM resources have been deleted after testing.