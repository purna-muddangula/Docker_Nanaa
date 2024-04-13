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


Port Binding












