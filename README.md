# farmmangmt
Farm Management System

## Overview
The Farm Management Database System is a robust solution for managing farm operations efficiently. Built using MySQL and XAMPP, it allows users to track and manage farm resources, crops, livestock, employees, and financial transactions.

---

## Features
- **Crop Management:** Record and track crops, planting schedules, and harvest details.
- **Livestock Management:** Maintain records of livestock health, feed schedules, and production.
- **Employee Management:** Manage employee details, roles, and salaries.
- **Inventory Management:** Track tools, seeds, fertilizers, and other farm resources.
- **Financial Reports:** Generate reports on expenses, revenues, and overall profitability.

---

## Prerequisites
- XAMPP (PHPMyAdmin and MySQL Server)
- Web browser (for accessing PHPMyAdmin)
- Basic knowledge of SQL queries

---

## Getting Started

### 1. Install XAMPP
Download and install XAMPP from the [official website](https://www.apachefriends.org/index.html).

### 2. Import the Database
1. Start XAMPP and activate **Apache** and **MySQL** modules.
2. Open your browser and navigate to `http://localhost/phpmyadmin`.
3. Create a new database named `farm_management`.
4. Import the provided SQL file (`farm_management.sql`) into the `farm_management` database.

### 3. Configure Connection
- Update the database connection details in the PHP scripts (if applicable):
```php
$servername = "localhost";
$username = "root";
$password = "";
$dbname = "farm_management";
$conn = new mysqli($servername, $username, $password, $dbname);
```

---

## Queries and Operations

### Example Queries
- **Add New Crop**:
```sql
INSERT INTO crops (name, planting_date, harvest_date, quantity) 
VALUES ('Wheat', '2024-01-01', '2024-06-01', 100);
```

- **View All Employees**:
```sql
SELECT * FROM employees;
```

- **Update Inventory**:
```sql
UPDATE inventory SET quantity = quantity - 10 WHERE item_name = 'Fertilizer';
```

- **Generate Financial Report**:
```sql
SELECT transaction_type, SUM(amount) AS total FROM financial_records GROUP BY transaction_type;
```

---

## Usage
1. Navigate to `http://localhost/phpmyadmin` to interact directly with the database.
2. Use SQL queries for CRUD operations or integrate the database with a front-end system for a complete application.

---
