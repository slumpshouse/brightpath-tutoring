# BrightPath Tutoring – App Features

## Core Features

### 1. Student Login

Students can log into the app using their email and password.

**Purpose:**
Allows students to securely access their account, lessons, and quiz results.

---

### 2. View Lessons

Students can browse and view math and science lesson content.

**Purpose:**
Ensures students can access learning materials anytime, from any device.

---

### 3. Take Quizzes

Students can take quizzes after completing lessons. Answers are saved immediately to the database.

**Purpose:**
Helps measure understanding, track academic progress, and prevents lost work if the page refreshes.

---

### 4. Track Progress

Students can see their quiz scores and completed lessons on a progress page.

**Purpose:**
Allows students and teachers to monitor improvement over time and reduces manual grade tracking.

---

### 5. Profile Dashboard

Students have a personal dashboard showing their name, grade level, completed lessons, and quiz scores.

**Purpose:**
Gives students a central starting point to manage their learning every time they log in.

---

## System Needs

### 1. Database Connectivity

The app must connect to a PostgreSQL database to store student accounts, lesson data, and quiz results.

---

### 2. Secure Authentication

Passwords must be hashed and stored securely. Credentials must not be exposed in the system or in version control.

---

### 3. Containerized Environment

The application must run inside Docker to ensure it works the same on every developer's machine and in production. The app and database must start correctly together using Docker Compose.