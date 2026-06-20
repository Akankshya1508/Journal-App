**📓 Journal Service – Secure Backend System (Spring Boot)**
A stateless, secure REST API backend for a journal management system built using Spring Boot, Spring Security, JWT authentication, and MongoDB.
The system is designed as a production-style backend service with a focus on security, scalability, and clean architecture.

**🧩 System Overview**
This application provides secure journal management capabilities for authenticated users. Each user can create, read, update, and delete their own journal entries.

The backend is designed as a stateless service, where authentication is handled using JWT tokens, eliminating server-side session dependency and enabling horizontal scalability.

**🚀 Key Features**
Stateless authentication using JWT
Secure REST APIs using Spring Security filter chain
User-specific data isolation (multi-user support)
CRUD operations for journal entries
MongoDB-based NoSQL persistence layer
Centralized exception handling (@ControllerAdvice)
Structured logging for observability
Layered architecture (Controller → Service → Repository)

**🏗️ System Architecture**
The system follows a clean layered architecture:

Controller Layer → API request handling
Service Layer → Business logic + validation
Repository Layer → Database interaction (MongoDB)
Core Design Principles
Stateless authentication (JWT-based)
Secure request filtering via Spring Security chain
Separation of concerns across layers
REST-compliant API design
No session storage on server (scalable architecture)

**🔐 Authentication & Security Flow**
User registers or logs in
Credentials are validated on the server
JWT token is generated and returned to the client
Client sends token in Authorization: Bearer <token> header
Spring Security filter intercepts request
JWT is validated before request reaches controllers
Access is granted or denied based on token validity

**📌 API Design**
Authentication APIs
POST /auth/register   → Register new user
POST /auth/login      → Authenticate user and generate JWT
Journal APIs
GET    /journal        → Fetch all journals for authenticated user
POST   /journal        → Create a new journal entry
PUT    /journal/{id}   → Update existing journal entry
DELETE /journal/{id}   → Delete journal entry

**🛠️ Tech Stack**
Java
Spring Boot
Spring Security
Spring Data MongoDB
JWT (JSON Web Token)
MongoDB
Maven

**⚙️ How to Run**
git clone https://github.com/Akankshya1508/Journal-App.git
cd Journal-App
mvn spring-boot:run

**🗄️ Configuration**
Configure MongoDB connection in application.properties:
spring.data.mongodb.uri=your-mongodb-connection-string;

**📊 System Qualities**
Stateless and horizontally scalable backend design
Secure authentication and authorization layer
Clean separation of business logic and data access
Production-style REST API structure
Extensible architecture for future microservices migration

**👩‍💻 Ownership**
Built by Akankshya
