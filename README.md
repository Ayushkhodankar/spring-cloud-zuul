# Zuul - Spring Cloud

Zuul Server is an API Gateway application. It handles all the requests and performs the dynamic routing of microservice applications. It works as a front door for all the requests.

## Contents in the Repository

This repository consists of the implementation of the Zuul API Gateway in Java.

### Modules

1. **gateway-service**
   - A module using Spring Cloud Netflix Zuul for running a Spring Boot application that acts as a proxy/gateway in our architecture.

   #### Dependency
   Add the following dependency in `pom.xml` to enable the Zuul Gateway in the module:
   ```xml
   <dependency>
       <groupId>org.springframework.cloud</groupId>
       <artifactId>spring-cloud-starter-netflix-zuul</artifactId>
   </dependency>
   ```

   #### Configuration
   Add the following properties in `application.properties`:
   ```properties
   zuul.routes.doctor-service.url=http://localhost:8081/
   zuul.routes.diagnosis-service.url=http://localhost:8082/
   ribbon.eureka.enabled=false
   server.port=8080
   ```

2. **diagnosis-service**
   - An API module that invokes services acknowledged in diagnosis.

   #### Configuration
   Add the following properties in `application.properties`:
   ```properties
   spring.application.name=diagnosis-service
   server.port=8081
   ```

3. **hospital-service**
   - An API module that shows and presents the services provided in the hospital arena.

   #### Configuration
   Add the following properties in `application.properties`:
   ```properties
   spring.application.name=doctor-service
   server.port=8082
   ```

## Tools and Technologies Used

- **Spring Tool Suite 4**
- **Eclipse 2022-12**
- **Java Version**: 1.8
- **JDK**: 17
- **Zuul Netflix Support/Dependency**
