# BankingInTheCloud-Tutorials
This repo provides tutorials for the BankingInTheCloud workshop. 

## Project Setup

The master-branch contains the zip files needed for the stages. 
Note: If you cannot 

## Tutorial stages

The tutorials are done in steps that are based on each other. 
Participants are supposed to solve each tutorial stage by themselfes. A recerence solution can be found in branches.

### Stage 00 - Basic Setup

#### Goal
You have your first spring boot application up and running.

#### Project Setup
The basic project setup is based on the demo-project one can generate using the [SpringBoot Initializr](https://start.spring.io/). Use the following settings:

* Generate a ```Gradle Project``` with ```Java``` and Spring Boot ```1.5.4```
* Group: ```com.senacor.bitc```
* Artifact: ```demo```
* Dependencies: ```Web```

Open the ```demo``` project using IntelliJ IDEA.

#### Tasks

1. Implement a REST controller that offers one GET method that returns the IP address of the server. 

### Stage 01 - Cloud Config Server

#### Goal
Your spring boot application can be configured via a configuration server. 

#### Project Setup 

The cloud config requires another spring-boot project that represents the cloud config server. Use [SpringBoot Initializr](https://start.spring.io/) to generate the project using the following settings:

* Generate a ```Gradle Project``` with ```Java``` and Spring Boot ```1.5.4```
* Group: ```com.senacor.bitc```
* Artifact: ```config```
* Dependencies: ```Web``` ```Config Server```

#### Tasks

1. Configure the spring cloud config server to use a repsoitory where you put the configuration for your demo service.
2. Configure the demo service so it uses the cloud config server for configuration.
3. Configure the port where the demo application is served through the config server. The port should not be hard-wired in the demo application any more, but is defined by the configuration file served by the config server.


### Stage 02 - Flyway (database migration)

#### Goal
Create a database with dummy-data for your service using flyway migration scripts.

#### Project Setup

1. Create a XXX database 
2. (...)

#### Tasks



### Stage 03 - Spring Data

#### Goal
Create domain objects and fill them with data from the previously created database using Spring Data.

Note: include Lombok

#### Tasks


### Stage 04 - Create a second service

#### Goal
You create a second service that can communicate with the first service (demo-service).


#### Tasks



### Stage 05 - Eureka (service discovery)

#### Goal
You add a service discovery so the services can find each other through the discovery server.

#### Tasks



### Stage 06 - Docker (containerize)

#### Goal
You pack your services into containers for deployment.

#### Tasks


### Stage 07 - Messaging and Event Sourcing

#### Goal
You add endpoints that emit events, so your two services don't directly communicate with each other but one service emits an event that the other service consumes.

#### Tasks

