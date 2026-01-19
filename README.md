# E-commerce-assignment

## 📌 Project Title

Minimal E-Commerce Backend API using Spring Boot

---

## 🎯 Project Description

This project implements a backend system for a minimal e-commerce application using Spring Boot and MongoDB. The system supports product management, cart operations, order processing, and online payment handling using Razorpay integration. The project demonstrates real-world backend concepts like database relationships, REST APIs, and webhook-based asynchronous payment updates.

---

## 🏗️ Tech Stack

* Java 17+
* Spring Boot
* Spring Data MongoDB
* MongoDB
* Razorpay Payment Gateway
* Postman (API testing)

---

## ⚙️ Setup Instructions

* Clone the project repository
* Install MongoDB and ensure it is running on `localhost:27017`
* Open the project in IntelliJ IDEA
* Update `application.properties` with Razorpay keys
* Run `ECommerceApplication.java`
* Server starts at `http://localhost:8080`

---

## 📋 API Documentation

### User APIs

| Method | Endpoint          | Description |
| ------ | ----------------- | ----------- |
| POST   | `/api/users`      | Create user |
| GET    | `/api/users/{id}` | Get user    |

---

### Product APIs

| Method | Endpoint                  |
| ------ | ------------------------- |
| POST   | `/api/products`           |
| GET    | `/api/products`           |
| GET    | `/api/products/search?q=` |

---

### Cart APIs

| Method | Endpoint                   |
| ------ | -------------------------- |
| POST   | `/api/cart/add`            |
| GET    | `/api/cart/{userId}`       |
| DELETE | `/api/cart/{userId}/clear` |

---

### Order APIs

| Method | Endpoint                       |
| ------ | ------------------------------ |
| POST   | `/api/orders`                  |
| GET    | `/api/orders/{orderId}`        |
| GET    | `/api/orders/user/{userId}`    |
| POST   | `/api/orders/{orderId}/cancel` |

---

### Payment APIs

| Method | Endpoint                |
| ------ | ----------------------- |
| POST   | `/api/payments/create`  |
| POST   | `/api/webhooks/payment` |

---

## 🔄 Implementation Flow

* Create User
* Create Products
* Add Products to Cart
* Create Order from Cart
* Initiate Payment
* Razorpay Webhook updates Order Status

---

## ⭐ Bonus Implemented

* Product Search
* Order History
* Order Cancellation
* Razorpay Payment Gateway

---

## ✅ Conclusion

This project demonstrates how a real e-commerce backend works by connecting cart, order, and payment flows using REST APIs and webhook-based updates.

## 📊 ER Diagram (Logical)

```
USER ───< CART_ITEM >─── PRODUCT
│
└───< ORDER ───< ORDER_ITEM >─── PRODUCT
     │
     └── PAYMENT
```

