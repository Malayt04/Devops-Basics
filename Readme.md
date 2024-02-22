# Devops Basics


# Day 1


# Monolithic vs Microservices architecture

## Monolithic Architecture:
![monolithic architecture](https://media.geeksforgeeks.org/wp-content/uploads/20200322175817/monolithic.jpg)

Built as a single unit <br>
Duplicated on each server <br>

### Tradational Method Of Deployment
In earlier times, the whole app used to be deployed as a single unit including the frontend, backend and the bisuness logic. Even if we make a small change any part of the application, we have to deploy the  whole app everytime. For scalling also, the whole app used to be deplployed in multiple servers.



## Microservices:
![Microservices](https://media.geeksforgeeks.org/wp-content/uploads/20200322182733/microservices.jpg)

Seperates functionallity into smaller seperate services each with a single responsibility <br>
Scales out by deploying each service independently<br>
Loosely coupled<br>
Enable autonomus developement by different teams, languages and platform<br>
Can be written by smaller times<br>
Each microservice can have its own data and database<br>

### Deployment in  Microservice architecture:
Services are deployed as units. For scalling purpose also, the applications are deployed independently.

### Microservices Anti-Patterns:
Risk of unessecery complexity.<br>
Risk of security.<br>
Domaino effect(Error in one area could affect the other parts).<br>
Latency Issue.<br>
Trainsint Error<br>
Multiple Point of failure.<br>



# Cloud Native
![Cloud Native](https://www.okta.com/sites/default/files/styles/tinypng/public/media/image/2020-11/Cloud_Native_Architecture.png?itok=CmjOtXAS)

Cloud native refers to an approach to designing, building, and operating applications that are optimized for cloud computing environments. Cloud native architecture involves breaking down applications into smaller, independent services called microservices that can be deployed and scaled independently. Cloud native applications are designed to take full advantage of cloud infrastructure, including automation, containerization, and orchestration. The benefits of cloud native architecture include increased efficiency, scalability, and resilience, as well as reduced costs and improved availability.

## Difference between cloud native and cloud computing:

Cloud-native refers to an approach to designing, building, and running applications that take full advantage of cloud computing infrastructure. Cloud-native applications are typically composed of microservices, which are small, independent services that work together. They are designed to be flexible, scalable, and resilient, and they can be deployed and scaled independently. Cloud-native applications are built using continuous integration and continuous delivery (CI/CD) principles, container-based engines, and orchestrators. They are optimized for the cloud and can be run on any cloud infrastructure, including public, private, and hybrid clouds
<br><br>
Cloud computing, on the other hand, is a model for delivering computing services such as servers, storage, databases, networking, software, analytics, and intelligence over the internet ("the cloud") to offer faster innovation, flexible resources, and economies of scale. Cloud-native applications are built to leverage the benefits of cloud computing, such as scalability, agility, and cost savings
<br><br>
Cloud-based applications, in contrast, are applications that are hosted on a cloud platform but were not originally designed for the cloud. They may not take full advantage of cloud-native features and may be slower to deploy and less flexible than cloud-native applications
<br><br>
Cloud-enabled applications are applications that have been adapted to run on cloud infrastructure, but they may not have been designed specifically for the cloud. They may not have the same level of flexibility, scalability, and resilience as cloud-native applications
<br><br>
In summary, cloud-native applications are designed to take full advantage of cloud computing infrastructure, while cloud-based applications are applications that have been adapted to run on cloud infrastructure. Cloud-enabled applications are applications that have been adapted to run on cloud infrastructure but were not originally designed for the cloud.


# Containers
We have been using the term containers for a while now and you must be wondering what it means or looks like? So now let's talk about it in detail. But first, we have to also discuss about virtual machines as that is where the whole story starts. <br>
A <b>virtual machine</b> is a software-based, self-contained computer system that runs on top of a host operating system. VMs are capable of running their own operating systems and applications, and they are often used for system virtualization, server virtualization, and cloud computing. VMs are hardware-centric and can be used to run applications that require specific hardware configurations or to isolate applications from the host environment. Now we know about virtual machines, let's see what containers do.
<br>
Containers, on the other hand, are lightweight, self-contained units that encapsulate an application's code, dependencies, and runtime environment. Containers are application-centric and are designed to be portable, scalable, and easy to manage. Containers are built on top of a host operating system and share the host's kernel, which makes them more lightweight and faster to start than VMs. Containers are often used in cloud-native applications and microservices architectures. <br>
In summary, VMs are used for running applications that require specific hardware configurations or to isolate applications from the host environment, while containers are used for building, deploying, and managing applications that are portable, scalable, and easy to manage.<br>

![COntainers vs Vm's](https://www.netapp.com/media/Screen-Shot-2018-03-20-at-9.24.09-AM_tcm19-56643.png)



# Day 2


# Gerting Started With Docker:

We have heard a very common  saying of developers "It was running on my system" due to differences between local machines. Let's see how docker resolves this issue.<br><br>

# What is Docker
At its core, Docker is a platform that enables developers to package, distribute, and run applications in isolated containers. These containers encapsulate everything an application needs to run, including code, runtime, system tools, libraries, and settings.

## Why Docker:
Docker simplifies the process of software development and deployment by providing a consistent environment across different platforms. Here are some key reasons why Docker has become indispensable in modern software development:<br><br>
#### Portability: 
Docker containers can run on any machine that supports Docker, regardless of the underlying operating system. This portability eliminates the notorious "it works on my machine" problem, ensuring consistency across development, testing, and production environments.

#### Isolation: 
Docker containers offer lightweight, isolated environments for running applications. Each container operates independently of others, preventing conflicts between dependencies and enabling efficient resource utilization.

#### Scalability: 
Docker simplifies the scaling of applications by allowing developers to replicate containers across multiple hosts. This flexibility enables seamless scaling up or down based on demand, ensuring optimal performance and resource utilization.

#### Efficiency:
Docker's lightweight nature and efficient resource utilization make it ideal for microservices architectures and cloud-native applications. By breaking down monolithic applications into smaller, manageable components, developers can achieve greater agility, scalability, and resilience.


# Docker Architecture
![Docker-Architecture](https://imgs.search.brave.com/YWnLa2AiK0-6aVz5ZRS5Y-WeTwOfQfby2o6S7Ne8bL8/rs:fit:860:0:0/g:ce/aHR0cHM6Ly9kb2Nz/LmRvY2tlci5jb20v/Z2V0LXN0YXJ0ZWQv/aW1hZ2VzL2RvY2tl/ci1hcmNoaXRlY3R1/cmUud2VicA)

Understanding Docker's architecture provides insight into how Docker manages containers, images, and the resources of the host system. Docker's architecture is designed to be modular, allowing for flexibility and scalability across various environments. Let's delve into the details of Docker's architecture:<br><br>

## Docker Daemon
The Docker daemon runs as a background process on the host machine and is responsible for managing Docker objects such as containers, images, networks, and volumes. It listens for Docker API requests and executes them, handling container lifecycle management, image handling, networking, and storage operations.

## Docker Client:
This is what we use to interact with docker. It is a command line tool. Users issues a command to performing various docker operations such as creating managing and inspecting containers. The Docker client communicates with the Docker daemon via the Docker API, enabling users to control Docker's behavior and manage containerized applications.

## Docker regestiry:
It is a place where all the docker images are stored. Its just like github but for docker containers. You can pull an image made my someone else and also can upload your own image. You can check out the website (hub.docker.com) for more info and hands on.

## Docker Engine API:
The Docker Engine API is a RESTful API that exposes endpoints for interacting with the Docker daemon. The API enables programmatic access to Docker's functionality, allowing developers to integrate Docker into their applications and automate container management tasks. The Docker Engine API is used by the Docker client, Docker Compose, and other Docker-compatible tools to interact with the Docker daemon.


# Docker Objectes 

In the previous topic you saw some terms like images, volumes etc. These are all docker objects. Let's discuss then in detail:

## Images:
A docker image is a file that defines a docker container. It is the tampelate containing the filesystem of the containarized application and its dependencies. Imagine it as a class in Object Oriented Programming. This will make  you understand better. Containers are the instances of these docker images. Think of them as the object of a particular class. Now I hope the relation between an image and a container is clear to you.

## Docker File:
Docker file is a file that we create which contains the step of instruction that will execute when you run a container in your local system. Let's take an example to understand it better:<br>
Let's imagine you're building a model airplane from a kit. The kit comes with a set of instructions that tell you how to assemble the airplane step by step. You follow these instructions to ensure that the airplane is built correctly. a Dockerfile is like those instructions for building a containerized application. It's a simple text file that contains a set of instructions, known as commands, that specify how to build a Docker image.<br><br>

Here's how it works:<br>
### Choosing a base image:
Suppose you are containerizing a nodejs application. You have to specify on which version of node will the application run or on which operatiing system it should run which are already predefined images in the docker registry. These are known as the base images.
<br>
### Specify instruction:
In the Dockerfile, you specify a series of instructions, such as copying files, installing software, setting environment variables, and defining runtime commands. These instructions are written in a clear, human-readable format.
<br>
### Build the image:
Once you have written the Dockerfile, you use the <b>docker build</b> command to build the Docker image based on the instructions in the file. Docker reads the Dockerfile and executes each instruction to create the image.

Here is an expample of a dockerfile for a nodejs application:

```Dockerfile
FROM node:lts-alpine

# Set Node.js environment to production
ENV NODE_ENV=production

# Set the working directory
WORKDIR /usr/src/app

# Copy package.json, package-lock.json, and npm-shrinkwrap.json files
COPY ["package.json", "package-lock.json*", "npm-shrinkwrap.json*", "./"]

# Install production dependencies
RUN npm install --production --silent && mv node_modules ../

# Copy application files
COPY . .

# Expose port 3000
EXPOSE 3000

# Set user permissions
RUN chown -R node /usr/src/app
USER node

# Command to run the application
CMD ["node", "app.js"]
```

<br><br>

# Docker Commands
 Now let's discuss some basic docker commands which will help you get started:<br>

- To check Docker vesrion

```
docker version
```

- To check all the available images

```bash
docker images
```

- Pull/Download the image from the Docker registry to local machine.

```bash
docker pull <image name>
//Eg: docker pull nginx
```

- To run an container (It will 1st pull the image if not present in the local sytem)
  - NOTE: When we just provide the name of the image it will pull the latest one, i.e `nginx:latest`. We can also specify the version `nginx:1.14`
  - Additioanly we can use flags
  
     - `--name <name> `- To give a name to the container.
     - `-p <Host port:container port>`- To forward the port.
     - `-d` - To run in detached mode
     - `-it` - For interactive envirnoment
     - `-e` - For environment variable

```bash
docker run <image-name>
//Eg: docker run nginx
```

- We can also pass a complete `.env` file

```bash
--env-file <path-to-env-file>
Eg: --env-file ./.env
```

### Docker Container

- To stop a running container

```bash
docker stop <container-ID/name>
``` 

- To resume a stopped container

```bash
docker start <container-ID/name>
```

- To check the running processes inside a container.

```bash
docker top <container-name/id>
```

- To check stats of running container.

```bash
docker stats <container-name/id>
```

- Check the config and info of a container.

```bash
docker inspect <container-name/id>
//Eg: docker inspect mynginx
```

- Check all the container running.

```bash
docker ps
or
docker container ls
```

- To start and interactive session and attach terminal with the container.

  - NOTE: every image does not support `bash` so we should use `sh`

```
docker exec -it <container-ID/name> bash/sh
```

- To check which ports has been exposed and forwarded

```bash
docker port <image-name>
```

- To check all the containers (stopped, paused and running)

```bash
docker ps -a
```

- Check logs of a container

```bash
docker logs <container-ID/name>
```

- Delete all the stopped containers

```bash
docker container prune -f
```

- Delete all the containers (stopped, paused and running)
```bash
docker rm -f $(docker ps -aq)
```
- Delete all the images 
```bash
docker rmi -f $(docker images -q)
```

- Remove unused images
```bash
docker image prune -all
```

- Auto cleanup when the container exits

```bash
 docker container run —rm <image-name>
```

### Docker Network

- Check list of avilable networks.

```bash
docker network ls
```

- Inspect a network components, like which container are attached to that network.

```bash
docker network inspect <network-name>
```

- Run a container on a certian network/own careted network 

```
docker run --network <network-name> <image-name>
```

```
docker inspect --format "{{.NetworkSettings.IPAddress}}" <container-name>
```

### Docker Images

- Remove an image

```bash
docker rmi <image name> -f
```

- Remove all the images at once

```bash
docker rmi $(docker images -q)
```

- To inspect an image layers and other info

```bash
docker inspect  <image-name/id>
```

- Check the image layers formation

```bash 
docker history <image-name/id>
```
- Create a our own image with an existing image.

```
docker image tag <image-name:tag> <new-image-name:tag>
docker image tag nginx pradumna/nginx:hello
docker image tag ubuntu:18.04 pradumna/ubuntu:example
```

### Docker Volume

- Create bind mount
  - Help to sync our local files with help of Docker container.
  

- To sync our local machine changes with help of Docker volume (Bind mount)
    - `- v` is use to define volume, also we give another `-v` flag to override the changes so that it will not chnage in container.

```bash
docker run -v <path-to-folder-on-local-machine>:<path-to-folder-on-container> -p <host-port>:<container-port> -d --name docker-node docker-node
docker
```

```bash
docker run -v <path-to-folder-on-local-machine>:<path-to-folder-on-container> -v <path-to-file/folder-on-container> -p <local-machine-port>:<container-port> -d --name docker-node docker-node
```
To make it read only so that when you add some files inside it, the container will not get created on your local machine use `-v port:port:ro`

- docker  volume command for mounting the docker socket to the docker container for accessing the host's docker daemon for performing the continuous integration in jenkins while using docker as a agent.. 
```bash
docker run -it -v /var/run/docker.sock:/var/run/docker.sock docker-image:version bin/bash
```

### Docker Compose

- Run docker compose file.
  Note: By default it finds for the file name `docker-compose.yaml`, to give file with other naming use `-f <file-name.yaml>` command

```bash
docker compose up -d
```

```bash
docker compose down
```

- To rebuilt the new Image with thew new changes

```bash
docker compose up --build
```

- Override the existing of compose file

```bash
docker compose -f docker-compose.yaml  -f docker-compose.dev.yaml
```

###  Docker Swarm and Services

- Initalize swarm

```bash
docker swarm init
```

- Check all the node available

```bash
docker node ls
```

- To add a node as a manager

```bash
docker node update --role manager <node-name>
```

- To create an overlay network

```bash
docker network create -d overlay backend
```

- Create a service. Also we can add flags for further customization.

    - `--name` - to give a service name
    - `--replicas` - to define how many running instance of the same image.
    - `-p` - for port forwarding

```bash
docker service create -p 8080:80 --name vote --replicas 2 nginx
```

- To get all task containers running on different node 

```bash
docker service ps <service-name/id>
```

> SERVICE UPDATE

- To scale up the service (i.e increasing the no of replicas)

```bash
docker service scale <service name>=<no to scale>
docker service scale mynginx=5
```

- To update the image in running service

```bash
docker service update --image <updated image> <service name>
docker service update --image mynginx:1.13.6  web
```

- To update the port

We can't directly update the port We have to add and remove the ports

```
docker service update --publish-rm 8080 --publish-add 808180 <service name>
docker service update --publish-rm 8080 --publish-add 808180 mynginx
```

### Docker Stack

- To deploy a stack file

```bash
docker stack deploy -c <file-name.yaml> <stackname>
```

- To remove running stack

```
docker stack rm <stack name>
```

- To check list of stacks running

```
docker stack ls
```

**STACK -> SERVICES -> TASKS -> CONTAINERS**

- To check which services are running inside a staacks

```
docker stack services <stack name>
```

- To check taks are running inside a stack

```
docker stack ps <stack name> 
```

> Registry

```
127.0.0.0:5000/v2/_catalog
```

### Tips and Short hands

- Run the command with the container creation

```bash
doc run <image-name> <command>
// Eg: `doc run ubuntu:16.04 echo hey`
```


- Creating our Own image and container.

```
Step 1 - create Dockerfile
Step 2 - docker build -t myimage:1.0 <path-of-dockerfile> (-t for tag)
Step 3 - docker run myimage:1.0
```


