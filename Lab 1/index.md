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

2.  **Enter Name as EC2 Instance** and enter 2 as number of instances (one for Jenkins and another for Tomcat)

<div style="display: flex; gap: 10px; align-items: flex-start;">
  <div style="text-align: center;">
    <img src="Asset/Images/name tag.jpg" alt="Write instance name - EC2 Instance" width="400"/>
    <p>⬅️ Step 2: Write instance name - EC2 Instance</p>
  </div>
  <div style="text-align: center;">
    <img src="Asset/Images/Ec2 setup 1.jpg" alt="Setup EC2" width="400"/>
    <p>⬅️ Step 3: Click “Setup EC2”</p>
  </div>
</div>

3. Select **Ubuntu**

![Selecting Ubuntu server](Asset/Images/select Ubuntu.jpg)

4. Choose **Ubuntu server 22.0.4** as AMI

![Using Ubuntu server 22.0.4](Asset/Images/Ubuntu 22.04 Server.jpg)

5. Enter **t2.small** as instance type

![Using t2.micro](Asset/Images/t2 micro.jpg)

6. Click on **Create new Key Pair**

<div style="display: flex; gap: 10px; align-items: flex-start;">
  <div style="text-align: center;">
    <img src="Asset/Images/set up 2.jpg" alt="Create a new key" width="400"/>
    <p>⬅️ Step 2: Create a new key</p>
  </div>
  <div style="text-align: center;">
    <img src="Asset/Images/Create Key pairs.jpg" alt="Name key and create" width="400"/>
    <p>⬅️ Step 3: Click “create”</p>
  </div>
  <div style="text-align: center;">
    <img src="Asset/Images/set up key.jpg" alt="Key pair login" width="400"/>
    <p>⬅️ Step 4: Key pair login</p>
  </div>
</div>


7. Choose the existing key pair if you have one, otherwise create new one, give some name as myJenkinsKey. Make sure you download the key in your local machine. Please do NOT give space or any character while naming the key.

![Choose the key pair](Asset/Images/Chose key pair.jpg)

8. Under Network settings, **Click Edit**

<div style="display: flex; gap: 10px; align-items: flex-start;">
  <div style="text-align: center;">
    <img src="Asset/Images/edit network setting.jpg" alt="edit network setting" width="400"/>
    <p>⬅️ Step 2: Click “Edit”</p>
  </div>
  <div style="text-align: center;">
    <img src="Asset/Images/Full network settings.jpg" alt="network settings" width="400"/>
    <p>⬅️ Step 3: network settings</p>
  </div>
</div>

- Add port range as **8080** and select **AnyWhere** as Source Type, that should enter **0.0.0.0/0** as Source

<div style="display: flex; gap: 10px; align-items: flex-start;">
  <div style="text-align: center;">
    <img src="Asset/Images/Add security group.jpg" alt="Add security group" width="400"/>
    <p>⬅️ Step 2: Add security group</p>
  </div>
  <div style="text-align: center;">
    <img src="Asset/Images/Edit network.jpg" alt="Edit new security group" width="400"/>
    <p>⬅️ Step 3: network settings</p>
  </div>
</div>
 
9. Enter **10 GB** as storage

![Configure storage](Asset/Images/configure storage.jpg)
    
11. And then make sure in Summary, values appear as below:

<div style="display: flex; gap: 10px; align-items: flex-start;">
  <div style="text-align: center;">
    <img src="Asset/Images/Summary 1.jpg" alt="Summary with one EC2 instance" width="400"/>
    <p>⬅️ Step 2: Summary with one EC2 instance</p>
  </div>
  <div style="text-align: center;">
    <img src="Asset/Images/Increase Instance in summary.jpg" alt="Summary with two EC2 instance" width="400"/>
    <p>⬅️ Step 3: Summary with two EC2 instance</p>
  </div>
</div>
  
12. Click on Launch Instance.

<div style="text-align: center;">
  <img src="Asset/Images/click launch instance.jpg" alt="Click launch instance" width="400"/>
  <p>⬅️ Step 3: Click <strong style="color: green;">“Launch Instance”</strong></p>
</div>


- Click on **View instances**

<p>Click Image to view more images</p>

<style>
  .zoom-on-hover {
    cursor: pointer;
    transition: transform 0.4s ease;
  }

  .zoom-on-hover:hover {
    transform: scale(1.2);
    z-index: 5;
  }

  .step {
    text-align: center;
  }
</style>

<div class="container" style="display: flex; gap: 10px; align-items: flex-start;">
  <div class="step visible" id="step1">
    <img
      src="Asset/Images/setting up.jpg"
      alt="Setting Up"
      width="400"
      class="zoom-on-hover"
      onclick="rotateAndShow('step2', this)"
    />
    <p>⬅️ Step 2: Setting Up</p>
  </div>

  <div class="step" id="step2" style="display: none;">
    <img
      src="Asset/Images/Lunch success.jpg"
      alt="Successful Confirmation launch"
      width="400"
      class="zoom-on-hover"
      onclick="rotateAndShow('step3', this)"
    />
    <p>⬅️ Step 3: Successful Confirmation launch</p>
  </div>

  <div class="step" id="step3" style="display: none;">
    <img
      src="Asset/Images/Instance working.jpg"
      alt="View Instance"
      width="400"
      class="zoom-on-hover"
    />
    <p>⬅️ Step 4: View Instance</p>
  </div>
</div>

<!-- Notification placeholder -->
<p id="notify" style="font-weight: bold; color: green; margin-top: 20px;"></p>

<script>
  function rotateAndShow(nextId, currentImg) {
    // Add temporary rotation
    currentImg.style.transform = "rotateY(180deg) scale(1.2)";

    setTimeout(() => {
      const nextStep = document.getElementById(nextId);
      if (nextStep) {
        nextStep.style.display = "block";
      }

      // Reset transform to allow repeated animations
      currentImg.style.transform = "none";

      if (nextId === 'step3') {
        document.getElementById('notify').innerText = "✅ Click 'View Instances' to continue";
      }
    }, 600);
  }
</script>


13 🔧 Renaming the EC2 Instance to **Jenkins** or **Tomcat**

### Steps:

- Hover your mouse over the **EC2 instance name** in the **Instances** list.
- A small **pencil icon** (✏️) will appear next to the name.
- Click the **pencil icon**.
- Type the new name, such as **Jenkins** or **Tomcat**.
- Press **Enter** or click **Save** to confirm the change.


<style> .zoom-container { display: flex; gap: 10px; align-items: flex-start; } .zoom-image { transition: transform 0.3s ease; cursor: zoom-in; } .zoom-image:hover { transform: scale(1.5); z-index: 10; } </style> <div class="zoom-container"> <div style="text-align: center;"> <img class="zoom-image" src="Asset/Images/Edit name.jpg" alt="Edit name" width="400"/> <p>⬅️ Step 2: Edit name</p> </div> <div style="text-align: center;"> <img class="zoom-image" src="Asset/Images/Changed name.jpg" alt="Changed name" width="400"/> <p>⬅️ Step 3: Changed name</p> </div> </div>



  




