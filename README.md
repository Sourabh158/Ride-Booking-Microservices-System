# Ride-Booking-Microservices-System
# 🚖 Online Ride Booking System (Microservices)

link of other Repositories
      - https://github.com/Sourabh158/EcoRide-Ride-Service
      - https://github.com/Sourabh158/EcoRide-Deploy-User
      - https://github.com/Sourabh158/API-GATEWAY
      - https://github.com/Sourabh158/EcoRide-Deploy-Notification
      - https://github.com/Sourabh158/Service-Registry

### 🚀 Overview
**Online Ride Booking System** is a scalable, backend microservices application designed to mimic core functionalities of apps like **Uber/Ola**. Built using **Java, Spring Boot, and Spring Cloud**, it features independent services for user management and ride processing, communicating seamlessly via **REST APIs**.

This project demonstrates the implementation of **Service Discovery (Eureka)**, **Inter-Service Communication (Feign Client)**, and **Database Management (PostgreSQL/MySQL)**.

---

### 🛠️ Tech Stack & Tools
- **Programming Language:** Java 17
- **Framework:** Spring Boot 3.x
- **Architecture:** Microservices
- **Database:** PostgreSQL / MySQL
- **Service Discovery:** Netflix Eureka Server
- **Communication:** Spring Cloud OpenFeign
- **Build Tool:** Maven
- **Testing:** Postman

---

### 📂 Microservices Architecture (Source Code)
This project is divided into multiple independent services. Click the links below to view the source code for each:

| Service Name | Description | Repository Link |
| :--- | :--- | :--- |
| **User Service** | Manages Rider/Driver registration and profiles. | [🔗 Link to User-Service Repo](YAHAN_APNA_USER_SERVICE_KA_LINK_DALO) |
| **Ride Service** | Handles ride booking, fare calculation, and trip logic. | [🔗 Link to Ride-Service Repo](YAHAN_APNA_RIDE_SERVICE_KA_LINK_DALO) |
| **Service Registry** | Netflix Eureka Server for Service Discovery. | [🔗 Link to Eureka-Server Repo](YAHAN_APNA_EUREKA_REPO_KA_LINK_DALO) |
| **API Gateway** | (Optional) Central entry point for all requests. | [🔗 Link to Gateway Repo](AGAR_HAI_TOH_LINK_DALO_VARNA_HATA_DO) |

---

### ✨ Key Features
1.  **Microservices Architecture:** Decoupled services for better scalability and maintenance.
2.  **Service Discovery:** Dynamic registration of services using **Netflix Eureka**.
3.  **Inter-Service Communication:** `Ride-Service` fetches user details from `User-Service` internally using **Feign Client**.
4.  **RESTful APIs:** Clean and well-documented API endpoints.
5.  **Data Persistence:** Uses **Spring Data JPA** & **Hibernate** for efficient database operations.
6.  **Error Handling:** Global Exception Handling for scenarios like "Service Unavailable (503)" or "User Not Found".

---

### ⚙️ How to Run Locally

1.  **Clone the Repositories:** Clone all the services listed above.
2.  **Start Service Registry (Eureka):**
    - Run the Eureka Server application first on port `8761`.
3.  **Start Microservices:**
    - Run **User-Service** (Port: `8081` or as configured).
    - Run **Ride-Service** (Port: `8082` or as configured).
4.  **Verify Eureka Dashboard:**
    - Open `http://localhost:8761` in your browser. You should see `USER-SERVICE` and `RIDE-SERVICE` registered.

---

### 🔌 API Endpoints (Postman)

**1. Register a User (Rider/Driver)**
- **Method:** `POST`
- **URL:** `http://localhost:8081/users`
- **Body:**
  ```json
  {
      "name": "Sourabh",
      "email": "sourabh@example.com",
      "mobileNumber": "9876543210",
      "password": "password123",
      "role": "RIDER"
  }
