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

