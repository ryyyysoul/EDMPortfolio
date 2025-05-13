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
