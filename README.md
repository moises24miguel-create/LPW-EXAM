# LPW-EXAM

# Student Record Management System

A full-stack PHP & MySQL based Student Record Management System developed as part of a web development practical assignment.
This project demonstrates frontend, backend, database integration, AJAX operations, form validation, session management, and responsive UI design using Bootstrap 5 and jQuery.

---

# Features

## Authentication System

* Admin Login & Logout
* PHP Session Management
* Protected Routes

---

# Student Management

* Add Student
* View Students
* Edit Student Details
* Delete Student Record (AJAX)
* Live Search Functionality
* Column-wise Sorting

---

# Form Validation

## Client-Side Validation

Implemented using JavaScript & Regex:

* Name Validation
* Email Validation
* Phone Validation
* Date Validation
* Image Validation

## Server-Side Validation

Implemented using PHP:

* Secure Input Validation
* Prepared Statements
* File Upload Handling

---

# AJAX Features

* Fetch Student Records using AJAX
* Live Search without page reload
* Delete Record using AJAX
* Dynamic Table Rendering
* jQuery fadeIn() & fadeOut() Effects

---

# UI/UX Features

* Responsive Bootstrap 5 Layout
* Semantic HTML5 Structure
* Custom CSS Styling
* Card Hover Effects
* Fade-in Page Animation
* Bootstrap Modal Confirmation Dialog

---

# Technologies Used

| Technology  | Purpose                       |
| ----------- | ----------------------------- |
| HTML5       | Structure                     |
| CSS3        | Styling                       |
| Bootstrap 5 | Responsive Design             |
| JavaScript  | Client-side Logic             |
| jQuery      | DOM Manipulation & AJAX       |
| PHP         | Backend Development           |
| MySQL       | Database                      |
| AJAX        | Asynchronous Requests         |
| XAMPP       | Local Development Environment |

---

# Database Structure

## Database Name

```sql
student_db
```

---

# Tables

## students

| Column     | Type                     |
| ---------- | ------------------------ |
| id         | INT (PK, AUTO_INCREMENT) |
| name       | VARCHAR(100)             |
| email      | VARCHAR(150) UNIQUE      |
| phone      | VARCHAR(15)              |
| course     | VARCHAR(100)             |
| dob        | DATE                     |
| photo      | VARCHAR(255)             |
| created_at | TIMESTAMP                |

---

## admin_users

| Column   | Type                     |
| -------- | ------------------------ |
| id       | INT (PK, AUTO_INCREMENT) |
| username | VARCHAR(50)              |
| password | VARCHAR(255)             |

---

# Project Structure

```bash
project/
│
├── assets/
│   ├── css/
│   │   └── style.css
│   │
│   ├── js/
│   │   └── script.js
│
├── uploads/
│
├── includes/
│   ├── config.php
│   ├── auth.php
│   └── navbar.php
│
├── login.php
├── logout.php
├── index.php
├── add_student.php
├── view_students.php
├── edit_student.php
├── fetch_students.php
├── search_students.php
├── delete_student.php
└── README.md
```

---

# Installation Guide

## 1. Clone Repository

```bash
git clone https://github.com/your-username/student-record-system.git
```

---

## 2. Move Project to XAMPP htdocs

```bash
C:/xampp/htdocs/
```

---

## 3. Start XAMPP Services

Start:

* Apache
* MySQL

---

## 4. Create Database

Open:

* phpMyAdmin

Create database:

```sql
student_db
```

---

## 5. Import SQL Tables

```sql
CREATE TABLE students (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    email VARCHAR(150) UNIQUE,
    phone VARCHAR(15),
    course VARCHAR(100),
    dob DATE,
    photo VARCHAR(255),
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

CREATE TABLE admin_users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(50),
    password VARCHAR(255)
);
```

---

## 6. Insert Admin User

```sql
INSERT INTO admin_users(username, password)
VALUES ('admin', 'admin123');
```

---

# Configure Database Connection

Update `config.php`:

```php
<?php

$conn = mysqli_connect("localhost", "root", "", "student_db");

if (!$conn) {
    die("Connection Failed: " . mysqli_connect_error());
}

?>
```

---

# Run the Project

Open browser:

```bash
http://localhost/project-folder-name/
```

---

# Screenshots

## Login Page

* Admin Authentication Interface

## Dashboard

* Student Statistics Cards
* Navigation Menu

## Add Student

* Form Validation
* Image Upload

## View Students

* AJAX Data Fetching
* Live Search
* Sorting & Delete Features

---

# Learning Outcomes

This project demonstrates:

* Full-stack PHP development
* CRUD operations
* MySQL integration
* Session handling
* AJAX implementation
* jQuery DOM manipulation
* Bootstrap responsive design
* Client-side & server-side validation
* File upload handling

---

# Future Improvements

* Password Hashing (`password_hash`)
* PDO instead of mysqli
* Pagination
* Role-based Authentication
* REST API Integration
* Laravel Migration
* Cloud Image Storage
* Data Export (PDF/Excel)

