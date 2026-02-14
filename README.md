<h1 align="center">🎓 Quiz Portal Backend Application</h1>
<p align="center">
  <strong>A Production-Ready Spring Boot Backend for Online Examination Systems</strong>
</p>

<div align="center">

<!-- Colorful Badges -->
<img src="https://img.shields.io/badge/Java-17-orange?style=flat-square&logo=java&logoColor=white" alt="Java 17">
<img src="https://img.shields.io/badge/Spring%20Boot-3.1-brightgreen?style=flat-square&logo=springboot&logoColor=white" alt="Spring Boot">
<img src="https://img.shields.io/badge/Spring%20Security-6.1-blue?style=flat-square&logo=springsecurity&logoColor=white" alt="Spring Security">
<img src="https://img.shields.io/badge/MySQL-8.0-blue?style=flat-square&logo=mysql&logoColor=white" alt="MySQL">
<img src="https://img.shields.io/badge/Maven-C2A120?style=flat-square&logo=apachemaven&logoColor=white" alt="Maven">
<img src="https://img.shields.io/badge/Status-Ready-success?style=flat-square" alt="Status">

</div>

<hr>

## 📌 Overview

The **Quiz Portal Backend Application** is a secure, scalable, and modular REST API built using **Spring Boot**. It powers an online quiz & examination system, enabling administrators to manage quizzes and students to attempt them securely.

This project reflects real-world backend development practices and is suitable for:
- 🎓 **Academic projects**
- 💼 **Backend developer interviews**
- 🌐 **GitHub portfolio showcase**

## 💡 Project Motivation & Idea

**Why This Project?**  
I built this project to gain hands-on experience with real backend systems, focusing on:
- Authentication & authorization
- RESTful API design
- Database relationships
- Secure application architecture

**Idea Source**  
Inspired by online learning platforms, digital examination systems, and quiz-based evaluation tools. The goal was to simulate how a real online exam backend works internally.

## ✨ Key Features

<div align="center">

| 🔐 Authentication & Security | 🧑‍💼 Admin Features | 🎓 Student Features |
| :--- | :--- | :--- |
| Role-based authentication | Create & manage quiz categories | View available quizzes |
| Secure password encryption | Add quizzes under categories | Attempt quizzes |
| Protected APIs using Spring Security | Add and manage questions | Fetch quiz questions securely |
| | Activate / deactivate quizzes | Submit quiz responses |

</div>

## 🛠️ Technology Stack

<div align="center">

| **Category** | **Technologies** |
| :--- | :--- |
| **Backend** | Spring Boot, Spring MVC, Spring Data JPA, Spring Security, Hibernate ORM |
| **Database** | MySQL |
| **Tools** | Java 17+, Maven, Postman |

</div>

## 🏗️ Application Architecture

The application follows a **Layered Architecture** for separation of concerns and maintainability.


## 📁 Project Structure
📦 src/main/java/com.exam
┣ 📂 controller // REST Controllers
┣ 📂 service // Business Logic Interfaces
┣ 📂 service.impl // Business Logic Implementations
┣ 📂 repository // JPA Repositories
┣ 📂 model // Entity Classes
┣ 📂 config // Configuration
┣ 📂 security // Security Setup
┗ 📜 ExamPortalApplication.java


## 🧬 Database Design (ER Diagram)

**Entities:**
- `User`
- `Role`
- `Category`
- `Quiz`
- `Question`

**Relationships:**
- `[ROLE] 1 -------- 1 [USER]`
- `[CATEGORY] 1 -------- * [QUIZ]`
- `[QUIZ] 1 -------- * [QUESTION]`

✔ Normalized database  
✔ Minimal redundancy  
✔ Clear relationships  

## 📐 UML Diagrams (Textual Representation)

### 📘 Class Diagram
Each entity maps to a database table. Service & controller layers interact cleanly, with repository layer handling persistence.

