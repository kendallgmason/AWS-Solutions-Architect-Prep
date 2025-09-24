# AWS Solutions Architect Associate Labs

This repository documents my hands-on practice while preparing for the **AWS Solutions Architect Associate (SAA-C03)** certification using Stéphane Maarek’s course.

Each section contains:
- 📝 My own notes & explanations
- 📸 Screenshots of AWS Console/CLI
- 💻 Commands & configs (where relevant)

## Sections Completed
- [x] IAM & AWS Fundamentals
- [ ] EC2 Deep Dive (in progress)
- [ ] Elastic Load Balancing & Auto Scaling
- [ ] S3 & CloudFront
- [ ] RDS, DynamoDB, Aurora
- [ ] VPC & Networking
- [ ] Security & Monitoring
- [ ] Architecture & Exam Prep

---

# AWS Free Tier & Cost Awareness

While working through these AWS SAA labs, I’ve ensured all resources stay within the Free Tier to avoid unnecessary costs.  

## Budget Setup
- AWS Budget: $0.01 monthly
- Notifications sent to my email/SNS to alert on any usage beyond Free Tier

## Free Tier Practices
- EC2: Only t2.micro or t3.micro instances
- S3: Max 5GB standard storage
- RDS: Free Tier databases (MySQL/PostgreSQL)
- Lambda: <= 1M requests/month
- CloudFront: <= 50GB/month
- Always terminate/delete resources immediately after use

## Screenshot of Budget Setup
![Budget Setup in AWS](Budget Setup.png)



# Section 4 – IAM (Identity & Access Management)

## What I learned
- IAM allows you to **control access** to AWS resources.
- Users, Groups, Roles, and Policies are the building blocks.
- AWS best practice: **Least privilege principle** — only give permissions needed.
- IAM roles can be assigned to EC2 instances or Lambda for temporary access.

## What I did
1. Created an IAM user for lab purposes.
2. Attached a policy (`AmazonS3ReadOnlyAccess`) to limit permissions.
3. Created an IAM group and added the user to it.
4. Created an IAM role and attached it to an EC2 instance.
5. Experimented with logging in as the IAM user and verifying permissions.

## Screenshots
![Create IAM User](screenshots/create-user.png)
![Attach Policy](screenshots/attach-policy.png)

# Section 5 – EC2 Fundamentals
📌 **What I learned:**  
- EC2 = Elastic Compute Cloud → virtual servers on demand.  
- Pricing models: On-Demand, Reserved, Spot, Dedicated.  
- Security groups act like virtual firewalls.  

🛠 **What I did:**  
1. Launched a t2.micro EC2 instance in the AWS Free Tier.  
2. Connected via SSH.  
3. Terminated the instance safely.  

📸 **Screenshots:**  
![EC2 Launch](section-05-ec2/screenshots/launch-ec2.png)  
![EC2 Terminate](section-05-ec2/screenshots/terminate-ec2.png)

