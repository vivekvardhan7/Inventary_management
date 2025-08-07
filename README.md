# 🚀 Airbus Inventory Management System

A full-stack Inventory Management System built with **Spring Boot** and **Angular**, enabling secure product management with JWT authentication and RESTful APIs.

---

## 📌 Features

- ✅ Login & Authentication (JWT-based)
- 📦 CRUD operations on products
- 🔐 Secured APIs with token validation
- 📊 Angular frontend with:
  - Product table display
  - Filters & search by category
  - Add / Edit / Delete products
- ⚠️ Custom error handling for better API responses

---

## 🛠️ Tech Stack

**Backend:**
- Java
- Spring Boot (MVC, JDBC)
- MySQL
- JWT (Security)
- Maven

**Frontend:**
- Angular 12+
- Angular Material UI
- Bootstrap
- HTML5, CSS3

---

## 🎯 REST API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| `POST` | `/airbusManagement/JWT/authenticateUser` | Login using username & password |
| `GET` | `/airbusManagement/getAllProducts` | Get all products |
| `GET` | `/airbusManagement/getProductsByCategory/{category}` | Get products by category |
| `POST` | `/airbusManagement/addProduct` | Add a new product |
| `POST` | `/airbusManagement/updateProduct/{productId}` | Update existing product |
| `DELETE` | `/airbusManagement/deleteProduct/{productId}` | Delete a product |

> ⚠️ All routes (except login) require an `Authorization: Bearer <JWT>` header.

---

## 🔑 Default Login Credentials
Username: airbus02@gmail.com
Password: 1234

yaml
Copy
Edit

---

## 🧪 How to Run the Project

### 🔁 Backend Setup (Spring Boot)

1. Clone the repository:
   ```bash
   git clone https://github.com/vivekvardhan7/Inventary_management.git
   cd Inventary_management
Create MySQL database and tables:

sql
Copy
Edit
CREATE DATABASE Product;

USE Product;

CREATE TABLE Product (
  productId VARCHAR(256) UNIQUE NOT NULL,
  productName VARCHAR(256),
  productDescription VARCHAR(3500),
  productCategory VARCHAR(256),
  units INT
);

CREATE TABLE User (
  username VARCHAR(256),
  password VARCHAR(256)
);

INSERT INTO User(username, password)
VALUES
  ("airbus01@gmail.com", "$2a$10$slYQmyNdGzTn7ZLBXBChFOC9f6kFjAqPhccnP6DxlWXx2lPk1C3G6"),
  ("airbus02@gmail.com", "$2a$10$ZnnAdfh3cc7a/b1aODLeoOjifNPbHL6Vo8kpRJj.muPsVp1697hJO");
In application.properties, configure your local MySQL credentials.

Run the Spring Boot app:

bash
Copy
Edit
./mvnw spring-boot:run
🌐 Frontend Setup (Angular)
Navigate to the Angular project directory:

bash
Copy
Edit
cd AirbusInventory
Install dependencies:

bash
Copy
Edit
npm install
Run the frontend app:

bash
Copy
Edit
ng serve
Access the application at: http://localhost:4200

📋 Project Structure
pgsql
Copy
Edit
Inventory-Management-System/
│
├── Spring (Backend)
│   ├── src/
│   │   └── main/
│   │       ├── java/
│   │       └── resources/
│   │           └── schema.sql
│   └── pom.xml
│
├── AirbusInventory (Frontend)
│   └── src/
│       ├── app/
│       └── assets/
│
└── README.md
📌 Notes
Encrypted passwords are handled using BCrypt for enhanced security.

Make sure MySQL service is running locally before launching the Spring Boot app.

schema.sql is also available under: src/main/resources/schema.sql.

🤝 Contributing
Fork the repository.

Create your feature branch: git checkout -b feature/YourFeature

Commit your changes: git commit -m 'Add some feature'

Push to the branch: git push origin feature/YourFeature

Open a Pull Request.

📧 Contact
Made by Sai Vivek 

✉️ saivivek2809@gmail.com



