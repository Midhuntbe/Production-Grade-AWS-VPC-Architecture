# Production-Grade-AWS-VPC-Architecture
Highly Available VPC Setup in AWS with Auto Scaling and NAT Gateway Integration

This project demonstrates how to build a **production-grade VPC** in AWS, focused on high availability, scalability, and secure networking. The architecture includes public and private subnets, NAT Gateways, Load Balancers, and Auto Scaling — all spread across **two Availability Zones** for fault tolerance.

##  Objective

To provision a secure and resilient AWS network infrastructure that can host auto-scaled application servers, with controlled internet access via NAT and traffic routing via ALB.

##  Architecture Overview

- **VPC with Public and Private Subnets** across **2 Availability Zones**
- **NAT Gateways** in each AZ for secure internet access from private subnets
- **Application Load Balancer (ALB)** in public subnets to route traffic
- **Auto Scaling Group (ASG)** managing EC2 instances in private subnets
- **EC2 Instances** only accessible via ALB, no direct internet exposure

##  Technologies Used

| Service           | Purpose                                              |
|-------------------|------------------------------------------------------|
| Amazon VPC        | Custom network with subnet isolation                 |
| Subnets           | Public (ALB/NAT) and Private (EC2) segmentation      |
| EC2               | Compute for app servers inside private subnets       |
| Auto Scaling      | Automatically launch/terminate EC2s based on demand |
| Load Balancer     | Distributes traffic across AZs securely              |
| NAT Gateway       | Allows private subnet instances to access internet  |
| Route Tables      | Controls traffic flow between subnets and gateways   |
| Security Groups   | Fine-grained traffic control                         |

# Screenshots
**VPC Architecture**

<img width="1919" height="1014" alt="Screenshot 2025-06-29 121516" src="https://github.com/user-attachments/assets/1899dfee-5c31-4d20-b6a2-882bbe06354b" />

**Autoscaling group**

<img width="1917" height="1017" alt="Screenshot 2025-06-29 121534" src="https://github.com/user-attachments/assets/a72cd038-0ba0-4f10-9862-978a61f1bb29" />

**Loadbalancer**

<img width="1913" height="1015" alt="Screenshot 2025-06-29 121550" src="https://github.com/user-attachments/assets/b73ef40e-ab59-4814-b9df-f2586718ebed" />

**Project Outcome**

<img width="1904" height="1008" alt="Screenshot 2025-06-29 120305" src="https://github.com/user-attachments/assets/6932db74-6569-49f0-b1c2-8339cd8e2819" />








