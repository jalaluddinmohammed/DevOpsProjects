![image](https://github.com/jalaluddinmohammed/DevOpsProjects/assets/145260536/294aa6d1-ed9f-4ecc-8667-b23b87221f1e)








Project Overview
Description
This project involves setting up a CI/CD pipeline to automate the deployment process. The pipeline includes pushing code to GitHub, pulling the code using Jenkins, performing static code analysis with SonarQube, and deploying the code using Docker. The entire process will be orchestrated on EC2 instances, requiring three instances for Jenkins, SonarQube, and Docker deployment.

Steps
1. GitHub Repository Setup
Create a new repository on GitHub named "Jenkins-SonarQube-Docker."
Upload the code to the repository, or you can use a template from a free CSS website.
2. CI/CD Pipeline Overview
GitHub: Code will be pushed to GitHub repository.

Jenkins:

Jenkins will pull the code from the GitHub repository.
A freestyle project will be used in Jenkins for automation.
SonarQube:

Jenkins will trigger SonarQube for static code analysis.
Identify and fix bugs and vulnerabilities using SonarQube.
Define rules and quality standards for scanning.
Docker Deployment:

If the code passes the SonarQube analysis, it will be deployed on Docker.
EC2 instances will be used for Jenkins, SonarQube, and Docker.
EC2 Instances:

Set up three EC2 instances: one for Jenkins, one for SonarQube, and one for Docker deployment.
3. HTML Template
A basic HTML template will be used for the website. You can download templates from free CSS websites.
4. Project Execution
Clone Repository:

Clone the GitHub repository to your local machine.
EC2 Instances:

Create three EC2 instances for Jenkins, SonarQube, and Docker deployment.
Pipeline Execution:

Push code to GitHub.
Jenkins pulls code, triggers SonarQube analysis, and deploys on Docker.
Verify Deployment:

Access the deployed website on your browser to verify functionality.
