# DevOps Lab: Jenkins and Tomcat Setup on AWS EC2

## Introduction

Hello DevOps Champs,

Welcome to my first lab exercise! In this project, I'm creating a basic infrastructure on AWS by provisioning two EC2 instances. These virtual machines will be used to install and configure Jenkins and Apache Tomcat.

This setup is the foundation for future DevOps practices, including continuous integration and continuous deployment (CI/CD).

## Objective

- Launch two EC2 instances in AWS.
- Set up **Jenkins** on one EC2 instance.
- Set up **Apache Tomcat** on the other EC2 instance.

## Prerequisites

Before you begin, ensure the following:

- You have an [AWS account](https://aws.amazon.com/).
- IAM user with permissions to create EC2 instances.
- AWS CLI configured on your local machine (optional, if using CLI).
- Basic understanding of Linux commands and SSH.

## Architecture

| AWS Cloud |
|
+-- EC2 Instance 1: Jenkins Server (Ubuntu)
|
+-- EC2 Instance 2: Tomcat Server (Ubuntu)


## Steps

### 1. Launch EC2 Instances

- Log in to the AWS Management Console.
- Navigate to **EC2 > Instances > Launch Instance**.
- Use Ubuntu Server 20.04 LTS for both instances.
- Choose t2.micro (or any suitable type).
- Allow the following ports in the security group:
  - **Jenkins Server**: TCP 22, 8080
  - **Tomcat Server**: TCP 22, 8080
- Launch and note the public IPs or DNS names.

### 2. Connect to EC2 Instances

Use SSH to connect to your EC2 instances:

```bash
ssh -i /path/to/your-key.pem ubuntu@<JENKINS_INSTANCE_PUBLIC_IP>

## Repeat for the Tomcat server.

