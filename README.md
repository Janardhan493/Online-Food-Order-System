# Online Food Order System

A RESTful backend application developed using **Java, Spring Boot, Spring Data JPA, and MySQL**. This application allows users to create, retrieve, update, and delete food orders through REST APIs.

## Features

- Create new food orders
- Retrieve all orders
- Retrieve an order by ID
- Update complete order details
- Update specific order fields
- Delete orders
- Store order information in MySQL
- REST API architecture

## Technologies Used

- Java 17
- Spring Boot
- Spring Web
- Spring Data JPA
- Hibernate
- MySQL
- Maven
- REST APIs

## Project Structure

```text
src/main/java/com/jaan/food_order
├── controller
│   └── OrderController.java
├── entity
│   └── FoodOrder.java
├── repository
│   └── OrderRepository.java
├── service
│   └── OrderService.java
└── OnlineFoodOrderSystemApplication.java
```

## Database Configuration

Create a MySQL database:

```sql
CREATE DATABASE food_order_db;
```

Configure `src/main/resources/application.properties`:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/food_order_db
spring.datasource.username=root
spring.datasource.password=YOUR_MYSQL_PASSWORD

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true

server.port=8081
```

Replace `YOUR_MYSQL_PASSWORD` with your local MySQL password.

## How to Run

1. Clone the repository.
2. Configure MySQL.
3. Update `application.properties`.
4. Open the project in VS Code.
5. Run:

```bash
mvn spring-boot:run
```

The application runs at:

```text
http://localhost:8081
```

## REST API Endpoints

Base URL: `/api/orders`

| HTTP Method | Endpoint | Description |
|---|---|---|
| GET | `/api/orders` | Retrieve all orders |
| GET | `/api/orders/{id}` | Retrieve order by ID |
| POST | `/api/orders` | Create a new order |
| PUT | `/api/orders/{id}` | Update complete order |
| PATCH | `/api/orders/{id}` | Update selected fields |
| DELETE | `/api/orders/{id}` | Delete an order |

## Sample Request

### Create Order

**POST** `/api/orders`

```json
{
  "customerName": "Janardhan",
  "foodItem": "Chicken Biryani",
  "quantity": 2,
  "price": 250.00
}
```

## Testing

The REST APIs were tested using PowerShell `Invoke-RestMethod`.

## Learning Outcomes

- Building REST APIs using Spring Boot
- Implementing CRUD operations
- Understanding Controller, Service, and Repository layers
- Integrating MySQL with Spring Data JPA
- Using HTTP methods such as GET, POST, PUT, PATCH, and DELETE
- Testing REST endpoints

## Author

Janardhan

Java Full Stack Developer
