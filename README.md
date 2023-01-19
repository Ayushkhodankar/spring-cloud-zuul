# Zuul - Spring Cloud

Zuul Server is an API Gateway application.

It handles all the requests and performs the dynamic routing of microservice applications. It works as a front door for all the requests.

# Contents in the repo

This repo consist of the implementation of the Zuul API Gateway in Java.

This samplezuul-gateway based repository consists of the following modules:
- **gateway-service** - a module that Spring Cloud Netflix Zuul for running Spring Boot application that acts as a proxy/gateway in our architecture.
- **diagnosis-service** - an API module that basically invokes services acknowlegded in diagnosis.
- **hospital-service** - an API module that basically shows and presents the services provided in hosspital arena.
