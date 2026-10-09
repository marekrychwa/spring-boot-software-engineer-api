# Software Engineer Management API

A RESTful API built with **Spring Boot 3** for managing software engineer data, integrated with a **PostgreSQL** database running inside a **Docker** container.

## 🛠️ Tech Stack

- **Java 21**
- **Spring Boot 3** (Spring Data JPA, Spring Web)
- **PostgreSQL**
- **Docker & Docker Compose**
- **Maven**

## 🏗️ Architecture

The application follows the standard **Three-Layer Architecture**:
1. **Controller Layer** (`SoftwareEngineerController`) – Handles HTTP requests and exposes REST endpoints.
2. **Service Layer** (`SoftwareEngineerService`) – Contains business logic.
3. **Repository Layer** (`SoftwareEngineerRepository`) – Manages database communication via Spring Data JPA.

## 🚀 Getting Started

### Prerequisites
- Java 21 or higher
- Docker Desktop

### 1. Run the Database in Docker
```bash
docker compose up -d
```

### 2. Run the Application
```bash
./mvnw spring-boot:run
```
## 📡 API Endpoints

| Method | Endpoint | Description |
| :--- | :--- | :--- |
| `GET` | `/api/v1/software-engineers` | Retrieves a list of all software engineers |
| `GET` | `/api/v1/software-engineers/{id}` | Retrieves a specific software engineer by ID |
| `POST` | `/api/v1/software-engineers` | Adds a new software engineer to the database |

### Example JSON Body for `POST` Request:

```json
{
  "name": "Marek",
  "techStack": "java, spring boot, docker"
}
```


Tip: You can use the requests.http file included in the project to test all endpoints directly from IntelliJ IDEA.



