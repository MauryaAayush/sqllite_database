# SQLlite Database

# Employee Database Management System

This repository contains SQL scripts to manage an employee database. The scripts allow you to perform various operations such as adding employees, retrieving information, updating records, and deleting employees from the database.

## Table of Contents

- [Table Schema](#table-schema)
- [Add a New Employee](#add-a-new-employee)
- [Add Multiple Employees](#add-multiple-employees)
- [Retrieve All Employees](#retrieve-all-employees)
- [Retrieve Specific Columns](#retrieve-specific-columns)
- [Find Employees by Role](#find-employees-by-role)
- [Search Employees by Name](#search-employees-by-name)
- [Find Employees by Age and Salary](#find-employees-by-age-and-salary)
- [Update Employee Salary](#update-employee-salary)
- [Update Employee Address](#update-employee-address)
- [Remove an Employee](#remove-an-employee)
- [Delete Employees by Age](#delete-employees-by-age)

## Table Schema

First, create the `employees` table with the following schema:

```sql
CREATE TABLE employees (
    id INT PRIMARY KEY,
    name VARCHAR(100),
    role VARCHAR(50),
    salary DECIMAL(10, 2),
    age INT,
    address VARCHAR(255),
    phone VARCHAR(15)
);
```

## Add a New Employee
### Add a new employee with all details:
```sql
INSERT INTO employees (id,name,role,salary,age,address,Phone)
VALUES (1,'Aayush','CEO',500000,22,'74,raghuvir dham,limbayat,surat',8604949240);
```
## Add Multiple Employees
### Add multiple employees with data:
```sql
INSERT INTO employees (id, name, role, salary, age, address, Phone) VALUES
(4, 'Bhavika', 'CTO', 450000, 28, '12, Krushna Kunj, Adajan, Surat', 860499241),
(5, 'Chetan', 'CFO', 400000, 35, '56, Laxmi Nagar, Vesu, Surat', 8604949242),
(6, 'Dhara', 'COO', 420000, 30, '89, Green Park, Piplod, Surat', 8604949243),
(7, 'Esha', 'CMO', 380000, 32, '45, Shiv Mandir Road, Katargam, Surat', 8604949244),
(8, 'Farhan', 'CIO', 410000, 29, '22, Sagar Society, Rander, Surat', 8604949245);
```

## Retrieve All Employees
### Retrieve all employee information:
```sql
SELECT * FROM employees;
```

## Retrieve Specific Columns
### Get specific columns for all employees (e.g., name, salary):
```sql
SELECT name, salary FROM employees;
```

## Find Employees by Role
### Find employees with a specific role (e.g., CEO):
```sql
SELECT * FROM employees WHERE role = 'CEO';
```

## Search Employees by Name
### Search for employees with names containing "R" (case-insensitive):
```sql
SELECT * FROM employees WHERE LOWER(name) LIKE '%R%';
```

## Find Employees by Age and Salary
### Find employees older than 30 and earning more than $70,000:
```sql
SELECT * FROM employees WHERE age > 28 AND salary > 70000;
```

## Update Employee role
### Change the role of an employee with ID 3:
```sql
UPDATE employees SET role = "developer" WHERE id = 3;
```


## Remove an Employee
### Remove an employee with ID 2:
```sql
DELETE FROM employees WHERE id = 2;
```

## Delete Employees by Age
### Delete all employees with age less than 28 (assuming it's not a valid age):
```sql
DELETE FROM employees WHERE age < 28;
```

