# FROM jenkins/jenkins:lts
# USER root
# RUN apt-get update -qq \
#     && apt-get install -qqy apt-transport-https ca-certificates curl gnupg2 software-properties-common
# RUN curl -fsSL https://download.docker.com/linux/debian/gpg | apt-key add -
# RUN add-apt-repository \
#     "deb [arch=amd64] https://download.docker.com/linux/debian \
#     $(lsb_release -cs) \
#     stable"
# RUN apt-get update  -qq \
#     && apt-get install docker-ce -y
# RUN usermod -aG docker jenkins


# FROM jenkins/jenkins:lts

# USER root

# RUN apt-get update -qq \
#     && apt-get install -qqy apt-transport-https ca-certificates curl gnupg2 software-properties-common

# RUN curl -fsSL https://get.docker.com | sh

# RUN usermod -aG docker jenkins

# USER jenkins


# Use an appropriate base image
# FROM ubuntu:20.04

# # Install necessary dependencies
# RUN apt-get update -qq \
#     && apt-get install -y apt-transport-https ca-certificates curl gnupg lsb-release

# # Add Docker’s official GPG key
# RUN curl -fsSL https://download.docker.com/linux/ubuntu/gpg | gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

# # Add the Docker APT repository
# RUN echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" > /etc/apt/sources.list.d/docker.list

# # Install Docker CE
# RUN apt-get update -qq \
#     && apt-get install -y docker-ce docker-ce-cli containerd.io

# # Add Jenkins user to the Docker group
# RUN usermod -aG docker jenkins

# # Add your application to the image
# ADD target/java-jenkins-docker.jar java-jenkins-docker.jar

# # Set the entrypoint
# ENTRYPOINT ["java", "-jar", "java-jenkins-docker.jar"]

# # Expose the application's port
# EXPOSE 8080





# FROM jenkins/jenkins:lts
# USER root

# # Install necessary dependencies
# RUN apt-get update -qq \
#     && apt-get install -qqy apt-transport-https ca-certificates curl gnupg2 software-properties-common

# # Add Docker’s official GPG key
# RUN curl -fsSL https://download.docker.com/linux/debian/gpg | apt-key add -

# # Add the Docker APT repository
# RUN add-apt-repository \
#     "deb [arch=amd64] https://download.docker.com/linux/debian \
#     $(lsb_release -cs) \
#     stable"

# # Update repositories and install Docker CE
# RUN apt-get update -qq \
#     && apt-get install -y docker-ce docker-ce-cli containerd.io

# # Add Jenkins user to the Docker group
# RUN usermod -aG docker jenkins

# # Switch back to the Jenkins user
# USER jenkins



FROM jenkins/jenkins:lts
USER root

# Install necessary dependencies
RUN apt-get update -qq \
    && apt-get install -qqy apt-transport-https ca-certificates curl gnupg2 software-properties-common

# Add Docker’s official GPG key
RUN curl -fsSL https://download.docker.com/linux/debian/gpg | gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

# Add the Docker APT repository
RUN echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/debian $(lsb_release -cs) stable" > /etc/apt/sources.list.d/docker.list

# Update repositories and install Docker CE
RUN apt-get update -qq \
    && apt-get install -y docker-ce docker-ce-cli containerd.io

# Add Jenkins user to the Docker group
RUN usermod -aG docker jenkins

# Switch back to the Jenkins user
USER jenkins



