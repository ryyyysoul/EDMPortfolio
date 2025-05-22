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
- This will display the `Vendors` following needed information.

```sql
CREATE VIEW view_products_2002_onwards AS
SELECT v.v_code, v.v_name, p.p_descript, p.p_indate
FROM vendors v
JOIN products p ON v.v_code = p.v_code
WHERE YEAR(p.p_indate) >= 2002;
```

![image](https://github.com/user-attachments/assets/f199845f-8f21-4537-a46e-cb7bfec8cc98)

---

- This will display all products whose price range is between 100-150.

```sql
CREATE VIEW view_products_price_100_150 AS
SELECT *
FROM Products
WHERE p_price BETWEEN 100 AND 150;
```

![image](https://github.com/user-attachments/assets/2050ce7a-21d3-45fe-b569-27fb56e3474b)

---

- This will COMPUTE for the (TOTAL_PRICE) of ALL PRODUCTS.

```sql
CREATE VIEW view_total_price_by_vendor AS
SELECT v.v_code, v.v_name, p.p_descript, (p.p_onhand * p.p_price) AS total_price
FROM vendors v
JOIN Products p ON v.v_code = p.v_code
WHERE v.v_code IN (21344, 23119, 24288);
```

![image](https://github.com/user-attachments/assets/14a3a123-3a4a-4922-aa9d-c03af60b8881)

---

## Step 2: CREATE a STORED PROCEDURE
- This WILL take a SINGLE PARAMETER and UPDATED the Name of Vendor `Bryson,Inc.` to `Bryson and Co`.

```sql
DELIMITER //
CREATE PROCEDURE update_vendor_name(IN old_name VARCHAR(50))
BEGIN
UPDATE vendors
SET v_name = 'Bryson and Co'
WHERE v_name = old_name;
CALL update_vendor_name('Bryson,Inc.');
SELECT * FROM vendors WHERE v_name LIKE 'Bryson%';
SET SQL_SAFE_UPDATES = 0;
END //
```

![image](https://github.com/user-attachments/assets/da21798f-e100-4fd5-b7f9-d94cacfb8fc0)

---

- A Function that will take 2 parameters(v_code and v_state) and display all the product description and price based on the parameters passed to the function.

```sql
DELIMITER //
CREATE FUNCTION get_products_by_vendor(vcode INT, vstate
VARCHAR(3))
RETURNS TEXT
DETERMINISTIC
BEGIN
DECLARE result TEXT;
SELECT GROUP_CONCAT(CONCAT(p.p_descript, ' - ', p.p_price)
SEPARATOR '; ')
INTO result
FROM Products p
JOIN vendors v ON p.v_code = v.v_code
WHERE v.v_code = vcode AND v.v_state = vstate;
RETURN result;
END //
DELIMITER ;
SELECT get_products_by_vendor(21344, 'KY');
```

![image](https://github.com/user-attachments/assets/202f7222-5b6b-46ea-9325-f0cfbb776ed8)