---

# Security Improvements Recommended

* Use `password_hash()` and `password_verify()`
* Validate MIME types for uploads
* Prevent XSS attacks using `htmlspecialchars()`
* Add CSRF protection
* Restrict upload file size

---

# 1. Static Webpage with HTML & CSS

## README.md

````markdown
# Static Webpage using HTML & CSS

A responsive multi-section static webpage developed using HTML5 and CSS3.  
This project demonstrates the use of semantic HTML elements, tables, lists, forms, and media integration.

---

# Features

- Responsive webpage layout
- Semantic HTML5 structure
- Navigation menu
- Tables and lists
- Contact form
- Embedded images and media
- Custom CSS styling
- Mobile-friendly design

---

# Technologies Used

| Technology | Purpose |
|---|---|
| HTML5 | Structure |
| CSS3 | Styling |

---

# Project Structure

```bash
project/
│
├── index.html
├── style.css
├── images/
└── README.md
````

---

# Sections Included

* Header
* Navigation Bar
* About Section
* Services Section
* Table Section
* List Section
* Media Section
* Contact Form
* Footer

---

# How to Run

1. Download or clone the repository
2. Open `index.html` in your browser

---

# Learning Outcomes

* HTML5 semantic tags
* CSS styling techniques
* Responsive layout design
* Form creation
* Table and list implementation
* Media embedding

---

# Author

Developed by Eng. Miguel

````

---

# 2. PHP CRUD with MySQL

## README.md

```markdown
# PHP CRUD Application with MySQL

A simple CRUD (Create, Read, Update, Delete) application developed using PHP and MySQL.  
This project demonstrates database connectivity, form handling, and dynamic data display.

---

# Features

- Insert records into MySQL database
- Display records dynamically
- Edit existing records
- Delete records
- PHP form handling
- MySQL database integration

---

# Technologies Used

| Technology | Purpose |
|---|---|
| HTML5 | Structure |
| CSS3 | Styling |
| PHP | Backend Logic |
| MySQL | Database |
| XAMPP | Local Development Environment |

---

# Project Structure

```bash
project/
│
├── config.php
├── index.php
├── insert.php
├── edit.php
├── delete.php
├── style.css
└── README.md
````

---

# Database Setup

## Database Name

```sql
crud_db
```

---

# Create Table

```sql
CREATE TABLE students (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    email VARCHAR(100),
    course VARCHAR(100)
);
```

---

# Configure Database Connection

Update `config.php`:

```php
<?php

$conn = mysqli_connect("localhost", "root", "", "crud_db");

if (!$conn) {
    die("Connection failed: " . mysqli_connect_error());
}

?>
```

---

# How to Run

1. Move project folder to:

```bash
C:/xampp/htdocs/
```

2. Start Apache and MySQL in XAMPP

3. Open browser:

```bash
http://localhost/project-folder-name/
```

---

# Learning Outcomes

* CRUD operations
* PHP & MySQL integration
* Database connectivity
* Dynamic data rendering
* Form handling

---

# Future Improvements

* Add form validation
* Use prepared statements
* Add search functionality
* Improve UI with Bootstrap

---

# Author

Developed by Eng. Miguel

````

---

# 3. jQuery Selectors & AJAX Request

## README.md

```markdown
# jQuery Selectors & AJAX Project

A frontend project demonstrating jQuery selectors, events, DOM traversal, and AJAX requests.

---

# Features

- jQuery selectors
- DOM manipulation
- Event handling
- AJAX requests
- Dynamic content loading
- Interactive UI effects

---

# Technologies Used

| Technology | Purpose |
|---|---|
| HTML5 | Structure |
| CSS3 | Styling |
| JavaScript | Client-side Logic |
| jQuery | DOM Manipulation & AJAX |

---

# Project Structure

```bash
project/
│
├── index.html
├── style.css
├── script.js
├── data.json
└── README.md
````

---

# Functionalities

## jQuery Selectors

* Element selectors
* Class selectors
* ID selectors
* Attribute selectors

---

# Event Handling

* click()
* keyup()
* hover()
* change()

---

# DOM Traversal

* parent()
* children()
* find()
* siblings()

---

# AJAX Features

* Fetch JSON data
* Dynamically update content
* No page reload

---

# How to Run

1. Open the project folder
2. Run using Live Server or browser

---

# Example AJAX Request

```javascript
$.ajax({
    url: "data.json",
    method: "GET",
    success: function(response) {
        console.log(response);
    }
});
```

---

# Learning Outcomes

* jQuery basics
* DOM traversal techniques
* AJAX implementation
* Dynamic UI updates
* Event-driven programming

---

# Future Improvements

* Add API integration
* Improve animations
* Add form validation
* Convert to Fetch API

---

# Author

Developed by Eng. Miguel

```
```


# Licensehttps://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax

This project is for educational purposes only.
