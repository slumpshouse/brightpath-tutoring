# BrightPath Tutoring – App Features

## Core Features

### 1. Student Login

Students can log into the app using their email and password.

**Purpose:**

Allows students to securely access their account, lessons, and quiz results.

---

### 2. View Lessons

Students can view math and science lesson videos.

**Purpose:**

Ensures students can access learning materials anytime.

---

### 3. Take Quizzes

Students can take quizzes after completing lessons.

**Purpose:**

Helps measure understanding and track academic progress.

---

### 4. Track Progress

Students can see their quiz scores and completed lessons.

**Purpose:**

Allows students and teachers to monitor improvement over time.

---

### 5. Profile Dashboard

Students have a personal dashboard showing:

- Name
- Grade level
- Completed lessons
- Quiz scores

**Purpose:**

Gives students a central place to manage their learning.

---

## System Needs

### 1. Database Connectivity

The app must connect to a PostgreSQL database to store student accounts and quiz results.

---

### 2. Secure Authentication

Passwords must be stored securely and not exposed in the system.

---

### 3. Reliable Server Startup

The application and database must start correctly together using Docker Compose.

## Core Features

### 1. Student Login System

**Description:**

Students can log in securely using an email and password.

**Why It Helps:**

Prevents unauthorized access and ensures students can reliably access their homework and quizzes.

**Business Impact:**

Reduces login-related support tickets and prevents account confusion.

---

### 2. Dashboard Page

**Description:**

After logging in, students see a dashboard with their lessons and progress.

**Why It Helps:**

Gives students a consistent starting point every time they log in.

**Business Impact:**

Prevents confusion and improves user experience across different computers.

---

### 3. Quiz Submission & Saving

**Description:**

When a student completes a quiz, their answers are saved immediately to the database.

**Why It Helps:**

Prevents quizzes from disappearing if the page refreshes or crashes.

**Business Impact:**

Builds trust and prevents lost homework complaints.

---

### 4. Progress Tracking

**Description:**

Students can see completed lessons and quiz scores.

**Why It Helps:**

Keeps learning progress organized and easy to review.

**Business Impact:**

Teachers can track grades more easily and reduce manual work.

---

### 5. Error Message Display

**Description:**

If something goes wrong (e.g., server error), the app shows a clear error message instead of crashing.

**Why It Helps:**

Users know something is wrong instead of thinking the app is broken.

**Business Impact:**

Reduces frustration and improves professionalism.

---

# System Needs 

### 1. Database Connection

The application must connect to a PostgreSQL database to store student accounts and quiz data.

---

### 2. Containerized Environment

The application must run inside Docker to ensure it works the same on every computer.

---

### 3. Automated Build Testing (CI)

The system must automatically build and test the application when new code is pushed to prevent broken updates.