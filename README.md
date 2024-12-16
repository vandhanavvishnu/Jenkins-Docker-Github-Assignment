This repository contains the deliverables for the assignment 'Integrating Jenkins with Github and Docker.

## Overview
This project demonstrates the integration of Jenkins, GitHub, Docker, and Docker Hub. The goal is to automate the build, test, dockerization, and deployment of a Java application Docker image to Docker Hub after every commit made to the application's repository on Github.

#### 1. Download the Demo Java Application:

- Download the Java application from this link.

#### 2. Host the Application Code on GitHub:

- Clone the repository to your local machine.

- Create a new repository on GitHub.

- Push the local repository to GitHub.

#### 3. Download the Jenkins Dockerfile from the folder 'jenkins-docker-files' and Build the Docker Image using the below command:
```
docker build -t jenkins-docker .
```
#### 4. Run the Docker Container
```
docker run -it -p 8080:8080 -p 50000:50000 -v jenkins_home:/var/jenkins_home -v /var/run/docker.sock:/var/run/docker.sock --restart unless-stopped jenkins-docker
```
#### 5.Configure JDK and Maven in Jenkins:
Find the JAVA_HOME path:
```
bash
docker exec -it <container_name_or_id> /bin/bash
echo $JAVA_HOME
```
#### 6. Configure the Jenkins job and Configure the Build Steps
#### 7. Download the Dockerfile for the Java application
#### 8. Add Docker Build and Publish Steps:
- Install docker-build-step and CloudBees Docker Build and Publish plugins.
- Add build steps to build and push Docker images to Docker Hub.
#### 9. Configure Jenkins Build Script
#### 10. Verify Build and Deployment:
- Commit changes to GitHub and ensure Jenkins automatically builds and deploys the Docker image.
