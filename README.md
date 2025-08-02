# 🎓 Institute Management System

A web-based application developed using **Servlets**, **JSP**, and **JDBC** to manage records of students, courses, and staff in an educational institute.

---

## ✅ Features

- Add, update, delete student records
- Assign students to specific courses
- View list of students and staff
- Basic authentication (optional)
- Database integration using JDBC

---

## 🛠 Tech Stack

- Java (Servlets, JSP)
- JDBC (MySQL)
- HTML, CSS, Bootstrap (UI)
- Apache Tomcat Server
- MySQL Database

---

## 🧱 Project Structure
InstituteManagementSystem/
├── src/main/java
│ ├── com/institute
│ │ └── MyServlet.java
│ ├── com/institute/model/
│ │ └── dao.java
│ ├── com/institute/bean/
│ │ └── Student.java
│ │ └── User.java
├── src/main/webapp/
│ ├── WEB-INF/
│ │ ├── lib/
│ │ │ ├── mysql-connector-j-8.3.0.jar
│ │ ├── web.xml
│ └── delete.jsp
│ └── display.jsp
│ └── home.jsp
│ └── login.jsp
│ └── register.jsp
│ └── studentform.jsp
│ └── update.jsp

---

## 💾 Database Setup

1. Create a MySQL database:
```sql
CREATE DATABASE mvc;  #mvc i named you can give your name and remember to change in dao class.
use mvc;

2. Create 2 tables:
- Table to store user login credentials
CREATE TABLE user (
    uid INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(20),
    email VARCHAR(20) UNIQUE,
    password VARCHAR(30)
);

-- Table to store student information
CREATE TABLE student (
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(20),
    age INT,
    mobile BIGINT UNIQUE,
    address VARCHAR(50),
    email VARCHAR(20) UNIQUE,
    course VARCHAR(20)
);

---


⚙️JDBC Configuration
Update DB credentials in dao.java:

java
Copy code
String jdbcURL = "jdbc:mysql://localhost:3306/mvc";
String jdbcUsername = "root";
String jdbcPassword = "yourpassword";

---

▶️ How to Run
1. Import the project into Eclipse as a Dynamic Web Project
2. Configure Apache Tomcat server
3. Deploy and run the project on the server
4. Access app via: http://localhost:8080/InstituteManagementSystem/

---

👩‍💻 Author
Zaiba Khanum G N
GitHub: @zaib9112002
