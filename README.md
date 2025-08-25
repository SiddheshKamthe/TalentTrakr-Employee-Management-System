# TalentTrakr: Employee Management System

A full-stack CRUD application for managing employees, built with **React** (frontend) and **Spring Boot** (backend). It supports creating, listing, updating, deleting, and viewing employee records with a RESTful API and a MySQL database.

---

## Features

- **CRUD operations** for employee profiles (first name, last name, email)
- Backend layers: **Controller, Service, Repository** with Spring Data JPA
- **REST APIs** with custom exceptions and clean DTO-ready structure
- React UI with reusable components, routing, and **Axios-based API calls**
- Optional **pagination/sorting** via JPA repositories (extensible)

---

## Tech Stack

- **Languages:** Java, JavaScript, HTML, CSS
- **Frontend:** React, React Router, Axios
- **Backend:** Spring Boot, Spring Data JPA
- **Database:** MySQL
- **Build/Tools:** Maven, Node.js, npm, Git, GitHub, Spring DevTools
- **IDEs:** IntelliJ IDEA/Eclipse (backend), VS Code (frontend)

---

## Project Structure

```
root/
├─ backend/              # Spring Boot app (API, entities, repos, services, config)
│  ├─ src/main/java/...  # Controller, Service, Repository, Entity
│  └─ src/main/resources/application.properties
└─ frontend/             # React app (components, services, routes)
   └─ src/
      ├─ components/
      ├─ services/       # Axios client (EmployeeService)
      └─ App.jsx / Router setup
```

---

## Getting Started

### Prerequisites

- Java 17+
- Node.js 18+ and npm
- MySQL 8+
- Maven 3.8+

---

### Backend Setup

**1. Create database:**

- Name: `employee_management_system`

**2. Configure properties** (`backend/src/main/resources/application.properties`):

```
spring.datasource.url=jdbc:mysql://localhost:3306/employee_management_system
spring.datasource.username=YOUR_USERNAME
spring.datasource.password=YOUR_PASSWORD
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

**3. Run backend:**

```
mvn spring-boot:run
```

- API base URL: `http://localhost:8080/api/v1`

---

### Frontend Setup

**1. Install dependencies:**

```
cd frontend
npm install
```

**2. Configure API base URL** (e.g., `src/services/EmployeeService.js`):

```js
const API_BASE_URL = process.env.REACT_APP_API_BASE_URL || "http://localhost:8080/api/v1/employees";
```

**3. Start frontend:**

```
npm start
```

---

## API Endpoints

| Method | Endpoint                   | Description           |
|--------|----------------------------|-----------------------|
| GET    | `/api/v1/employees`        | List employees        |
| POST   | `/api/v1/employees`        | Create employee       |
| GET    | `/api/v1/employees/{id}`   | Get employee by ID    |
| PUT    | `/api/v1/employees/{id}`   | Update employee       |
| DELETE | `/api/v1/employees/{id}`   | Delete employee       |

- **Response format:** JSON

---

## UI Pages

- **Employee List:** Table view with actions (view, edit, delete)
- **Add/Update Employee:** Single reusable form component
- **View Employee:** Detail page

---

## Scripts

### Backend

- **Run:** `mvn spring-boot:run`
- **Build:** `mvn clean package`

### Frontend

- **Start:** `npm start`
- **Build:** `npm run build`

---

## Environment Variables

### Backend

- `spring.datasource.url`
- `spring.datasource.username`
- `spring.datasource.password`

### Frontend

- `REACT_APP_API_BASE_URL` (optional override for Axios)

---

## Testing (Optional)

- **Backend:** JUnit 5 + Spring Boot Test
- **API:** Postman collection for CRUD flows
- **Frontend:** React Testing Library

---

## Roadmap

- Add request/response DTOs and validation
- Enable pagination/sorting in UI
- Search/filter by name/email
- Docker for backend, frontend, and MySQL
- CI (GitHub Actions) for build/test
- Auth (Spring Security + JWT) with roles

---

## Contributing

Fork the repo, create a feature branch and open a PR with a clear description.

---


## Acknowledgments

Inspired by common React + Spring Boot CRUD architecture and community resources.
