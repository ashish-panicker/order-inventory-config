# Order Inventory Config Repository

This repository serves as the centralized configuration source for the Spring Cloud Config Server of the Order Inventory system. It contains the properties files for all the microservices in the architecture.

## Services

* **discovery-service**: Configuration for the Eureka Discovery Server.
* **inventory-service**: Configuration for the Inventory Service.
* **order-service**: Configuration for the Order Service.

The properties files are organized in separate directories for each service. The Spring Cloud Config Server will read these files and provide the configurations to the respective services upon startup.
