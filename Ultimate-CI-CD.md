
![image](https://github.com/jalaluddinmohammed/DevOpsProjects/assets/145260536/f905cc6a-c51a-4fd6-987d-275279737282)

# Project Documentation

## GitHub Integration and Jenkins Pipeline

1. **Code Repository on GitHub:**
   - Place the project code in a GitHub repository.

2. **GitHub Webhook Setup:**
   - Create a webhook on GitHub to trigger Jenkins builds on each commit.
   - Add Jenkins URL to the GitHub webhook settings.

3. **Jenkins GitHub Plugin:**
   - Install the GitHub plugin on Jenkins for seamless integration.

## Azure VM Setup with Jenkins, Docker, and SonarQube

4. **Azure VM Creation:**
   - Create an Azure VM for hosting Jenkins, Docker, and SonarQube.

5. **Installation of Tools:**
   - Install Jenkins, Docker, and Sonarqube on the Azure VM.

6. **Maven Docker Image Usage:**
   - Maven installation is not required; use a Maven Docker image for code builds.

7. **Network Security Group (NSG) Configuration:**
   - Ensure NSGs allow access to SonarQube and Jenkins URLs.
   - Verify local accessibility of SonarQube and Jenkins URLs.

8. **Jenkins Plugin Installation:**
   - Install necessary plugins on Jenkins for project dependencies.

9. **Authentication Configuration on Jenkins:**
   - Configure authentication for Docker and SonarQube on Jenkins.

10. **Jenkins Pipeline Setup:**
    - Create a Jenkins pipeline. The Jenkinsfile can be located anywhere on GitHub and have any name.

11. **Troubleshooting Tips:**
    - Restart/Start Jenkins and SonarQube services with Jenkins/SonarQube user ID during troubleshooting.

12. **SonarQube Startup After VM Reboot:**
    - After a VM reboot, start SonarQube using `./sonar start`.

## Kubernetes Setup with AKS and Argo CD

13. **Minikube Challenges and AKS Exploration:**
    - Investigated and spent time fixing Minikube issues without success.
    - Explored Azure Kubernetes Service (AKS) as a user-friendly alternative.

14. **AKS Deployment:**
    - Deploy AKS following the [Azure AKS documentation](https://learn.microsoft.com/en-us/azure/aks/learn/quick-kubernetes-deploy-portal?tabs=azure-cli).

15. **Load Balancer Setup for Argo CD:**
    - Configure a Load Balancer service for the Argo CD server to enable browser login.

16. **Argo CD Operator Lifecycle Software:**
    - Install Argo CD operator lifecycle software.

17. **Argo CD Controller Deployment:**
    - Deploy the Argo CD controller.

18. **Adding AKS Cluster to Argo CD:**
    - Download Argo CD software, set up environment variables, and log in to the Argo CD server using the CLI.
    - Add the AKS cluster to Argo CD.

## Continuous Integration and Deployment

19. **Jenkins Pipeline Trigger on Git Push:**
    - On every Git push, the Jenkins pipeline is triggered automatically.

20. **Automated Workflow:**
    - The automated workflow includes build, testing, image creation, and push to GitHub.

21. **Argo CD Continuous Deployment:**
    - Argo CD pulls manifests from GitHub and updates AKS pods, initiating a rollout.

---

This documentation provides a step-by-step guide for setting up the project, integrating GitHub with Jenkins, configuring Jenkins pipelines, deploying necessary services on Azure VM and AKS, and ensuring continuous integration and deployment with Argo CD. Please follow the instructions carefully for a successful project setup.
