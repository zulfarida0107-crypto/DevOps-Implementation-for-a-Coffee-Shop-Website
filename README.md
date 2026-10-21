# ☕ DevOps Implementation for a Coffee Shop Website

A containerized web application infrastructure project demonstrating DevOps practices, multi-container orchestration using Docker, Nginx web server configuration, PHP-FPM integration, MySQL database management, and automated CI/CD workflows via GitHub Actions.

---

## 🛠️ Tech Stack & Environment

- **Containerization & Orchestration:** Docker Desktop, Docker Compose
- **Web Server & PHP:** Nginx, PHP 8.2-FPM
- **Database:** MySQL 8.0, phpMyAdmin
- **CI/CD Pipeline:** GitHub Actions (`runner.yml`)
- **Operating System & Environment:** Windows 11 Home, WSL (Ubuntu / Debian)

---

## 📄 Project Documentation

[DevOps-Implementation-for-a-Coffee-Shop-Website-Paper (PDF)](./DevOps-Implementation-for-a-Coffee-Shop-Website-Paper.pdf)

[DevOps-Implementation-for-a-Coffee-Shop-Website-Runner (PDF)](./DevOps-Implementation-for-a-Coffee-Shop-Website-Paper-Runner.pdf)

---

## 🚀 Infrastructure & DevOps Architecture

The project implements a decoupled multi-container architecture using Docker Compose:
- **Nginx (`Dockerfile.nginx` & `default.conf`):** Serves as the high-performance web server handling HTTP requests on port `1234` and routing PHP scripts via FastCGI to PHP-FPM.
- **PHP-FPM (`Dockerfile`):** Custom PHP environment container configured with MySQL extensions (`mysqli`, `pdo`, `pdo_mysql`) running on port `9000`.
- **MySQL Database (`db_kantin` / `db_museum`):** Persistent database server running on port `3308` with automated data volumes.
- **phpMyAdmin:** Web-based database management tool accessible via port `8086`.
- **GitHub Actions (`runner.yml`):** Automated workflow configuration to handle repository integration and build processes.
