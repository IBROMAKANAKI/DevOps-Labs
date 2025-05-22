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

- Prepare to Connect from Your Local Machine

   i) Open your terminal or command prompt on your local machine.

  ii) Change directory to where your .pem key file is downloaded.

  <style>
  .zoom-gallery {
    display: flex;
    align-items: center;
    gap: 1rem;
    justify-content: center;
    flex-wrap: wrap;
  }
  .zoom-image {
    width: 300px;
    cursor: pointer;
    transition: transform 0.3s ease;
    border-radius: 12px;
    box-shadow: 0 4px 12px rgba(0,0,0,0.2);
  }
  .zoom-image:hover {
    transform: scale(1.05);
  }

  /* Lightbox effect */
  #lightbox {
    position: fixed;
    display: none;
    top: 0; left: 0;
    width: 100%; height: 100%;
    background: rgba(0,0,0,0.9);
    justify-content: center;
    align-items: center;
    z-index: 1000;
  }
  #lightbox img {
    max-width: 90%;
    max-height: 90%;
    border-radius: 10px;
  }
</style>

<div class="zoom-gallery">
  <img src="Assets/Images/Connect%20instance.jpg" alt="Connect" class="zoom-image" onclick="showLightbox(this.src)" />
  <span style="font-size: 2rem;">➡️</span>
  <img src="Assets/Images/Terminal%20connect.jpg" alt="Terminal" class="zoom-image" onclick="showLightbox(this.src)" />
</div>

<div id="lightbox" onclick="this.style.display='none'">
  <img src="" alt="Zoomed" id="zoomedImg" />
</div>

<script>
  function showLightbox(src) {
    document.getElementById('zoomedImg').src = src;
    document.getElementById('lightbox').style.display = 'flex';
  }
</script>


