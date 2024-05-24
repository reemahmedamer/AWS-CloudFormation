# AWS-CloudFormation
## Overview
This CloudFormation template sets up a web infrastructure with a VPC, subnets, internet connectivity, security groups, an Auto Scaling group of EC2 instances, and an Application Load Balancer (ALB).

## Resources Created
**1) VPC and Subnets** 

- VPC with CIDR block 10.0.0.0/16
- 2 Public subnets (one in each AZ)
- 2 Private subnets (one in each AZ)

**2) Internet Connectivity**

- Internet Gateway  
- 2 NAT Gateways  

**3) Routing** 

- Public and private route tables with routes
   
**4) Security Group**

- Allows inbound HTTP (port 80) traffic
  
**5) Compute Resources**

- Launch Template with AWS Linux AMI, t2.micro instances, Apache installation script
- Auto Scaling Group with 2 instances across private subnets
  
**6) Load Balancing**

- Application Load Balancer (ALB) in public subnets
