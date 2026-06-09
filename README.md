# ☁️ Highly Available 3-Tier Web Application on AWS
![AWS](https://img.shields.io/badge/AWS-Cloud-orange)
![EC2](https://img.shields.io/badge/EC2-Compute-blue)
![RDS](https://img.shields.io/badge/RDS-Database-green)
![CloudWatch](https://img.shields.io/badge/CloudWatch-Monitoring-yellow)
![SNS](https://img.shields.io/badge/SNS-Notifications-red)

## 📖 Project Overview

This project demonstrates the deployment of a highly available, scalable, and secure three-tier web application architecture on AWS.

The infrastructure is designed using AWS best practices and includes networking, compute, load balancing, database services, monitoring, notifications, and automatic scaling capabilities.

Architecture Components

**Networking**

- Amazon VPC

- Public and Private Subnets across multiple Availability Zones

- Internet Gateway

- NAT Gateway

- Route Tables

**Compute**

- EC2 Bastion Host (Jump Server)

- EC2 Application Servers

- Auto Scaling Group (ASG)

**Load Balancing**
- Application Load Balancer (ALB)

- Target Groups

- Health Checks

**Database**

- Amazon RDS MySQL

- Private Database Subnets

- DB Subnet Group

**Monitoring & Notifications**

- Amazon CloudWatch

- Amazon SNS (Simple Notification Service)

**DNS**

- Amazon Route 53

## 🏗️ Architecture Components

   Users
 
   │
   
   ▼

   Route 53

   │
   
   ▼

   Application Load Balancer

   │
   
   ▼

   
   Auto Scaling Group

   ┌───────────────┐
 
   │ EC2 Instance 1│
 
   │ EC2 Instance 2│
 
   └───────────────┘
 
   │
   
   ▼

   Amazon RDS MySQL

   ##  📸 Project Screenshots

 VPC
 
 <img width="1009" height="306" alt="image" src="https://github.com/user-attachments/assets/c72206be-2698-4c22-853f-e2f1ca9b789c" />
   

Auto Scaling Group

<img width="1920" height="1080" alt="Screenshot (70)" src="https://github.com/user-attachments/assets/12c4d1a7-accd-4047-9300-df9d2b7126e5" />

Instances

<img width="1020" height="192" alt="image" src="https://github.com/user-attachments/assets/af266626-17b5-448d-a8ce-cdebcf0c4411" />

CloudWatch Alarm

<img width="1920" height="1080" alt="Screenshot (72)" src="https://github.com/user-attachments/assets/2c8be22d-f75a-4c8d-a261-f275a17701e1" />

SNS Alert

<img width="1920" height="1080" alt="Screenshot (67)" src="https://github.com/user-attachments/assets/71860850-9cd9-4197-8534-ab4c72276d22" />


## 🚀 Features

**High Availability**

- Multi-AZ deployment

- Redundant application servers

- Load balancing across Availability Zones

**Scalability**

- Auto Scaling Group automatically adds/removes EC2 instances based on demand

- Dynamic resource allocation

**Security**

- Private subnets for application and database layers

- Bastion Host for secure SSH access

- Security Groups with least-privilege access

**Monitoring**

- CloudWatch metrics for EC2 instances

- CPU Utilization monitoring

- Health monitoring of application servers

**Notifications**

- SNS topic configured to send email alerts

- Notifications triggered by CloudWatch alarms

## 🛠️ AWS Services Used

- Service	Purpose

- VPC	Network Isolation

- EC2	Application Hosting

- ALB	Traffic Distribution

- Auto Scaling Group	Automatic Scaling

- RDS MySQL	Database Layer

- Route 53	DNS Management

- CloudWatch	Monitoring & Metrics

- SNS	Alert Notifications

- IAM	Access Management

- NAT Gateway	Internet Access for Private Subnets

## 🌐 Infrastructure Setup

- VPC Configuration

- Resource	CIDR

- VPC	20.0.0.0/20

- Public Subnet 1	20.0.1.0/24

- Public Subnet 2	20.0.2.0/24

- App Private Subnet 1	20.0.3.0/24

- App Private Subnet 2	20.0.4.0/24

- DB Private Subnet 1	20.0.5.0/24

- DB Private Subnet 2	20.0.6.0/24

**Application Deployment**

**Web Layer**

- Apache HTTP Server

- PHP 8.2

- phpMyAdmin

**Database Layer**

- Amazon RDS MySQL

- Private database access

- Secure connectivity via Security Groups

## 📈 Auto Scaling Configuration

Launch Template
Configured with:

- Amazon Linux

- Apache

- PHP

- Application dependencies

- Auto Scaling Policies

Scale Out

- Trigger: CPU Utilization > 70%

- Action: Add EC2 Instance

Scale In

- Trigger: CPU Utilization < 30%

- Action: Remove EC2 Instance

**Benefits**

- Improved application availability

- Reduced operational costs

- Automatic handling of traffic spikes

## 📊 CloudWatch Monitoring

CloudWatch monitors:

- CPU Utilization

- Network In/Out

- Status Check Failures

- Auto Scaling Activities

- Application Health

**CloudWatch Alarms**

Alarm	Condition
High CPU	CPU > 70%
Low CPU	CPU < 30%
Instance Health	Failed Status Checks

## 🔔 SNS Notifications

- Amazon SNS is integrated with CloudWatch alarms.

**Alert Scenarios**

- High CPU Utilization

- EC2 Instance Failure

- Auto Scaling Events

- Application Health Issues

**Notification Channels**

- Email Alerts

## 🔒 Security Groups

**Bastion Host Security Group**

- SSH (22) from Admin IP

**ALB Security Group**

- HTTP (80) from Internet

**Application Server Security Group**

- HTTP from ALB Security Group

- SSH from Bastion Host

**Database Security Group**

- MySQL (3306) from Application Servers

## 💡 Skills Demonstrated

- AWS VPC
- EC2
- Application Load Balancer
- Auto Scaling Group
- Amazon RDS
- Route 53
- CloudWatch
- SNS
- Linux Administration
- Apache Web Server
- Networking
- Security Groups
- High Availability Architecture

## 🎯 Key Achievements

- Designed a highly available 3-tier AWS architecture.
- Implemented Auto Scaling for dynamic workload management.
- Configured CloudWatch monitoring and SNS alerting.
- Secured infrastructure using VPC, private subnets, and Security Groups.
- Deployed application across multiple Availability Zones for fault tolerance.

## 🎯 Project Outcomes

- Built a production-style AWS architecture

- Implemented high availability across multiple Availability Zones

- Configured Auto Scaling for dynamic workload management

- Implemented monitoring using CloudWatch

- Configured SNS alerts for operational visibility

 Secured infrastructure using VPC, private subnets, and Security Groups
