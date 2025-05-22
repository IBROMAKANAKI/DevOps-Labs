# Lab Exercise # 2 - CICD setup - Install Jenkins in One instance and Tomcat on second EC2 instance in AWS Cloud

Jenkins is an open source continuous integration/continuous delivery and deployment (CI/CD) automation software DevOps tool written in the Java programming language. It is used to implement CI/CD workflows, called pipelines
 
**follow the steps to install Java, Jenkins, Maven on Ubuntu 22.0.4 instance. Jenkins, Maven are Java based applications, so we need to install Java first.**

# Steps

## 1. 🔗 Connect to the Jenkins Instance from a Local Machine After Creating an EC2 Instance on AWS

- Open the AWS Console
   i) Navigate to **https://console.aws.amazon.com**.

   ii) Sign in to your AWS account.

- Locate Your **Jenkins EC2 Instance**

    i) From the AWS Console, go to the EC2 Dashboard.

    II) Click on Instances in the left-hand menu.

    iii) Find and select your Jenkins EC2 instance from the list.

  ![Connect to Jenkins](Assets/Images/Connect to EC2.jpg)

- Click "Connect"

    i) With your Jenkins instance selected, click the “Connect” button at the top of the page.

- Choose "SSH Client" Option

    i) Under the "Connect to instance" page, select the SSH Client tab.

    ii) You will see an example SSH command provided by AWS (e.g., ssh -i "your-key.pem" ubuntu@ec2-XX-XX-XX-XX.compute-1.amazonaws.com).

 | Connect to Instance | ➡️ | Terminal Connected |
|---------------------|----|--------------------|
| ![Connect](Assets/Images/Connect%20instance.jpg) |  | ![Terminal](Assets/Images/Terminal%20connect.jpg) |

- Prepare to Connect from Your Local Machine

   i) Open your terminal or command prompt on your local machine.

  ii) Change directory to where your .pem key file is downloaded.


