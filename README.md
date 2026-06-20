**Journal Application – Spring Boot Backend**

A secure RESTful journal management system built using Spring Boot, JWT authentication, and MongoDB. It supports user-specific CRUD operations with logging and security filters.

**Key Features**
JWT-based authentication & authorization
Secure REST APIs using Spring Security
User-specific journal CRUD operations
MongoDB integration using Spring Data MongoDB
Request logging and exception handling
Stateless authentication architecture

**Tech Stack**
Java
Spring Boot
Spring Security
Spring Data MongoDB
JWT (JSON Web Token)
MongoDB
Maven
Architecture

**The system follows a layered architecture:**

Controller → Service → Repository pattern
Stateless authentication using JWT
MongoDB as NoSQL persistence layer
Spring Security filter chain for request validation

**Authentication Flow**

User logs in / registers
Server generates JWT token
Client sends token in Authorization header
Spring Security validates token on each request
Access granted to protected endpoints
API Endpoints
POST /auth/register – Register user
POST /auth/login – Authenticate & get JWT
GET /journal – Get user journals
POST /journal – Create journal entry
PUT /journal/{id} – Update entry
DELETE /journal/{id} – Delete entry
How to Run
git clone https://github.com/your-username/repo-name.git
cd repo-name
mvn spring-boot:run
MongoDB Configuration
spring.data.mongodb.uri=your-mongo-uri
