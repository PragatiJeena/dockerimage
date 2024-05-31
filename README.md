# dockerimage
Dockerfile with Ubuntu 16.04 as a base image. The image should have following packages present:  telnet curl ffmpeg Finally, when running a container from the docker image, it should launch with bash.



#########This Dockerfile builds an Ubuntu 16.04 based Docker image with the following packages installed#########
- telnet
- curl
- ffmpeg

####### Build Instructions#########
1. Clone or download this repository.
2. Navigate to the directory containing the Dockerfile.
3. Build the Docker image using the following command:
    docker build -t Dockerfile .
    

Step 1: Create Dockerfile
  Open ubuntu Virtual Machine and first download the Docker in it
  For installing docker use the command
  
---->sudo apt update

---->sudo apt install -y apt-transport-https ca-certificates curl software-properties-common

---->curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

---->sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"

---->sudo apt update

---->sudo apt install -y docker

Create a DockerFile Inside a Directory for this steps are:-

---->mkdir imagedirectory

---->vim dockerfile (keep in mind we are using UBUNTU so before usinf vim we need to install it)

Step:2 Build Docker Image

Navigate to the directory containing the Dockerfile

---->docker build -t Dockerfile .

Step 3: Run Docker Container

after the the image get build sucessfully 

---->docker run -it Dockerfile

This command launches a Docker container from the Dockerfile image in interactive mode (-it) and starts bash as the default command.

