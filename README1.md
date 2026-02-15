# QuizMaster Pro 🧠

A full-featured quiz management system built with Angular, designed for educational institutions and trainers to create, manage, and evaluate quizzes with ease.

## 📋 Table of Contents
- [Overview](#overview)
- [Key Features](#key-features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage Guide](#usage-guide)
- [API Integration](#api-integration)
- [Testing](#testing)
- [Build & Deployment](#build--deployment)
- [Contributing](#contributing)
- [License](#license)

## 🔍 Overview

QuizMaster Pro is a scalable Angular application that provides a complete quiz management solution. It features separate dashboards for administrators and regular users, secure authentication, and real-time quiz evaluation. The application follows Angular best practices with modular architecture, lazy loading, and comprehensive route protection.

## ✨ Key Features

### 🔐 Authentication Module
- User registration and login with JWT
- Password encryption and secure storage
- Session management with token refresh
- Role-based access control (Admin/User)

### 👑 Admin Dashboard
- **Category Management**: Create, edit, delete quiz categories
- **Question Bank**: 
  - Add multiple choice questions
  - Set correct answers and explanations
  - Upload images with questions
  - Configure difficulty levels
- **Quiz Builder**:
  - Set time limits and passing criteria
  - Randomize question order
  - Schedule quiz availability
  - View analytics and statistics
- **User Management**: View and manage registered users
- **Result Analysis**: Export results in CSV/PDF format

### 👤 User Portal
- **Available Quizzes**: Browse and attempt assigned quizzes
- **Quiz Interface**:
  - Real-time timer countdown
  - Question navigation panel
  - Mark for review functionality
  - Progress indicator
- **Instant Results**: Auto-graded with detailed feedback
- **Performance History**: Track past attempts and scores
- **Profile Management**: Update personal details and password

### ⚡ Technical Features
- Lazy loading for optimized performance
- HTTP interceptors for token management
- Reactive forms with custom validators
- Route guards for protected views
- Shared components for reusability
- Custom pipes for data transformation
- Error handling with user-friendly messages

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| Angular 15+ | Frontend framework |
| TypeScript 4.8+ | Programming language |
| RxJS 7.5+ | Reactive programming |
| Bootstrap 5 | UI styling |
| Font Awesome | Icons |
| JWT | Authentication |
| Jasmine/Karma | Unit testing |

## 📁 Project Structure
quiz-master-pro/
├── src/
│ ├── app/
│ │ ├── components/
│ │ │ ├── footer/
│ │ │ │ ├── footer.component.ts
│ │ │ │ ├── footer.component.html
│ │ │ │ └── footer.component.css
│ │ │ └── navbar/
│ │ │ ├── navbar.component.ts
│ │ │ ├── navbar.component.html
│ │ │ └── navbar.component.css
│ │ │
│ │ ├── pages/
│ │ │ ├── admin/
│ │ │ │ ├── dashboard/
│ │ │ │ ├── categories/
│ │ │ │ ├── questions/
│ │ │ │ ├── quizzes/
│ │ │ │ └── results/
│ │ │ ├── home/
│ │ │ ├── login/
│ │ │ ├── profile/
│ │ │ ├── signup/
│ │ │ └── user/
│ │ │ ├── dashboard/
│ │ │ ├── quiz-attempt/
│ │ │ └── history/
│ │ │
│ │ ├── services/
│ │ │ ├── auth/
│ │ │ │ ├── login.service.ts
│ │ │ │ └── login.service.spec.ts
│ │ │ ├── guards/
│ │ │ │ ├── admin.guard.ts
│ │ │ │ ├── admin.guard.spec.ts
│ │ │ │ ├── user.guard.ts
│ │ │ │ └── user.guard.spec.ts
│ │ │ ├── interceptors/
│ │ │ │ └── authinterceptor.ts
│ │ │ ├── category.service.ts
│ │ │ ├── category.service.spec.ts
│ │ │ ├── question.service.ts
│ │ │ ├── question.service.spec.ts
│ │ │ ├── quiz.service.ts
│ │ │ ├── quiz.service.spec.ts
│ │ │ ├── result.service.ts
│ │ │ ├── result.service.spec.ts
│ │ │ ├── user.service.ts
│ │ │ └── user.service.spec.ts
│ │ │
│ │ ├── models/
│ │ │ ├── category.ts
│ │ │ ├── category.spec.ts
│ │ │ ├── question.ts
│ │ │ ├── question.spec.ts
│ │ │ ├── quiz.ts
│ │ │ ├── quiz.spec.ts
│ │ │ ├── result.ts
│ │ │ ├── result.spec.ts
│ │ │ ├── user.ts
│ │ │ ├── user.spec.ts
│ │ │ ├── userqna.ts
│ │ │ └── userqna.spec.ts
│ │ │
│ │ ├── shared/
│ │ │ ├── helper.ts
│ │ │ └── constants.ts
│ │ │
│ │ ├── app-routing.module.ts
│ │ ├── app.module.ts
│ │ ├── app.component.ts
│ │ ├── app.component.html
│ │ ├── app.component.css
│ │ └── app.component.spec.ts
│ │
│ ├── assets/
│ │ ├── images/
│ │ └── icons/
│ │
│ ├── environments/
│ │ ├── environment.ts
│ │ └── environment.prod.ts
│ │
│ ├── index.html
│ ├── main.ts
│ └── styles.css
│
├── .editorconfig
├── .gitignore
├── angular.json
├── package.json
├── README.md
└── tsconfig.json


## 💻 Installation

### Prerequisites
- Node.js (v16 or higher)
- npm (v8 or higher)
- Angular CLI (v15+)

### Step-by-Step Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/quiz-master-pro.git
   cd quiz-master-pro
   ```
2. Install dependencies
   npm install

3. Install Angular CLI globally (if not installed)
   npm install -g @angular/cli

4. Start the development server
   ng serve

5. Navigate to http://localhost:4200

## 🚀 Usage Guide
Running the Application
# Development server with hot reload
ng serve

# Development server on specific port
ng serve --port 4200 --open

# Build for production
ng build --prod

# Run unit tests
ng test

# Run e2e tests
ng e2e

Default Credentials
Role	Email	Password
Admin	admin@quiz.com	Admin@123
User	user@quiz.com	User@123

##🔌 API Integration
The application expects a REST API with the following endpoints:

### Authentication
POST /api/auth/login - User login
POST /api/auth/register - User registration
POST /api/auth/refresh - Refresh token
POST /api/auth/logout - User logout

### Categories
GET /api/categories - Get all categories
POST /api/categories - Create category
PUT /api/categories/:id - Update category
DELETE /api/categories/:id - Delete category

### Questions
GET /api/questions - Get questions (with filters)
POST /api/questions - Create question
PUT /api/questions/:id - Update question
DELETE /api/questions/:id - Delete question

### Quizzes
GET /api/quizzes - Get all quizzes
GET /api/quizzes/active - Get active quizzes
POST /api/quizzes - Create quiz
POST /api/quizzes/:id/start - Start quiz attempt
POST /api/quizzes/:id/submit - Submit quiz answers

### Results
GET /api/results/user - Get user results
GET /api/results/quiz/:quizId - Get quiz results (admin)
GET /api/results/:resultId - Get specific result

### Users
GET /api/users/profile - Get user profile
PUT /api/users/profile - Update profile
PUT /api/users/change-password - Change password

## 🧪 Testing
Unit Tests

# Run all tests
ng test

# Run tests with coverage
ng test --code-coverage

# Run specific test file
ng test --include=**/user.service.spec.ts

