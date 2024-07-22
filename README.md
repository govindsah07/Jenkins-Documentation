# Jenkins Documentation

![documentation](https://github.com/govindsah07/Jenkins-Documentation/assets/159414736/1af93323-7846-48c9-add4-d17cdf87061d)

## Table of Contents

1. [Introduction to Jenkins](#introduction-to-jenkins)
2. [Use of Jenkins](#use-of-jenkins)
3. [Advantages of Jenkins](#advantages-of-jenkins)
4. [Architecture of Jenkins](#architecture-of-jenkins)
5. [Installation of Jenkins](#Installation-of-Jenkins-in-Ubuntu)
6. [How to Set up a Build Job](#How-to-Set-up-a-Build-Job)
7. [Reference Link](#reference-link)

## Introduction to Jenkins

![jenkins11](https://github.com/user-attachments/assets/a534ec11-c5ef-4473-855a-9a9623fdc952)

Jenkins is an open-source automation server that makes it easy to set up continuous integration and continuous delivery (CI/CD) for your software projects. It helps automate the parts of software development related to building, testing, and deploying, so you can focus more on coding.

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

**Developer Action:** A developer writes code and commits it to a version control system Git.

**Jenkins Action:** Jenkins is configured to monitor the version control system for changes.

**Build:**

**Developer Action:** Once the code is committed, Jenkins automatically detects the change.

**Jenkins Action:** Jenkins pulls the latest code and starts the build process.

**Test:**

**Developer Action:** Developers write tests to check if the code works as expected.

**Jenkins Action:** Jenkins runs these tests automatically after the build. If the tests pass, it means the code is working correctly. If they fail, Jenkins notifies the developers.

**Stage:**

**Developer Action:** Developers don't need to do anything directly during this stage. They set up the staging process when they first configure Jenkins.

**Jenkins Action:** Jenkins takes the code that has passed all the tests. It takes this code to a staging environment, which is essentially a test version of the real environment in which the code will be used. Before releasing the code to users, ensure that everything works perfectly.

**Deploy:**

**Developer Action:** Developers or operations teams might trigger the deployment or Jenkins can do it automatically.

**Jenkins Action:** Jenkins deploys the code from the staging environment to the production environment, making it available to users.

## Installation of Jenkins in Ubuntu

### Hardware Requirements

**RAM:**

Minimum: 1 GB.

Recommended: 4 GB for larger project.

**Drive Space:**

Minimum: 1 GB.

Recommended: 50 GB for large projects.

### Software Requirements

**Operating System:**

Ubuntu 20.04.6 LTS (Focal Fossa)

**Java:**

Minimum: Java 11

Recommended: Java 11 or new OpenJDK 17.

**Web Browser:**

Latest web browser of Google Chrome: Version 126.0.6478.126

### Update the System

```bash
sudo apt update
```

![sudo apt update](https://github.com/user-attachments/assets/4c47134e-7f6e-40e3-87aa-b30cd20c74e2)

```bash
sudo apt upgrade -y
```

![sudo apt upgrade -y](https://github.com/user-attachments/assets/89f3503b-db43-4b53-b197-1bade3662044)

### Installation of Jenkins

```bash
sudo apt install openjdk-11-jdk -y
```

![sudo apt install openjdk-11-jdk -y](https://github.com/user-attachments/assets/62edd98f-782a-4210-b7a9-5d91bd7e2f8b)

To check java version

```bash
java -version
```

![java -version](https://github.com/user-attachments/assets/94ef1432-b1dd-4a21-b3ac-b1326b5163a5)

## Download Jenkins Repository key:

```bash
sudo wget -O /usr/share/keyrings/jenkins-keyring.asc https://pkg.jenkins.io/debian/jenkins.io-2023.key
```

![jenkins-keyring](https://github.com/user-attachments/assets/f6772e0f-2277-4b30-9986-5ce64caee0a0)

## To ensure that the repository has been added correctly:

```bash
cat /etc/apt/sources.list.d/jenkins.list
```

**output:**

deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] https://pkg.jenkins.io/debian binary/

![cat keyring](https://github.com/user-attachments/assets/cf6d4822-2a54-4b46-ae8f-bc71a47b019c)

## Step4 Update System

```bash
sudo apt-get update
```

![sudo apt-get update2](https://github.com/user-attachments/assets/5e256214-d000-4d63-b256-57f1022ae06a)

## Install Jenkins

```
sudo apt-get install jenkins -y
```

![sudo apt-get install jenkins -y](https://github.com/user-attachments/assets/220e42b5-215f-492f-9133-27645a835422)

### Start Jenkins Service

```bash
sudo systemctl start jenkins
```

![sudo systemctl start jenkins](https://github.com/user-attachments/assets/a68a200d-44a9-4279-a2de-911334657c4c)

### Enable Jenkins to Start

```bash
sudo systemctl enable jenkins
```

![sudo systemctl enable jenkins](https://github.com/user-attachments/assets/cbc2168e-ef93-44d5-8f31-522d11423cf4)

## Check Jenkins Status

```bash
sudo systemctl status jenkins
```

![sudo systemctl status jenkins](https://github.com/user-attachments/assets/8b34341c-271b-46ff-8a20-eb24cf2316d6)

## Open Chrome Browser

Paste Url

```bash
http://localhost:8080/
```

![login](https://github.com/user-attachments/assets/2517c7fe-429d-4856-80d0-29ae628a1c6a)

## Get Admin Password

```bash
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```

![keeeeey](https://github.com/user-attachments/assets/5f3f7a07-a5ce-4a3e-a282-0ecab18a3461)

### Install suggested plugins

![install plugins](https://github.com/user-attachments/assets/1954af47-bbf7-4cc9-be53-f2c3375b2487)

![getting start](https://github.com/user-attachments/assets/183184a7-3cdf-4680-a43a-7361f55f4286)

### Create Admin User

![adminuser](https://github.com/user-attachments/assets/5967205e-e9ba-48da-aa08-4489a388b702)

### Instance Configuration

![localhost8080](https://github.com/user-attachments/assets/585e0a36-1cbd-4e2d-8a82-bcde46d88486)

### Jenkins is ready!

![ready-jenkins](https://github.com/user-attachments/assets/1a5936a6-7f87-4e75-9a49-4e1490c697ca)

### Jenkins Dashboard

![dashboardjenkins](https://github.com/user-attachments/assets/25d5b4cb-1c4d-431a-af49-c663b96ebcb6)

## How to Set up a Build Job

![1](https://github.com/user-attachments/assets/ecd4f11c-7bcb-408e-bf67-991e240cf7b5)

### Create a new job

![2](https://github.com/user-attachments/assets/aaa83297-dec7-464e-9a9a-0eeb0a139e2c)

### Add description about job

![3](https://github.com/user-attachments/assets/47a019a3-9f4b-4328-9c68-51249c161a0f)

### Build Steps

![4](https://github.com/user-attachments/assets/7397113f-2838-4fc8-8546-405dde35e269)

### Run the Job

![5](https://github.com/user-attachments/assets/c2a84512-e2aa-450f-bbb6-72e34269b363)

### Check Status

![6](https://github.com/user-attachments/assets/09fe0148-8ec7-4bb0-a1ab-46118aac70cf)

## Reference link

https://www.jenkins.io/doc/
https://www.geeksforgeeks.org/jenkins-tutorial/?ref=header_search
