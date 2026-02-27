# BrightPath Tutoring

## Project Overview

BrightPath Tutoring is a web-based tutoring platform designed to help K–12 students access lessons, take quizzes, and track their academic progress. Many students, especially in underserved communities, lack consistent access to quality tutoring outside the classroom. BrightPath solves this by providing an always-available, easy-to-use application where students can log in, study lesson content in math and science, complete quizzes, and monitor their improvement over time.

The application is built with Next.js and backed by a PostgreSQL database managed through Prisma ORM, all containerized with Docker to ensure a consistent and reliable deployment experience.

---

## Quick Start

**Build the Docker image:**

```bash
docker build -t brightpath-app .
```

**Run the application with Docker Compose (app + database):**

```bash
docker compose up --build
```

The app will be available at [http://localhost:3000](http://localhost:3000).

**Stop the application:**

```bash
docker compose down
```

---

## Architecture

BrightPath uses a multi-container Docker architecture managed by Docker Compose:

- **App Container** — Runs the Next.js application built from a multistage Dockerfile. The builder stage installs dependencies and compiles the app, while the production stage contains only the minimal standalone output. This keeps the final image small and secure.
- **Database Container** — Runs PostgreSQL 15 to store student accounts, lesson data, and quiz results. A health check ensures the database is ready before the app connects.

The Dockerfile uses a **multistage build** strategy:

1. **Builder stage** (`node:20-alpine`): Installs pnpm, runs dependency installation, and builds the Next.js app with `output: "standalone"`.
2. **Production stage** (`node:20-alpine`): Copies only the compiled standalone server, static assets, and public files. No source code or `node_modules` are included, resulting in a much smaller and more secure image.

---

## Business Value

Docker containerization is critical for student-facing educational technology like BrightPath:

- **Eliminates "works on my machine" problems** — Every developer, tester, and deployment environment runs the exact same container image. A student in Philadelphia sees the same working app as a developer testing locally.
- **Consistent builds** — The multistage Dockerfile ensures the production image is built the same way every time, reducing bugs caused by environment differences.
- **Faster onboarding** — New team members can run `docker compose up` and have the full app and database running in minutes, with no manual setup.
- **Reliable deployments** — Since the container packages everything the app needs, deployments to staging or production are predictable and repeatable.

For an educational platform where students depend on the app for homework and quizzes, reliability is essential. Docker ensures that what works in development will work in production.

---

## Tech Stack

| Technology   | Purpose                                      |
| ------------ | -------------------------------------------- |
| Next.js 16   | React-based web framework (frontend + API)   |
| TypeScript   | Type-safe JavaScript                         |
| PostgreSQL   | Relational database for student data         |
| Prisma ORM   | Database access and schema management        |
| Docker       | Containerization for consistent environments |
| Docker Compose | Multi-container orchestration              |
| Tailwind CSS | Utility-first CSS framework                  |
| Node.js 20   | JavaScript runtime                           |

