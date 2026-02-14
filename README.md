# 🎓 Quiz Portal Backend Application
> 🚀 A Production-Ready Spring Boot Backend for Online Examination Systems

![Java](https://img.shields.io/badge/Java-8%2B-orange)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-Backend-brightgreen)
![REST API](https://img.shields.io/badge/REST-API-blue)
![Status](https://img.shields.io/badge/Status-Completed-success)

---

## 📌 Overview

The **Quiz Portal Backend Application** is a **secure, scalable, and modular REST API** built using **:contentReference[oaicite:0]{index=0}**.  
It powers an **online quiz & examination system**, enabling administrators to manage quizzes and students to attempt them securely.

This project reflects **real-world backend development practices** and is suitable for:
- 🎓 Academic projects
- 💼 Backend developer interviews
- 🌐 GitHub portfolio showcase

---

## 💡 Project Motivation & Idea

### Why This Project?
I built this project to gain **hands-on experience with real backend systems**, focusing on:
- Authentication & authorization
- RESTful API design
- Database relationships
- Secure application architecture

Online exams are widely used in **education, hiring, and training platforms**, making this a practical and industry-relevant system.

### Idea Source
The idea was inspired by:
- Online learning platforms
- Digital examination systems
- Quiz-based evaluation tools

The goal was to simulate how a **real online exam backend** works internally.

---

## ✨ Key Features

### 🔐 Authentication & Security
- Role-based authentication
- Secure password encryption
- Protected APIs using Spring Security

### 🧑‍💼 Admin Features
- Create & manage quiz categories
- Add quizzes under categories
- Add and manage questions
- Activate / deactivate quizzes

### 🎓 Student Features
- View available quizzes
- Attempt quizzes
- Fetch quiz questions securely
- Submit quiz responses

---

## 🛠️ Technology Stack

### Backend
- **Spring Boot**
- Spring MVC (REST APIs)
- Spring Data JPA
- Spring Security
- Hibernate ORM

### Database
- MySQL

### Tools
- Java 8+
- Maven
- Postman (API testing)

---

## 🏗️ Application Architecture
Client (Frontend / Postman)
↓
Controller Layer
↓
Service Layer
↓
Repository Layer
↓
Database


✔ Follows **Layered Architecture**  
✔ Ensures separation of concerns  
✔ Easy to maintain & scale  

---

## 📁 Project Structure
src/main/java
└── com.exam
├── controller // REST Controllers
├── service // Business Logic Interfaces
├── service.impl // Business Logic Implementations
├── repository // JPA Repositories
├── model // Entity Classes
├── config // Configuration
├── security // Security Setup
└── ExamPortalApplication.java


---

## 🧬 Database Design (ER Diagram)

### Entities
- User
- Role
- Category
- Quiz
- Question

### Relationships
[ROLE] 1 -------- 1 [USER]

[CATEGORY] 1 -------- * [QUIZ]

[QUIZ] 1 -------- * [QUESTION]


✔ Normalized database  
✔ Minimal redundancy  
✔ Clear relationships  

---

## 📐 UML Diagrams (Textual Explanation)

### 📘 Class Diagram
- Each entity maps to a database table
- Service & controller layers interact cleanly
- Repository layer handles persistence

### 🔄 Sequence Diagram (Login Flow)
User → Controller → Service → Security → Database ← JWT Token ←


### 👥 Use Case Diagram
**Admin**
- Login
- Manage categories
- Manage quizzes
- Add questions

**Student**
- Login
- View quizzes
- Attempt quiz
- Submit answers

---

## 🔄 Application Flow

### Admin Flow
1. Admin logs in
2. Creates categories
3. Adds quizzes
4. Adds questions
5. Activates quizzes

### Student Flow
1. Student logs in
2. Views quizzes
3. Attempts quiz
4. Submits answers
5. Receives result

---

## 🔗 REST API Endpoints (Sample)

### Authentication
POST /generate-token
POST /user/


### Category
POST /category/
GET /category/
PUT /category/
DELETE /category/{cid}


### Quiz
POST /quiz/
GET /quiz/
GET /quiz/category/{cid}
DELETE /quiz/{qid}


### Question
POST /question/
GET /question/quiz/{qid}


---

## ▶️ How to Run the Project

### 1️⃣ Prerequisites
- Java 8+
- MySQL
- Maven

### 2️⃣ Database Configuration
```properties
spring.datasource.url=jdbc:mysql://localhost:3306/exam_portal
spring.datasource.username=root
spring.datasource.password=your_password

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true

### 3️⃣ Run Application
mvn clean install
mvn spring-boot:run

Server runs at: http://localhost:8080

🔐 Security Implementation

Role-based access control

Encrypted passwords

Restricted endpoints

Secure API communication

User Request
   ↓
Controller
   ↓
Service
   ↓
Repository
   ↓
Database
   ↑
Response

🚀 Future Enhancements

Result analytics & reports

Quiz timer auto-submit

Swagger API documentation

Docker & cloud deployment

Pagination & filtering

🎯 Use Cases

Online examinations

Practice tests

Recruitment assessments

Educational platforms

🧾 Conclusion

This Quiz Portal Backend Application demonstrates:

Real-world backend development

Secure system design

Clean architecture

Industry-standard technologies
