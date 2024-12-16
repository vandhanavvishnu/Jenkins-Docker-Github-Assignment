This repository contains the deliverables for the assignment 'Integrating Jenkins with Github and Docker.

## Overview
This project demonstrates the integration of Jenkins, GitHub, Docker, and Docker Hub. The goal is to automate the build, test, dockerization, and deployment of a Java application Docker image to Docker Hub after every commit made to the application's repository on Github.

#### 1. Download the Demo Java Application:

- Download the Java application from this link.

#### 2. Host the Application Code on GitHub:

- Clone the repository to your local machine.

- Create a new repository on GitHub.

- Push the local repository to GitHub.

#### 3. Download the Jenkins Dockerfile from the folder 'jenkins-dockerfile' and Build the Docker Image using the below command:
```
docker build -t jenkins-docker .
```

