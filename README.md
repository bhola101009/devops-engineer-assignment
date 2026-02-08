# DevOps Engineer – AWS Technical Assignment

## Objective
Deploy a simple "Hello World" web application on AWS demonstrating
cloud infrastructure, networking, and basic DevOps practices.

---

## Architecture Overview
The application is deployed in a custom VPC with public and private subnets
across two Availability Zones.

- Public subnets host the Application Load Balancer and NAT Gateway
- Private subnets host EC2 instances running Nginx
- The ALB routes HTTP traffic to EC2 instances
- NAT Gateway provides outbound internet access for private instances

Refer to the architecture diagram in the `architecture/` folder.

---

## Application URL
http://devops-alb-706137901.ap-south-1.elb.amazonaws.com

---

## AWS Services Used
- Amazon VPC
- EC2
- Application Load Balancer
- Target Groups
- Security Groups
- NAT Gateway
- Elastic IP
- Internet Gateway

---

## Security Configuration
- ALB Security Group allows HTTP (80) from the internet
- EC2 Security Group allows HTTP (80) only from ALB Security Group
- No direct internet access to EC2 instances

---

## Verification
- Application is accessible via ALB DNS
- Page displays instance ID and availability zone
- Refresh confirms load balancing between instances

---

## Repository Structure
- `architecture/` – Architecture diagram
- `config/` – Nginx and HTML configuration
- `user-data/` – EC2 initialization script
- `screenshots/` – Deployment and verification screenshots

