# DevOps Lab 1 : Provision Ubuntu 22.0.4 EC2 Instance | How to create EC2 instance in AWS console | Launch Ubuntu 22.0.4 instance in AWS

## Introduction4

Welcome to my first lab exercise! In this project, I'm creating a basic infrastructure on AWS by provisioning two EC2 instances. These virtual machines will be used to install and configure Jenkins and Apache Tomcat.

This setup is the foundation for future DevOps practices, including continuous integration and continuous deployment (CI/CD).

## What is EC2 instance? 

It is virtual server provided by AWS. I will be using this EC2 to setup both Jenkins and Tomcat. Please follow the below steps to create an EC2 instance.

## Prerequisites

Before you begin, ensure the following:

- You have an [AWS account](https://aws.amazon.com/).

## Steps

1. To launch an EC2 instance, log in to the AWS Management Console and click on **“Launch Instance”** under the EC2 dashboard.

<div style="display: flex; gap: 10px; align-items: flex-start;">
  <div style="text-align: center;">
    <img src="Asset/Images/ec2 search.jpg" alt="Search EC2" width="400"/>
    <p>⬅️ Step 2: Search for EC2</p>
  </div>
  <div style="text-align: center;">
    <img src="Asset/Images/Launch.jpg" alt="Launch EC2" width="400"/>
    <p>⬅️ Step 3: Click “Launch Instance”</p>
  </div>
</div>

<br>

![AWS page for instance launch](Asset/Images/Lab pic 1-launch instant.jpg)

2.  **Enter Name as EC2** and enter 2 as number of instances (one for Jenkins and another for Tomcat)

3. Select **Ubuntu**

4. Choose **Ubuntu server 22.0.4** as AMI

5. Enter **t2.small** as instance type

6. Click on **Create new Key Pair**

7. Choose the existing key pair if you have one, otherwise create new one, give some name as myJenkinsKey. Make sure you download the key in your local machine. Please do NOT give space or any character while naming the key.

8. Under Network settings, **Click Edit**

- Add port range as **8080** and select **AnyWhere** as Source Type, that should enter **0.0.0.0/0** as Source
  
9. Enter **10 GB** as storage
    
10. And then make sure in Summary, values appear as below:
  
11. Click on Launch Instance.

- Click on **View instances**

  




