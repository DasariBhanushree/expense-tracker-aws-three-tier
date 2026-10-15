# AWS Setup Guide — Expense Tracker

## 1. Architecture
The project uses four EC2 instances:
- Load Balancer: Nginx, public HTTP traffic on port 80.
- Frontend: Nginx, serves the web application.
- Backend: Node.js 24, API on port 8080.
- Database: MySQL 8, database port 3306.

## 2. Security Group Rules

| Server | Inbound port | Allowed source |
|---|---:|---|
| Load Balancer | 80 | Internet (0.0.0.0/0) |
| Frontend | 80 | Load Balancer security group |
| Backend | 8080 | Frontend security group |
| Database | 3306 | Backend security group |

Do not expose backend port 8080 or database port 3306 to the internet.

## 3. Before Launching
- Confirm the AWS region.
- Check the selected AMI and operating system.
- Attach an appropriate IAM role if Systems Manager access is required.
- Use private IP addresses for communication between tiers.
- Never commit passwords, tokens, or other secrets to GitHub.

## 4. Cost Safety
- Stop EC2 instances when not using them.
- Check EBS volumes and public IPv4 charges.
- Verify current AWS Free Tier or credit eligibility.
- Do not assume stopping an instance removes all charges.

## 5. Deployment Status
Documentation started. Application deployment and end-to-end testing are pending.
