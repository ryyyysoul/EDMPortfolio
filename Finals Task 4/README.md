# 🧩 *Finals Lab Task 4*
## *Task Description:*
- This task involved working with a single database containing two tables: `EmployeeSalaries` and `EmployeeData`. I performed a series of SELECT statements to **extract and manipulate** employee information.

---

## Step 1: Query Statements
**Objective:** Perform queries on the `EmployeeSalaries` table.
- ### Problem 1: Consider a table named EmployeeSalaries that stores information about the salaries of employees.
- ### The table has the following fields:
```sql
CREATE DATABASE payroll;
USE payroll;

CREATE TABLE EmployeeSalaries (
    employee_id INT AUTO_INCREMENT PRIMARY KEY,
    employee_name VARCHAR(100),
    department VARCHAR(50),
    salary DECIMAL(10,2),
    hire_date DATE
);
```
![image](https://github.com/user-attachments/assets/abcfda96-0bd8-45b6-848a-3cee5b83d0d6)

---

### Retrieve the employee_name and salary and arrange from the highest salary to lowest.
```sql
SELECT employee_name, salary FROM EmployeeSalaries ORDER BY salary DESC;
```
![image](https://github.com/user-attachments/assets/c2f9f9da-1d2e-4c4b-a636-ee826de58774)
### Retrieve the department names along with the average salary for each department.
```sql
SELECT department, AVG(salary) AS average_salary FROM EmployeeSalaries GROUP BY department;
```
![image](https://github.com/user-attachments/assets/1a6e739c-1008-488b-933b-31ad1b14d4b4)

## Step 2: Key Schema Statements
**Objective:** Perform queries on the `EmployeeData` table.
- ### Problem 2: Create a database named employeeDB and copy and paste the initial query.
- ### The `EmployeeData` table stores information about employees with the following schema:
```sql
CREATE DATABASE employeeDB;
USE employeeDB;

CREATE TABLE EmployeeData (
    employee_id INT AUTO_INCREMENT PRIMARY KEY,
    full_name VARCHAR(100),
    department VARCHAR(50),
    salary DECIMAL(10,2),
    hire_date DATE,
    manager_id INT
);
```
![image](https://github.com/user-attachments/assets/9e4211c3-0f9c-4b1e-a22b-07733625f349)

---

### Retrieve the employees along with their full names and salaries with highest paying employee to the lowest.
```sql
SELECT full_name, salary FROM EmployeeData ORDER BY salary DESC;
```
![image](https://github.com/user-attachments/assets/3c87ab2e-80e3-4e4c-b50f-e9cd6578e20d)
### Retrieve the average salary from EmployeeData table, where the average salary exceeds $70,000.
```sql
SELECT AVG(salary) AS average_salary FROM EmployeeData HAVING average_salary > 70000;
```
![image](https://github.com/user-attachments/assets/61147522-d7f1-4f8a-9f44-aece0700f122)
### Retrieve the full names of employees who earn a salary greater than $100,000.
```sql
SELECT full_name FROM EmployeeData WHERE salary > 100000;
```
![image](https://github.com/user-attachments/assets/a486e92f-0535-49d4-a236-105561f5b59a)
### Retrieve the number of employees from the EmployeeData table.
```sql
SELECT COUNT(employee_id) AS number_of_employees FROM EmployeeData;
```
![image](https://github.com/user-attachments/assets/199d36e9-4a2e-438f-8acc-4e74e4f8e07b)
