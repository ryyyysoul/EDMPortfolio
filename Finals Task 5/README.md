# 🥼 *Finals Lab Task 5*
## *Task Description:*
Create an SQL view that displays the following details: `vendors_code`, vendor name, product description, and `p_indate` for all products with a `p_indate` from the year 2002 onward.

Before attempting this task, review the lecture on SQL Views and Stored Procedures to understand how views function. Then, proceed with the following steps:

#### ***1. Launch XAMPP and start MySQL.***
#### ***2. Open MySQL Workbench and create or start a database connection.***
#### ***3. Implement the required view using SQL syntax.***
#### ***4. Explore the use of Stored Procedures, Views, and Functions as part of this exercise.***

---

## Step 1: Create a View
```sql
CREATE VIEW view_products_2002_onwards AS
SELECT v.v_code, v.v_name, p.p_descript, p.p_indate
FROM vendors v
JOIN products p ON v.v_code = p.v_code
WHERE YEAR(p.p_indate) >= 2002;
```

![image](https://github.com/user-attachments/assets/f199845f-8f21-4537-a46e-cb7bfec8cc98)
