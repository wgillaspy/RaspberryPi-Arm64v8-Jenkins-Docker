# RaspberryPi-Arm64v8-Jenkins-Docker

## This is a Jenkins Docker image that will run on a Raspberry Pi running the Ubuntu 64bit arm distribution.
#### The image is based on the official Jenkins Docker project:  https://github.com/jenkinsci/docker

Please use at your own risk.  At minimum, I'd suggest comparing this project and the official project to understand the differences.

You will need to enable swap on your pi to make Jenkins work reliably.

#### Pull from latest directly from docker:  
docker pull williamgillaspy/arm64v8jenkins  
docker run -d  -p 8080:8080 -p50000:50000 --mount type=bind,source=/mnt/fileshare/jenkins,target=/var/jenkins_home williamgillaspy/arm64v8jenkins:latest  


##### Build it and run it yourself:
Example build command:  
- docker build . -t arm64v8/jenkins:local  

Example run command:  
- docker run -d  -p 8080:8080 -p50000:50000 --mount type=bind,source=/mnt/fileshare/jenkins,target=/var/jenkins_home arm64v8/jenkins:local
