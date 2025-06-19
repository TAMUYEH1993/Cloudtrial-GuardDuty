# 🛡 AWS Cloud Security Lab: CloudTrail + GuardDuty Threat Detection

## 🔍 Objective
To monitor, detect, and investigate suspicious or unauthorized activity in an AWS environment using CloudTrail and GuardDuty.

---

## 🛠 Tools Used
- AWS CloudTrail
- Amazon GuardDuty
- IAM (Identity & Access Management)
- EC2 (Simulated attack surface)
- Kali Linux (optional attacker simulation)

---

## ✅ Key Actions Performed

### 1. Enabled CloudTrail
- Created a trail named security-lab-trail
- Enabled logging for management and data events across all regions
- Configured logs to be stored in an S3 bucket

### 2. Enabled GuardDuty in All Regions
- Turned on GuardDuty threat detection globally
- Enabled auto-protection for new regions

### 3. Simulated Threats
- Created an EC2 instance with open ports (22 & 3389) to the internet
- Used Kali to simulate port scans and SSH brute-force attempts
- Generated sample GuardDuty findings

### 4. Investigated GuardDuty Findings
Example Finding:
- UnauthorizedAccess:EC2/SSHBruteForce
- Investigated source IP, impacted EC2 instance, and IAM role involved
- Verified activity using CloudTrail logs and VPC Flow Logs (if enabled)

---

## 🧠 Real-World Analysis Process

### 🛡 GuardDuty Alert Triage
- Identify and classify alert severity
- Correlate IP and resource (EC2, IAM)
- Validate threat using CloudTrail logs
- Simulate remediation: Restrict security group, terminate EC2, notify team
- Document and escalate based on risk

### 🔎 CloudTrail Log Analysis
- Queried CloudTrail for events like AuthorizeSecurityGroupIngress, RunInstances, and ConsoleLogin
- Validated who made the changes and from where
- Correlated activity with timestamps from GuardDuty alerts

---

## 📷 Screenshots
Include:
- GuardDuty findings
- CloudTrail logs
- Security group configuration
- Terminal commands (SSH or AWS CLI)

---

## 💡 Lessons Learned
- How to simulate cloud threats using open ports and access key misuse
- How AWS detects suspicious behavior using built-in services
- Importance of automation, logging, and least privilege in cloud environments

---

## 📚 Next Steps
- Add CloudWatch alarms for auto-remediation
- Send GuardDuty alerts to an external SIEM
- Integrate SNS for alert notifications

---

## 🔗 Connect
Built by Built by Bon Tamuyeh as part of a cloud security portfolio project.  
Feel free to connect on https://www.linkedin.com/in/bon-tamuyeh-b828a02ab/ or explore more projects on https://github.com/TAMUYEH1993/Cloudtrial-GuardDuty/edit/main/README.md.
