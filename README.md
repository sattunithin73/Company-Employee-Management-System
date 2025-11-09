# 🏢 Company Employee Management System (SQL Project)

A beginner-friendly SQL-based project to manage employees and departments using MySQL. This system includes database creation, relational table setup with **primary & foreign keys**, CRUD operations, aggregate functions, and **JOIN queries** to simulate a real-world employee management system.

---

## 📌 Features

- ✅ Create & use company database
- ✅ Relational table setup (`Employee`, `Department`)
- ✅ Primary and foreign key constraints
- ✅ CRUD operations (Create, Read, Update, Delete)
- ✅ Aggregate functions: `SUM()`, `AVG()`, `GROUP BY`, `HAVING`
- ✅ `JOIN` queries to fetch employee and department info together

---

## 🧱 Database Schema

### 📂 Department Table

| Column    | Type        | Constraints      |
| --------- | ----------- | ---------------- |
| dept_id   | INT         | PRIMARY KEY      |
| dept_name | VARCHAR(50) | NOT NULL, UNIQUE |

### 👨‍💼 Employee Table

| Column  | Type          | Constraints                       |
| ------- | ------------- | --------------------------------- |
| emp_id  | INT           | PRIMARY KEY                       |
| name    | VARCHAR(100)  | NOT NULL                          |
| salary  | DECIMAL(10,2) | CHECK (salary > 0)                |
| doj     | DATE          |                                   |
| dept_id | INT           | FOREIGN KEY → Department(dept_id) |

---

## 📊 Sample Queries

### 🔍 Basic SELECT

```sql
SELECT * FROM Department;
```

### 🔎 Filter & Sort

```sql
SELECT name, salary
FROM Employee
WHERE salary > 50000
ORDER BY salary DESC;
```

### ✏️ UPDATE

```sql
UPDATE Employee
SET salary = 65000
WHERE emp_id = 104;
```

### 🗑️ DELETE

```sql
DELETE FROM Employee
WHERE emp_id = 107;
```

### 📈 Aggregate

```sql
SELECT dept_id, SUM(salary) AS total_salary
FROM Employee
GROUP BY dept_id;
```

### 🤝 JOIN

```sql
SELECT e.emp_id, e.name AS employee_name, e.salary, d.dept_name AS department_name
FROM Employee e
JOIN Department d ON e.dept_id = d.dept_id;
```

---

## 📂 How to Run

1. Install MySQL and open MySQL client (Workbench)
2. Run the provided SQL script step by step
3. Query the tables to test

---

## ✅ Summary

This project demonstrates:
- Creating a database
- Working with primary and foreign keys
- CRUD operations
- Filtering and sorting
- Aggregate functions
- Joins

---

## 📩 Lets Connect

<a href="https://www.linkedin.com/in/sattu-nithin-63b00a286/" target="blank"><img align="center" src="https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white" alt="Chinmay'sLinkedinHandle" title="LinkedIn"/></a>

---

