# TalentTrakr – Employee Management System

A modern **full-stack web application** showcasing CRUD functionality with a **React.js frontend** and a **Spring Boot backend**. TalentTrakr offers a streamlined way to manage employee data via a responsive interface and a RESTful API.

##  Features
- **Full CRUD** operations on employee records – Create, Read, Update, Delete  
- **RESTful API** powered by Spring Boot and Spring Data JPA  
- Sleek, modern **React** UI with functional components, Hooks, React Router, and Axios  
- Persistent storage using **MySQL** with JPA/Hibernate  
- Responsive layout styled with **Bootstrap 4.5**

##  Tech Stack
- **Backend:** Spring Boot 2+, Spring Data JPA (Hibernate), MySQL, Maven, JDK 1.8+  
- **Frontend:** React.js, Axios, React Router, Bootstrap 4.5  

##  Prerequisites
- Java JDK 8 or higher  
- Node.js with npm  
- MySQL Server  
- Git

##  Installation Guide

### Clone the repository
```bash
git clone https://github.com/SiddheshKamthe/TalentTrakr-Employee-Management-System.git
cd TalentTrakr-Employee-Management-System
Backend Setup
Navigate to the backend/ directory.

Edit src/main/resources/application.properties to configure your MySQL settings:

properties
Copy code
spring.datasource.url=jdbc:mysql://localhost:3306/employees_db?useSSL=false&serverTimezone=UTC
spring.datasource.username=root
spring.datasource.password=your_password

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL8Dialect
Run the backend using Maven:

bash
Copy code
mvn spring-boot:run
Frontend Setup
Go to the frontend/ directory.

Install dependencies:

bash
Copy code
npm install
Launch the React development server:

bash
Copy code
npm start
Your application should now be live at http://localhost:3000, connecting to the backend running by default on port 8080.

Usage Overview
Users can interact with TalentTrakr to:

View all employees

Add a new employee

Edit employee details

Delete an employee

API Endpoints
Method	Endpoint	Description
GET	/api/employees	Get all employees
POST	/api/employees	Add a new employee
GET	/api/employees/{id}	Get employee by ID
PUT	/api/employees/{id}	Update an existing employee
DELETE	/api/employees/{id}	Delete an employee

All endpoints adhere to standard REST conventions, handling JSON request and response bodies.

Project Structure
css
Copy code
TalentTrakr-Employee-Management-System/
├── backend/
│   ├── src/main/java/
│   ├── src/main/resources/
│   └── pom.xml
├── frontend/
│   ├── public/
│   ├── src/
│   └── package.json
└── README.md
