# Company_DB-MySQL-Queries

## 📌 Overview
This repository contains MySQL queries for creating and modifying the `employees` table in the `Company_DB` database.  
It demonstrates **table creation, data insertion, and schema evolution** using `ALTER TABLE` commands, with screenshots showing each step.

---

## ⚙️ Queries Included

### 1. Create Database & Table
```sql
CREATE DATABASE Company_DB;
USE Company_DB;

CREATE TABLE employees (
    employee_ID INT AUTO_INCREMENT PRIMARY KEY,
    First_Name VARCHAR(25),
    Last_Name VARCHAR(25),
    Email VARCHAR(100),
    Hire_Date DATE,
    Salary INT
);

## 2. INSERT RECORDS
    INSERT INTO employees (First_Name, Last_Name, Email, Hire_Date, Salary)
VALUES 
('Amit', 'Verma', 'amit.verma@company.com', '2021-06-15', 55000),
('Neha', 'Sharma', 'neha.sharma@company.com', '2020-09-10', 62000),
('Rohan', 'Kapoor', 'rohan.kapoor@company.com', '2022-03-20', 48000),
('Sneha', 'Patel', 'sneha.patel@company.com', '2019-11-05', 72000),
('Vikram', 'Singh', 'vikram.singh@company.com', '2023-01-25', 65000);

## 3. Add Single Column
ALTER TABLE employees
ADD COLUMN department VARCHAR(30);

➕ Added Single Column

<p align="center"> <img src="./1%20COLUMN.png" alt="Add single column" width="800"> </p>

## 4. Add Two Columns
ALTER TABLE employees
ADD COLUMN emergency_contact VARCHAR(20),
ADD COLUMN date_of_joining DATE;

➕ Added Two Columns

<p align="center"> <img src="./2%20COLUMN.png" alt="Add two columns" width="800"> </p>

## 5. Rename Column
ALTER TABLE employees
CHANGE COLUMN emergency_contact emergency_phone VARCHAR(20);

🖊️ Renamed Column

<p align="center"> <img src="./COLUMN%20NAME%20CHANGE.png" alt="Rename column" width="800"> </p>

##. 6. Drop Columns
ALTER TABLE employees
DROP COLUMN date_of_joining,
DROP COLUMN emergency_phone;

🗑️ Dropped Columns

<p align="center"> <img src="./COLUMN%20DROP.png" alt="Drop column" width="800"> </p> ```
