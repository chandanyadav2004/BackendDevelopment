# Major Components of Backend Development

This document explains the **core building blocks of a backend system**, including programming, databases, architecture flow, and a standard project structure.

---

## 1. Two Major Components of Backend

A backend system is mainly divided into **two major components**:

---

### 1. Programming (Application Layer)

This layer contains the **business logic** of the application.

Common backend programming languages:
- Java
- JavaScript
- Python
- PHP
- Golang
- C++

👉 In real-world projects, **one framework** is usually chosen.

Examples:
- Java → Spring Boot  
- JavaScript → Express.js / NestJS  
- Python → Django / Flask  

---

### 2. Database (Data Layer)

The database stores and manages application data.

#### Types of Databases

**Relational Databases (SQL):**
- MySQL
- PostgreSQL
- SQLite

**Non-Relational Databases (NoSQL):**
- MongoDB

To interact with databases efficiently:
- **ORM (Object Relational Mapping)** – for SQL databases
- **ODM (Object Document Mapping)** – for NoSQL databases

Examples:
- Sequelize, TypeORM → SQL
- Mongoose → MongoDB

---

## 2. High-Level Backend Architecture

        Browser / Mobile App
        ↓
        API
        ↓
        Backend
        ↓
        Database


### Explanation
- Client (browser or mobile) sends a request
- API acts as a communication bridge
- Backend processes the request
- Database stores or retrieves data
- Response is sent back to the client

✔ Multiple backends can connect to one database  
✔ Backend can communicate with third-party APIs  

---

## 3. JavaScript-Based Backend

A JavaScript backend is responsible for:
- Handling API requests
- Database operations
- File handling
- Authentication & authorization
- Third-party API integration

### Data Sources
- Database
- Files
- External APIs (payment, email, maps, etc.)

---

## 4. JavaScript Runtime Environment

JavaScript runs on the server using a **runtime environment**.

Popular runtimes:
- **Node.js** (most widely used)
- Deno
- Bun

### Node.js Features
- Non-blocking I/O
- Event-driven architecture
- High performance and scalability

---

## 5. Configuration & Project Files

### package.json
- Project metadata
- Dependency management
- Script definitions

---

### .env
Stores environment variables securely.

Example:
```env
PORT=5000
DB_URL=mongodb://localhost:27017/app
JWT_SECRET=supersecret

### Other Important Files
-README.md – project documentation
-.gitignore – ignored files
-ESLint / Prettier – code formatting

6. Standard Backend Folder Structure
src/
│
├── index.js
├── app.js
├── constants/
├── config/
├── db/
├── models/
├── controllers/
├── routes/
├── middlewares/
├── utils/
└── more/

7. Folder Responsibilities
index.js (Entry Point)

Application startup

Database connection

Server listening

app.js

App configuration

Middleware setup

JSON & URL encoded parsing

Cookie configuration

constants/

Stores:

Enums

Database names

Roles (ADMIN, USER)

db/

Database connection logic

MongoDB / SQL setup

models/

Data schema definitions

Structure of database documents/tables

controllers/

Business logic

Handles request & response

routes/

API endpoint definitions

Connects routes to controllers

Example:

POST /signup
POST /login
GET  /users

middlewares/

Runs before controllers:

Authentication

Authorization

Validation

Logging

utils/

Reusable helper functions:

Email service

File upload

OTP generation

Utility helpers

more/

Optional advanced features:

Cron jobs

External integrations

Microservices

Feature-specific modules

8. Request Flow Example
Client → Route → Middleware → Controller → Model → Database

9. Key Takeaways

Backend = Logic + Data

API connects client and server

Clean structure improves scalability

Middleware enhances security

Utilities keep code reusable

10. Best Practices

Keep controllers thin

Use environment variables

Validate all inputs

Handle errors globally

Follow REST standards