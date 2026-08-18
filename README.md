# Order Inventory Config Repository

This repository serves as the centralized configuration source for the Spring Cloud Config Server of the Order Inventory system. It contains the properties files for all the microservices in the architecture.

## Services

* **discovery-service**: Configuration for the Eureka Discovery Server.
* **inventory-service**: Configuration for the Inventory Service.
* **order-service**: Configuration for the Order Service.

The properties files are organized in separate directories for each service. 

## Directory Structure

```text
.
├── discovery-service
│   └── application.properties
├── inventory-service
│   ├── application-actuator.properties
│   ├── application-eureka.properties
│   ├── application-h2.properties
│   ├── application-logs.properties
│   ├── application-mysql.properties
│   ├── application-swagger.properties
│   └── application.properties
├── order-service
│   ├── application-actuator.properties
│   ├── application-eureka.properties
│   ├── application-h2.properties
│   ├── application-logs.properties
│   ├── application-mysql.properties
│   ├── application-swagger.properties
│   └── application.properties
└── README.md
```

## How Spring Cloud Config Uses This Structure

In Spring Cloud Config, you can configure the search paths so that the config server looks into specific subdirectories to resolve properties. By setting `spring.cloud.config.server.git.search-paths={application}` in your Config Server, it will dynamically look into the directory matching the application's name (e.g., `inventory-service` or `order-service`) to find its configuration files. This allows for a clean, organized separation of concerns, ensuring each microservice's configuration is isolated within its own folder while being centrally managed in this single Git repository.
