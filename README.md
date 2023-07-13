# Spring Boot Eureka Server

This is a sample project demonstrating the setup and usage of a Spring Boot Eureka Server, which acts as a service registry and discovery server for microservices.

## Prerequisites

Before running this project, ensure that you have the following prerequisites installed:

- Java Development Kit (JDK) 8 or above
- Maven

## Getting Started

To get started with the project, follow these steps:

1. Clone the repository to your local machine:

   ```
   git clone https://github.com/Team-0230/eureka-server-springboot.git
   ```

2. Navigate to the project directory:

   ```
   cd eureka-server-springboot
   ```

3. Build the project using Maven:

   ```
   mvn clean install
   ```

4. Run the application:

   ```
   mvn spring-boot:run
   ```

5. The Eureka Server will start running at `http://localhost:8761`. You can access the Eureka dashboard in your browser to view registered services and instances.

## Configuration

The Eureka Server can be configured through the `application.properties` file located in the `src/main/resources` directory. You can modify the following properties according to your requirements:

```properties
# Server port
server.port=8761

# Eureka server configuration
eureka.client.register-with-eureka=false
eureka.client.fetch-registry=false
eureka.instance.hostname=localhost
```

## Usage

To register a service with the Eureka Server, include the `spring-cloud-starter-netflix-eureka-client` dependency in your service's `pom.xml` file, and configure it to connect to the Eureka Server by specifying the following properties:

```properties
eureka.client.serviceUrl.defaultZone=http://localhost:8761/eureka/
```

For more information on using Eureka Server with Spring Boot, refer to the [official documentation](https://docs.spring.io/spring-cloud-netflix/docs/current/reference/html/#spring-cloud-eureka-server).

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvement, please open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).

## Acknowledgements

This project was inspired by the Spring Cloud Netflix project and its Eureka Server implementation.
