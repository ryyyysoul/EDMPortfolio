# 🧠 *Finals Lab Task 3*
## *Task Description*
- **Designed and manipulated** a MySQL table named products by creating fields with appropriate data types and constraints. I created a product table, enforce business logic using a `check constraint`, insert valid data, and modify column definitions.

## Step 1: Create a table named *products* with the following fields:
- id: Unique integer, auto-increment, primary key.
- product_name: String (VARCHAR) with a maximum length of 100, cannot be null.
- price: Decimal

```sql
CREATE TABLE products_tbl ( 
id INT AUTO_INCREMENT PRIMARY KEY, 
product_name VARCHAR(100) NOT NULL, 
price DECIMAL(10, 2) ); 
```

![image](https://github.com/user-attachments/assets/6ab2ce8a-a024-4003-86f7-b2f717a090e5)

## Step 2
- Add a `CHECK` constraint, ensure that the price of the product must be greater than 0.
- Insert the products that will not violate the check constraint into the products table:

```sql
INSERT INTO products_tbl (product_name, price) VALUES
- ('Laptop', 999.99),
- ('Smartphone', 599.99),
- ('Tablet', 299.99),
- ('Keyboard', 19.99),
- ('Mouse', 14.99),
- ('Desk Lamp', 24.99),
- ('Speakers', 9.99); 
```

![image](https://github.com/user-attachments/assets/165e8052-2168-43ef-acbb-c69bbd9be982)

## Step 3: Modify the product name.
```sql
ALTER TABLE products_tbl MODIFY COLUMN product_name VARCHAR(120) NOT NULL; 
```

## ER Diagram
![image](https://github.com/user-attachments/assets/6919c29d-d6af-4a90-a4e2-b37cbab3a4bb)

## SQL Copy
