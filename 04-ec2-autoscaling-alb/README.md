# Scalable Web Application using EC2, Auto Scaling & ALB

This project demonstrates how to build a highly available and scalable web application on AWS.

---

## Step 1: Launch EC2 Instance
- Launch an Amazon Linux 2 EC2 instance
- Allow HTTP (80) and SSH (22) in the security group
- Verify access using public IP

## Step 2: Deploy Website on EC2
- Install Apache HTTP Server on the EC2 instance
- Create a simple `index.html` web page
- Start and enable the Apache service
- Verify website accessibility using the EC2 public IP

## Step 3: Create AMI
- Create a custom AMI from the configured EC2 instance
- This AMI acts as a golden image containing Apache and the deployed website
- Used by Auto Scaling Group to launch identical EC2 instances

## Step 4: Create Launch Template
- Use the custom AMI
- Configure instance type and security group

## Step 5: Create Target Group
- Configure HTTP health checks

## Step 6: Create Application Load Balancer
- Create an internet-facing ALB
- Attach target group

## Step 7: Create Auto Scaling Group
- Configure desired, min, and max capacity
- Enable CPU-based scaling

## Step 8: Attach ASG to ALB
- Attach target group to Auto Scaling Group

## Step 9: Testing & Validation
- Test website using ALB DNS
- Verify scale-out and scale-in
- Test instance replacement
