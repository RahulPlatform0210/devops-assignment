# DevOps Assignment

## Overview

This project demonstrates deployment and production setup of a backend application using containerized infrastructure and CI/CD practices.

The application is built using FastAPI and deployed using Docker Compose with PostgreSQL, Redis, and NGINX reverse proxy.

The objective was to simulate a production-oriented environment covering deployment automation, service orchestration, logging, health monitoring, and infrastructure organization.

---

## Tech Stack

- FastAPI
- Docker
- Docker Compose
- PostgreSQL
- Redis
- NGINX
- GitHub Actions

---

## Project Architecture

Client Request

↓

NGINX Reverse Proxy

↓

FastAPI Backend Service

↓

PostgreSQL Database

↓

Redis Cache Layer

Infrastructure managed through Docker Compose

CI/CD implemented using GitHub Actions

---

## Services Used

| Service | Purpose | Port |
|----------|----------|------|
| FastAPI | Backend API | 8000 |
| PostgreSQL | Database | 5432 |
| Redis | Cache Service | 6379 |
| NGINX | Reverse Proxy | 80 |

---

## Running the Application

Clone repository:

```bash
git clone <repository-url>

cd devops-assignment
```

Start containers:

```bash
docker compose up --build -d
```

Check running services:

```bash
docker compose ps
```

Check logs:

```bash
docker compose logs
```

---

## Health Endpoint

Health verification endpoint:

```bash
http://localhost/health
```

Response:

```json
{
 "status":"healthy"
}
```

---

## Docker Setup

Application infrastructure includes:

- FastAPI container
- PostgreSQL container
- Redis container
- NGINX reverse proxy container

Docker Compose handles service orchestration and dependency management.

---

## CI/CD Pipeline

GitHub Actions pipeline configured for:

- Dependency installation
- Docker image validation
- Docker Compose validation

Pipeline execution triggers:

- Push events
- Pull Requests

---

## Logging

Application logs can be verified using:

```bash
docker compose logs
```

Logs available for:

- FastAPI
- PostgreSQL
- Redis
- NGINX

---

## Security Considerations

Implemented:

- Environment variable usage
- Secret exclusion using .gitignore
- Reverse proxy setup using NGINX
- Container isolation

Production recommendations:

- Firewall configuration
- SSL certificates
- Secret management
- Restricted network exposure

---

## SSL Approach

SSL can be configured using:

- NGINX SSL termination
- Let's Encrypt certificates

Current setup prepared for SSL integration.

---

## Backup Strategy

PostgreSQL volume persistence enabled.

Recommended backup approach:

```bash
pg_dump -U admin devopsdb > backup.sql
```

Suggested backup frequency:

- Daily database backup
- Periodic backup validation

---

## Restart Strategy

Docker Compose service recovery mechanism used.

Container health checks configured to improve reliability.

---

## Deployment Verification

Verify application:

```bash
http://localhost
```

Verify health endpoint:

```bash
http://localhost/health
```

Verify containers:

```bash
docker compose ps
```

---

## Deliverables Completed

- Dockerized FastAPI application
- Docker Compose setup
- PostgreSQL integration
- Redis integration
- NGINX reverse proxy
- GitHub Actions CI/CD
- Environment variable configuration
- Health monitoring endpoint
- Logging strategy
- Deployment documentation
- Architecture documentation

---

Project developed as part of DevOps Engineer technical assignment.