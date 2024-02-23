# Ecommerce Microservices Application

This is a basic Ecommerce Microservices application built with Spring Boot. The application consists of three services: Order Service, Product Service, and Inventory Service. The services communicate with each other to handle the core functionalities of an Ecommerce system.

## Services

### 1. Order Service

The Order Service is responsible for managing customer orders. It handles order creation, order retrieval, and order updates.

#### Endpoints:

- **POST /orders**: Create a new order.
- **GET /orders/{orderId}**: Retrieve details of a specific order.
- **PUT /orders/{orderId}**: Update the status of a specific order.

### 2. Product Service

The Product Service manages the product catalog. It provides endpoints for retrieving product information.

#### Endpoints:

- **GET /products**: Retrieve a list of all products.
- **GET /products/{productId}**: Retrieve details of a specific product.

### 3. Inventory Service

The Inventory Service is responsible for managing product inventory. It tracks the available quantity of each product.

#### Endpoints:

- **GET /inventory/{productId}**: Retrieve the current inventory status for a specific product.
- **PUT /inventory/{productId}**: Update the inventory quantity for a specific product.

## Database

The application uses MySQL as the database to store and retrieve data. Make sure to configure the database connection properties in each service's `application.properties` file.

## Architecture

The application follows the Model-View-Controller (MVC) architecture.

- **Model**: Represents the data and business logic of the application.
- **View**: Handles the presentation and user interface.
- **Controller**: Manages the communication between the Model and View.

## Running the Application

1. Clone the repository.
2. Navigate to each service's directory (`order-service`, `product-service`, `inventory-service`) and run the following command:

   ```bash
   ./mvnw spring-boot:run
