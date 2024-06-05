# Jenkins Documentation

## Table of Contents

1. [Introduction to Jenkins](#introduction-to-jenkins)
2. [Workflow of Jenkins](#workflow-of-jenkins)
3. [Why Use Jenkins?](#why-use-jenkins)

4. [Advantages of Jenkins](#advantages-of-jenkins)
5. [Architecture of Jenkins](#architecture-of-jenkins)
6. [Installation of Jenkins](#installation-of-jenkins)
   - [Prerequisites](#prerequisites)
   - [Steps for Installation](#steps-for-installation)
     1. [Step 1: Install Java](#step-1-install-java)
     2. [Step 2: Download Jenkins Repository Key](#step-2-download-jenkins-repository-key)
     3. [Step 3: Add Jenkins Repository to APT Sources](#step-3-add-jenkins-repository-to-apt-sources)
7. [Reference Link](#reference-link)

## Introduction to Jenkins

Jenkins is an open-source automation server that makes it easy to set up continuous integration and continuous delivery (CI/CD) for your software projects. It helps automate the parts of software development related to building, testing, and deploying, so you can focus more on coding.

![jenkinshome](https://github.com/govindsah07/Jenkins-Documentation/assets/159414736/9ff9a96d-9ffd-48f1-9794-f4ec0a65ffa3)

## Workflow of Jenkins

The typical workflow of Jenkins involves these steps:

- **Source Code Management (SCM):**

It all starts with your code! Jenkins fetches your project's code from a version control system like Git, Subversion, or CVS.

- **Build Triggers:**

These are the events that kick off a Jenkins job. Triggers can be:
Manual: You initiate the job yourself by clicking a button.
Scheduled: The job runs at predetermined times (e.g., nightly builds).
SCM Changes: Whenever there's a change to your code (e.g., a push to a Git repository).
Other Events: External events from other tools can also trigger jobs.

- **Job Stages (Pipeline):**

A Jenkins job can be broken down into multiple stages, each representing a step in the development process. Common stages include:
Checkout: Get the latest code from SCM.
Build: Compile, assemble, or package your code.
Test: Run automated tests to ensure code quality.
Deploy: Push your code to production servers or other environments.
Post-build Actions: Perform additional tasks after the build, such as sending notifications or archiving artifacts.

- **Pipeline Definition (Jenkinsfile):**

Jenkins workflows are typically defined in a text file called a Jenkinsfile. This file resides in your project's source code repository, making it version controlled alongside your code. It specifies the stages, steps (commands executed in a stage), and overall flow of your job.

- **Pipeline Execution:**

Once triggered, Jenkins executes the stages defined in the Jenkinsfile. These stages can be sequential (one after another) or parallel (running simultaneously for efficiency).

- **Reporting and Feedback:**

After running the job, Jenkins provides detailed reports on its status (success, failure, or ongoing). You can also configure Jenkins to send notifications (e.g., emails) to keep you informed.

## Why Use Jenkins?

Here's what makes Jenkins such a valuable tool:

**Boosts Efficiency:** Automate tedious tasks like compiling code, running tests, and deploying updates. Spend less time on repetitive work and more time on innovation!

**Improved Quality:** Jenkins helps catch errors early and often through continuous integration (CI) and continuous delivery (CD) practices. By automating the build and test cycle, you can ensure your code is consistently high-quality.

**Streamlined Workflow:** Keep your development pipeline flowing smoothly with automated builds and deployments. No more manual intervention required, allowing for faster development cycles.

**Flexibility:** Jenkins is highly customizable to fit your specific needs. It supports a vast array of plugins for various tools and languages, making it adaptable to your development environment.

**Community Power:** Benefit from a large and active community that provides support, plugins, and best practices. Whether you encounter a hurdle or need guidance, a wealth of resources are available to help you on your Jenkins journey.

## Advantages of Jenkins

Jenkins stands out as a powerful tool for software development thanks to its numerous advantages. Let's explore some of the key benefits it offers:

- **Enhanced Efficiency:**

Automation Hero: Say goodbye to repetitive tasks like compiling code, running tests, and deploying updates. Jenkins automates these processes, freeing up your time for more creative and strategic development efforts.
Faster Development Cycles: With automation streamlining your workflow, you can iterate on your codebase more quickly. This translates to faster development cycles and quicker time-to-market for your applications.

- **Improved Software Quality:**

Early Error Detection: Jenkins promotes continuous integration (CI) practices. This means your code is automatically built and tested frequently, allowing you to catch bugs and errors early in the development cycle.
Consistent Quality: By automating the build and test process, Jenkins ensures your code undergoes the same rigorous testing each time. This consistency helps maintain a high standard of quality throughout your project.

- **Streamlined Development Workflow:**

Seamless Integration: Jenkins integrates seamlessly with your existing development pipeline, eliminating the need for manual intervention at each stage. This creates a smoother and more efficient development flow.
Visibility and Control: With Jenkins, you have a clear overview of your entire development process. You can monitor builds, tests, and deployments, giving you better control over your project's progress.

- **Flexibility and Customization:**

Tailored Automation: Jenkins is highly customizable to fit your specific needs. You can define custom build and test steps, triggers that initiate jobs, and the overall workflow of your project.
Plugin Power: A vast library of plugins extends Jenkins' functionality. These plugins integrate with various development tools and languages, allowing you to tailor Jenkins to your specific development environment.

- **Community Support:**

Active Community: A large and active community surrounds Jenkins. This means you have access to a wealth of resources, including:
Documentation and tutorials to help you learn and use Jenkins effectively.
Support forums where you can ask questions and get help from experienced users.
Plugins developed by the community that address specific needs and extend Jenkins' capabilities.

## Architecture of Jenkins

- **Jenkins architecture consists of:**
  Code Changes: Developers modify the source code and commit the changes to a version control system like Git.

- **Triggering the Build:** Jenkins can work in two ways:
  Push Mode: A code commit automatically triggers Jenkins to create a new build.
  Pull Mode: Jenkins periodically checks the repository for changes and initiates a build if there are any.

- **Building the Code:** The build process takes your code and transforms it into a deployable format (e.g., an executable file). If this step fails, developers are notified of any errors.

- **Automated Testing:** The built application is deployed to a testing environment where automated tests ensure everything functions correctly. Developers receive alerts if these tests fail, indicating potential regressions introduced by their changes.

- **Deployment:** If the build and tests are successful, Jenkins can optionally deploy the changes to the production environment, making the new features or bug fixes available to users.

## Installation of Jenkins in Ubuntu

### Prerequisites

Before you start, make sure you have:

- A running instance of Ubuntu.
- Sufficient system resources (CPU, RAM, Disk space).
- Root or sudo access to the system.

## Prerequisites

Minimum hardware requirements:

- 256 MB of RAM

- 1 GB of drive space (although 10 GB is a recommended minimum if running Jenkins as a Docker container)

Recommended hardware configuration for a small team:

- 4 GB+ of RAM

- 50 GB+ of drive space

Software requirements:

- Java

  ## Steps for installation of Jenkins

steps which you have fallow to install jenkins.

## Step1 Install Java

```bash
sudo apt-get install openjdk-11-jdk
```

To check java version

```bash
java --version
```

## Step 2 Download Jenkins Repository key:

```
sudo wget -O /usr/share/keyrings/jenkins-keyring.asc https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
```


![jenkinsdashboard](https://github.com/govindsah07/Jenkins-Documentation/assets/159414736/88d2bcb2-0662-4854-86c7-ce7686da0562)


### Step 3 Add Jenkins Repository to APT Sources

```
bash
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
https://pkg.jenkins.io/debian binary/ | sudo tee \
/etc/apt/sources.list.d/jenkins.list > /dev/null
```

# Step4 Update System

go to etc/apt/

```bash
sudo apt-get update
```

## Step5 Install Jenkins

```
sudo apt-get install jenkins -y
```

### check Jenkins which jenkins

```bash
which jenkins
```

## Step 6 Jenkins Status

```bash
systemctl status jenkins
```

![systemctl status jenkins](https://github.com/govindsah07/docker/assets/159414736/53b008ec-c3ad-4ba4-9e87-f362a9807eb7)

To access a web application running on your local machine on port 8080, open a web browser and enter http://localhost:8080 in the address bar, then press Enter.

Jenkins will prompt you for a username and password, which were created during the Jenkins installation. To retrieve the initial admin password

![Screenshot from 2024-03-14 00-57-21](https://github.com/ayanfosteringlinux/StuFFs/assets/153751979/f097f2a9-fc74-4d45-8c9a-a80f77a710e1)

![Screenshot from 2024-03-14 01-00-54](https://github.com/ayanfosteringlinux/StuFFs/assets/153751979/918b866d-dacf-4592-8d0c-84a1bea028b6)

![Screenshot from 2024-03-14 01-01-31](https://github.com/ayanfosteringlinux/StuFFs/assets/153751979/6b2aa3a2-3dca-4622-b8a4-d12380a08f8d)

![Screenshot from 2024-03-14 01-02-42](https://github.com/ayanfosteringlinux/StuFFs/assets/153751979/b46bf193-69ad-4c42-bccc-98347ea15eb6)


![jenkinsdashboard](https://github.com/govindsah07/Jenkins-Documentation/assets/159414736/88d2bcb2-0662-4854-86c7-ce7686da0562)


Reference link
https://www.jenkins.io/doc/
