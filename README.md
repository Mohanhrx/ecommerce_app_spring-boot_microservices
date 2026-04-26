📦 E-Commerce Microservices Application
🏗️ Project Architecture (Microservices)

This project follows a Microservices Architecture where each service is independently developed and deployed.

🔧 Services Included
Eureka Server → Service Registry
API Gateway → Single entry point for all client requests
Product Service → Manages product details
Order Service → Handles order placement and processing
🔁 Communication Flow

Client → API Gateway → Microservices (via Eureka Service Discovery)

⚙️ Tech Stack
Backend: Java, Spring Boot
Microservices: Spring Cloud
Service Discovery: Netflix Eureka
API Gateway: Spring Cloud Gateway
Database: MySQL
Build Tool: Maven
Reactive Calls: WebClient
🚀 How to Run the Project
🔹 Step 1: Start MySQL

Make sure MySQL is running and create databases:

CREATE DATABASE product_db_m;
CREATE DATABASE order_db_m;
🔹 Step 2: Run Services (Order matters)

Start services one by one:

Eureka Server
Product Service
Order Service
API Gateway
🔹 Step 3: Verify Eureka Dashboard

Open:

http://localhost:8761

Ensure all services are registered:

product-service
order-service
api-gateway
🔹 Step 4: Test APIs
📌 Get Product
GET http://localhost:8000/products/{id}
📌 Place Order
POST http://localhost:8000/orders/placeOrder

Sample Request Body:

{
  "productId": 1,
  "quantity": 2
}
📌 Notes
API Gateway runs on port 8000
Product Service runs on port 8081
Order Service runs on port 8082
Eureka runs on port 8761
Ensure all services are up before testing APIs
🎯 Features
Microservices architecture
Service discovery using Eureka
Centralized routing via API Gateway
Inter-service communication using WebClient
