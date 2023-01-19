# Zuul - Spring Cloud

Zuul Server is an API Gateway application.

It handles all the requests and performs the dynamic routing of microservice applications. It works as a front door for all the requests.

# Contents in the repo

This repo consist of the implementation of the Zuul API Gateway in Java.

This sample zuul-gateway based repository consists of the following modules:
- **gateway-service** - a module that Spring Cloud Netflix Zuul for running Spring Boot application that acts as a proxy/gateway in our architecture.

This dependency should be added in pom.xml to enable the zuul gateway in the module.
### 
    <dependency>
			<groupId>org.springframework.cloud</groupId>
			<artifactId>spring-cloud-starter-netflix-zuul</artifactId>
		</dependency>
    
This should be provided in application.properties of the module.
### `zuul.routes.doctor-service.url=http://localhost:8081/`
### `zuul.routes.diagnosis-service.url=http://localhost:8082/`
### `ribbon.eureka.enabled=false`
### `server.port=8080`
- **diagnosis-service** - an API module that basically invokes services acknowlegded in diagnosis.

This should be provided in application.properties of the module.
### `spring.application.name=diagnosis-service`
### `server.port=8081`
- **hospital-service** - an API module that basically shows and presents the services provided in hosspital arena.

This should be provided in application.properties of the module.
### `spring.application.name=doctor-service`
### `server.port=8082`


This Repository was built in :

1. Spring Tool Suite - 4
2. Eclipse 2022-12
3. Java Version - 1.8
4. JDK-17
5. Zuul-Netflix Support/ Dependency
