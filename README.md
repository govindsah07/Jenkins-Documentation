# Jenkins Documentation
![documentation](https://github.com/govindsah07/Jenkins-Documentation/assets/159414736/1af93323-7846-48c9-add4-d17cdf87061d)

## Table of Contents

1. [Introduction to Jenkins](#introduction-to-jenkins)
2. [Why Use Jenkins?](#use-of-jenkins)
3. [Advantages of Jenkins](#advantages-of-jenkins)
4. [Architecture of Jenkins](#architecture-of-jenkins)
5. [Installation of Jenkins](#Installation-of-Jenkins-in-Ubuntu)
   - [Prerequisites](#Prerequisites)
   - [Steps for Installation](#steps-for-installation)
     1. [Step 1: Install Java](#step-1-install-java)
     2. [Step 2: Download Jenkins Repository Key](#step-2-download-jenkins-repository-key)
     3. [Step 3: Add Jenkins Repository to APT Sources](#step-3-add-jenkins-repository-to-apt-sources)
    
6. [How to Set up a Build Job](#How-to-Set-up-a-Build-Job)

7. [Reference Link](#reference-link)

## Introduction to Jenkins

Jenkins is an open-source automation server that makes it easy to set up continuous integration and continuous delivery (CI/CD) for your software projects. It helps automate the parts of software development related to building, testing, and deploying, so you can focus more on coding.

![jenkins11](https://github.com/user-attachments/assets/a534ec11-c5ef-4473-855a-9a9623fdc952)

## Use of Jenkins

![use of jenkins](https://github.com/user-attachments/assets/73350786-3212-488b-b5d8-0958eb8d94d4)

Jenkins is used because it helps automate and speed up the software development process.
Jenkins can automatically build, test, and deploy code, saving developers time and effort.
Continuous Integration (CI): It helps developers quickly and frequently merge and test code changes.
Continuous Delivery (CD): Jenkins can deploy code to production quickly and without manual interference.
This makes the development process smoother, faster, and more reliable.

## Advantages of Jenkins

![advantage of jenkkins](https://github.com/user-attachments/assets/3f9cb348-87b7-4722-847e-5d8fd9b333f1)

**Open-source and Free:** Jenkins is free to use and open-source.

**Easily Configurable:** It quickly deploys code and generates test reports. You can set it up for continuous integration and continuous delivery as needed.

**Works on All Platforms:** Jenkins runs on any operating system, like OS, Windows, or Linux.

**Lots of Plugins:** There are many plugins available for Jenkins, making it flexible and useful for different tasks.

**Strong Community Support:** Since Jenkins is widely used and strong support from large online communities.

**Error Detection:** Developers can quickly find and fix errors in their code, avoiding large-scale problems.

**Automation:** Tasks are automated, reducing problems and saving time and money during a project.

## Architecture of Jenkins

![jenkins-pipline](https://github.com/user-attachments/assets/6c2d9748-1c1d-4e2d-b575-178ab39d6e38)

**Commit:**

Developer Action: A developer writes code and commits it to a version control system Git.
Jenkins Action: Jenkins is configured to monitor the version control system for changes.

**Build:**

Developer Action: Once the code is committed, Jenkins automatically detects the change.
Jenkins Action: Jenkins pulls the latest code and starts the build process.

**Test:**

Developer Action: Developers write tests to check if the code works as expected.
Jenkins Action: Jenkins runs these tests automatically after the build. If the tests pass, it means the code is working correctly. If they fail, Jenkins notifies the developers.

**Stage:**

Developer Action: Developers don't need to do anything directly during this stage. They set up the staging process when they first configure Jenkins.
Jenkins Action: Jenkins takes the code that has passed all the tests. It takes this code to a staging environment, which is essentially a test version of the real environment in which the code will be used. Before releasing the code to users, ensure that everything works perfectly.

**Deploy:**

Developer Action: Developers or operations teams might trigger the deployment or Jenkins can do it automatically.
Jenkins Action: Jenkins deploys the code from the staging environment to the production environment, making it available to users.


## Installation of Jenkins in Ubuntu

### Prerequisites

Minimum hardware requirements:

- 256 MB of RAM
- 1 GB of drive space

Software requirements:

- Java 
- Web browser 

### Steps for installation of Jenkins

steps which you have fallow to install jenkins.

### Check OS Version

 ```bash
cat /etc/os-release 
```
 ![os-version](https://github.com/user-attachments/assets/f34d9873-a22c-4f00-bcac-d8cf4c8c1217)


## Step1 Install Java

```bash
sudo apt-get install openjdk-11-jdk
```
![install jdk](https://github.com/govindsah07/Jenkins-Documentation/assets/159414736/6c4409a5-0af3-4679-8d9c-4e0a8e788f82)

To check java version

```bash
java --version
```
![java -version](https://github.com/govindsah07/Jenkins-Documentation/assets/159414736/eb650d93-b62c-494e-98db-079a1dee0e47)


## Step 2 Download Jenkins Repository key:

```
sudo wget -O /usr/share/keyrings/jenkins-keyring.asc https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
```
![keyring](https://github.com/user-attachments/assets/048a2645-104e-466b-b3cd-2ffd63630a00)

## Step 3 Add Jenkins Repository to APT Sources

```bash
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
https://pkg.jenkins.io/debian binary/ | sudo tee \
/etc/apt/sources.list.d/jenkins.list > /dev/null
```
![keyrings1](https://github.com/user-attachments/assets/9160bf32-2984-4d32-afed-04de2e911212)

## Step4 Update System

```bash
sudo apt-get update
```
![sudoapt-get update](https://github.com/govindsah07/Jenkins-Documentation/assets/159414736/1374f202-d032-4a68-950c-47169bd08f6f)

## Step5 Install Jenkins

```
sudo apt-get install jenkins -y
```
![1111](https://github.com/user-attachments/assets/7e7db506-ab60-4dd8-81c6-8e2712e3f6e4)

### check Jenkins which jenkins

```bash
which jenkins
```
![1111 which](https://github.com/user-attachments/assets/14fb4fd9-c224-4ced-9bb6-3fa7f6b60eef)

## Step 6 Jenkins Status

```bash
systemctl status jenkins
```

![systemctl status jenkins2](https://github.com/govindsah07/Jenkins-Documentation/assets/159414736/e183ed5e-7f6f-4948-96e3-61e60b9b1ffa)

## Open Browser 
To access a web application running on port 8080 Url http://localhost:8080/ and create username and passwords.

![jenkinsdashboard](https://github.com/govindsah07/Jenkins-Documentation/assets/159414736/88d2bcb2-0662-4854-86c7-ce7686da0562)

## How to Set up a Build Job

![Jenkins-Demo-Job-Ubuntu-22-04](https://github.com/govindsah07/Jenkins-Documentation/assets/159414736/7e401347-bc4a-4842-8e6b-44267a993d5d)


## Reference link
https://www.jenkins.io/doc/
