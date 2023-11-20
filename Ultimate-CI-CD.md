The code would be placed in Github.
We can create a webook on Github and add Jenkins URL on Github, Also Install Github Plugin on Jenkins, so whenever we commit any changes on Git Repo, Automatically Jenkins pipeline would be trigerred.

![image](https://github.com/jalaluddinmohammed/DevOpsProjects/assets/145260536/f905cc6a-c51a-4fd6-987d-275279737282)

Created Azure VM.
Install Jenkins, Docker, Sonarqube on it.
Maven installation is not needed as we are using maven docker image to build the code.
Ensure NSG's are not blocking it, locally also its accessible ( sonarqube and Jenkins URL)
Install necessary plugins on Jenkins.
configure authenticaton of docker,sonarqube on jenkins.
Create a pipeline on Jenkins, Jenkinsfile can be on any location on github and it can have any name, its not mandatory to have file name liek Jenkinsfile !!
While troubleshooting Jenkins and Sonarqube ensure you are restarting/starting these services with Jenkins/Sonarqube user id.
After a VM reboot, Sonarqube has to be started ./sonar start (otherwise sonarqube wont run).
Spent many hours fixing minikube, but didnt work.
Explored AKS option and found very easy and helpful.
https://learn.microsoft.com/en-us/azure/aks/learn/quick-kubernetes-deploy-portal?tabs=azure-cli
Deploy AKS using step by step above.
Setup LB service for argo cd server so that you can login to it on browser.
Install Argo CD operator lifecycle software.
deploy argo cd controller.
Add AKS cluster on argo cd ( you need to download argo cd software, setup env path)
After that login to argocd server using CLI and then add aks cluster on it.
Now whenever a git push happens, jenkins pipeline will trigger, build will happen, testing will be done, image would be created and pushed to github.
Argo cd will take the manifest from github and push it on AKS pods, a roll out will happen and all pods would be updated with latest changes.

