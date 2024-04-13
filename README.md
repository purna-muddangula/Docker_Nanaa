# Docker_Nanaa

Docker:Virutalization software
Makes developing and deploying apps much easier
packages apps with all the necessary dependencies, configuration, system tools and runtime 
portable artifact easily shared and distributed 

Docker Artifact includes everyhting that app needs
Run docker command to fetch and run docker artifacts 



Virtual machine vs Docker


In virtualization:

Docker virtulises os app layer 
services and apps installed on top of that layer

Virtual machine virtualises complete OS, kernel and os app layer 


Docker only supports linux
vm supports all os 

In order overcome this Docker desktop came into the picture 

Docker desktop:uses  Hypervisor layer with a light weight Linux distro


Docker Desktop includes 

Docker Engine
Docker CLI -Client 


Docker Images vs Docker Containers 

Package or artifact that we produce with docker is called Docker Image 

Executable app artifact
Includes app source code, but also complete env configuration
In the docker image it also installed the req softwares like node and npm
we can also add nev variables what we need 
so all of the information is packaged in the docker image together with the app code 
here package is called IMAGE 

When we take the images and download it on server and run image on os and the app inside starts the pre configured env that gives us container

the containers are created 

Docker Conatiner:Running instance of image is called a container


Docker   Registry:A storage and distribution systems for Docker images 

Docker itself it offers biggest Docker registry called Docker Hub

Docker images also versioned and different versions are identified by Tags
Tags are used to identify images by names 

Latest tag refers to newest release 

How to GET image from Docker Hub

Pulling an image 



docker run ngnix(name of image):creates container

Docker generates a random name for container automatically if we don't specify the name

-d or --detach=Runs container in background and prints the container id

docker logs:view logs from service running inside the conatiner 


Port Binding:Binds thecontainer's port to the host port to make the service available to outside world
Container runs on specific port
Docker stop:Stop one or more containers

-p or publish:publish a containersport to the host

docker run -d  -p 9000:80 ngnix:1.23

Docker run 

Creates a new container
Doesn't re use previous container

docker ps -a or -all(lists all containers stopped and running)
docket start=start one or

docker run --name web-app  -d -p 9000:80 ngnix :1.23


Public and private docker registries

Public:any one can access
Private:Need to authenticate before accessing the registry 
all big cloud provider offers private registries 
Nexus:popular artifact repository manager

Registry vs Repository

Registry:Service providing storage
collection of repositories

Repository:Collection of related images with same name but diff versions 

Docker Hub:is a registry
On Docker Hub you can host public or private repositories for apps

Docker File:Create own images 

We want to deploy our app as docker container

We need to create a definition of how to build an image from our app


DockerFile-->BUILD Image-->RUN-->Container

Dockerfile is text document that contains commands to assesmble image
Docker can then build an image by reading instructions 

We will write Dockerfile from Node js app

Structure of Docker file

Dockerfile strat from parent image or base image
It a docker image that your image is based on

have to choose base image depending up on which tools you need to have available 
eg:node base, tomcat, python 


FROM:

Dockerfile must begin with a FROM instruction
Build this image from specified image 


Evey image consists ofmultiple image layers 
This makes docker so efficient becauseimage layers can be cached 

RUN

Will execute any command in a shell inside the container env 

Executing NPM install:To install dependencies 


STRUCTURE OF DCKERFILE

COPY

Copies files or directories from <src> and adds them to filesystem of the container at the path <dest>
 While RUN is executed on container and COPY is executed on HOST


 WORKDIR:Sets the working dir for all commands 

 CMD:The instruction hat is to be executed when docker container starts
 There can only be one CMD instruction in Dockerfile

 Docker image consists of layers 

 each instruction in docker file createsone layer
 these layers are stacked and each one is a delta of chnages from previous layer














