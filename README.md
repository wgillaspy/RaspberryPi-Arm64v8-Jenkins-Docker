# RaspberryPi-Arm64v8-Jenkins-Docker

## This is a Jenkins Docker image that will run on a Raspberry Pi running the Ubuntu 64bit arm distribution.
#### The image is based on the official Jenkins Docker project:  https://github.com/jenkinsci/docker

Please use at your own risk.  At minimum, I'd suggest comparing this project and the official project to understand the differences.

Example build command:  
- docker build . -t arm/jenkins:latest  

Example run command:  
- docker run -d  -p 8080:8080 --mount type=bind,source=/mnt/fileshare/jenkins,target=/var/jenkins_home arm/jenkins:latest
