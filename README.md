# API Gateway

This project is a Spring Cloud API Gateway for routing requests to the following microservices:

- [Order Service](https://github.com/OmariJuma/order-service)
- [Inventory Service](https://github.com/OmariJuma/inventory-service)
- [Product Service](https://github.com/OmariJuma/product-service)

## Overview

The API Gateway acts as a single entry point for all client requests and forwards them to the appropriate backend service.

## Routes

| Path Prefix              | Service           | Target URL                |
|--------------------------|-------------------|---------------------------|
| `/api/v1/products`       | Product Service   | `http://localhost:8082`   |
| `/api/v1/orders`         | Order Service     | `http://localhost:8081`   |
| `/api/v1/inventory`      | Inventory Service | `http://localhost:8083`   |

## How It Works

- Requests to `/api/v1/products` are routed to the Product Service.
- Requests to `/api/v1/orders` are routed to the Order Service.
- Requests to `/api/v1/inventory` are routed to the Inventory Service.

## Prerequisites

- Java 21+
- Maven
- The three microservices running locally on their respective ports.

## Running the Gateway

```sh
mvn spring-boot:run