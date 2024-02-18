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


<br>Now let's talk about docker, a container manager.



