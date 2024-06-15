# Devops-p_Jenkinssetup
# Demo Project
#  Build Automation & CI/CD with jenkins

# Technologies used:
Jenkins
Docker
DigitalOcean
Linux
Git
java
maven

# Project Description
Create an ubuntu server on DigitalOcean
setup and run jenkins as Docker container
initialize jenkins

## configure tools on jenkins
install node and npm directly on server

Enter jenkins docker container as root user
docker exec -u 0 -it containerID bash
install curl
apt update
apt install curl

download the nodesource script with the curl command
curl -sl https://deb.nodesource.com/setup_20.x -o nodesource_setup.sh
run the script (bash nodesource_setup.sh)

run (apt-get install nodejs -y) to install
install nodejs from the plugin to make it available

# Make docker available on jenkins server

mount docker from droplet into the jenkins container as volume
stop running containers
run
docker run -p 8080:8080 -p 50000:50000 -v jenkins_home:/var/jenkins_home 
-v /var/run/docker.sock:/var/run/docker.sock jenkins/jenkins:lts

enter the jenkins container
download docker with the curl command
(curl https://get.docker.com/ >dockerinstall && chmod 777 dockerinstall && /dockerinstall

add readwrite permission to (/var/run/docker.sock) file
chmod 666 /var/run/docker.sock