### 🔄 Sequence Diagram (Login Flow)
User → Controller → Service → Security → Database ← JWT Token ←

                ┌─────────────────────────────────────┐
                │         Online Exam System          │
                ├─────────────────────────────────────┤
                │  ┌─────────────────────────────┐   │
                │  │        Admin                │   │
                │  ├─────────────────────────────┤   │
                │  │ • Login                      │   │
                │  │ • Manage categories          │   │
                │  │ • Manage quizzes             │   │
                │  │ • Add questions              │   │
                │  └─────────────────────────────┘   │
                │  ┌─────────────────────────────┐   │
                │  │        Student              │   │
                │  ├─────────────────────────────┤   │
                │  │ • Login                      │   │
                │  │ • View quizzes               │   │
                │  │ • Attempt quiz               │   │
                │  │ • Submit answers             │   │
                │  └─────────────────────────────┘   │
                └─────────────────────────────────────┘


## 🔄 Application Flow

**Admin Flow:**
1. Admin logs in
2. Creates categories
3. Adds quizzes
4. Adds questions
5. Activates quizzes

**Student Flow:**
1. Student logs in
2. Views quizzes
3. Attempts quiz
4. Submits answers
5. Receives result

## 🔗 REST API Endpoints (Sample)

### 🔐 Authentication
| Method | Endpoint | Description |
| :--- | :--- | :--- |
| `POST` | `/generate-token` | Authenticate user and get JWT |
| `POST` | `/user/` | Register a new user |

### 📂 Category
| Method | Endpoint | Description |
| :--- | :--- | :--- |
| `POST` | `/category/` | Create a new category (Admin) |
| `GET` | `/category/` | Get all categories |
| `PUT` | `/category/` | Update a category (Admin) |
| `DELETE` | `/category/{cid}` | Delete a category (Admin) |

### 📝 Quiz
| Method | Endpoint | Description |
| :--- | :--- | :--- |
| `POST` | `/quiz/` | Create a new quiz (Admin) |
| `GET` | `/quiz/` | Get all quizzes |
| `GET` | `/quiz/category/{cid}` | Get quizzes by category |
| `DELETE` | `/quiz/{qid}` | Delete a quiz (Admin) |

### ❓ Question
| Method | Endpoint | Description |
| :--- | :--- | :--- |
| `POST` | `/question/` | Add a question (Admin) |
| `GET` | `/question/quiz/{qid}` | Get questions for a quiz (Student) |

## ▶️ How to Run the Project

### 1️⃣ Prerequisites
- Java 8+
- MySQL
- Maven

### 2️⃣ Database Configuration
Add to `application.properties`:
```properties
spring.datasource.url=jdbc:mysql://localhost:3306/exam_portal
spring.datasource.username=root
spring.datasource.password=your_password

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

### 3️⃣ Run Application
mvn clean install
mvn spring-boot:run
Server runs at: http://localhost:8181

### 🔐 Security Implementation
Role-based access control
Encrypted passwords (BCrypt)
Stateless authentication with JWT
Secured endpoints based on user roles

### User Request → JWT Filter → Authentication Manager → Controller → Response

### 🚀 Future Enhancements
📊 Result analytics & reports
⏱️ Quiz timer auto-submit
📖 Swagger API documentation
🐳 Docker & cloud deployment
📄 Pagination & filtering

### 🎯 Use Cases
🏫 Online examinations
📝 Practice tests
💼 Recruitment assessments
🎮 Educational platforms

### 🧾 Conclusion
This Quiz Portal Backend Application demonstrates:
✅ Real-world backend development
✅ Secure system design
✅ Clean architecture
✅ Industry-standard technologies

<hr><div align="center"> <p> <strong>📧 For questions or collaboration, feel free to reach out!</strong> </p> <p> <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white"> <img src="https://img.shields.io/badge/GitHub-100000?style=flat-square&logo=github&logoColor=white"> <img src="https://img.shields.io/badge/Gmail-D14836?style=flat-square&logo=gmail&logoColor=white"> </p> <p>⭐ If you found this project helpful, consider giving it a star on GitHub!</p> </div> ```
