# INVENTORY-TRACKER-

NAME:LOKESHWARAN.K 
INTERN ID:CITS1967
DOMAIN: Full Stack Web Development
DURATION:4 WEEKS 
MENTOR: NEELASANTOSH

Inventory Tracker (SQL) – Complete Step-by-Step Explanation

Project Overview

Inventory Tracker is a database-driven application used to manage products, stock levels, suppliers, categories, and inventory transactions. It helps businesses monitor inventory, prevent stock shortages, and generate reports.


---

Main Objective

The system helps users:

✅ Add Products

✅ Manage Categories

✅ Manage Suppliers

✅ Record Stock In

✅ Record Stock Out

✅ Track Inventory Levels

✅ Generate Reports

✅ Get Low Stock Alerts


---

Database Structure

The system contains 5 main tables:

1. Categories Table

Stores product categories.

Fields

Field	Description

category_id	Unique category ID
category_name	Category name


Example

ID	Category

1	Electronics
2	Stationery
3	Furniture



---

2. Suppliers Table

Stores supplier information.

Fields

Field	Description

supplier_id	Supplier ID
supplier_name	Supplier name
phone	Contact number
email	Email address
address	Supplier address



---

3. Products Table

Stores all inventory products.

Fields

Field	Description

product_id	Product ID
product_name	Product Name
category_id	Category reference
supplier_id	Supplier reference
sku	Product code
unit_price	Product price
quantity	Available quantity
reorder_level	Minimum stock level



---

Example

Product	Quantity

Laptop	15
Pen	150
Chair	8



---

4. Stock In Table

Stores inventory purchases.

Purpose

Whenever new products arrive.

Example

Product	Quantity

Laptop	10
Pen	200



---

5. Stock Out Table

Stores sales or removed inventory.

Purpose

Whenever products leave inventory.

Example

Product	Quantity

Pen	50
Laptop	2



---

Screen 1: Dashboard

Purpose

Shows overall inventory status.

Features

Total Products

Displays total products.

Example:

23 Products


---

Total Stock

Displays available stock.

Example:

173 Units


---

Low Stock Items

Shows products running low.

Example:

5 Items


---

Inventory Value

Shows total inventory worth.

Example:

₹1,25,430


---

Pie Chart

Displays stock distribution by category.

Example:

Electronics → 45%

Stationery → 30%

Furniture → 25%


---

Screen 2: Products

Purpose

Manage inventory items.


---

Add Product

User enters:

Product Name

SKU

Category

Supplier

Price

Quantity



---

Product List

Displays:

Product Name

SKU

Price

Quantity



---

Actions

✏ Edit Product

🗑 Delete Product

🔍 View Details


---

Screen 3: Stock In

Purpose

Add new inventory.


---

Process

Step 1

Select Product

⬇

Step 2

Enter Quantity

⬇

Step 3

Enter Unit Cost

⬇

Step 4

Save


---

Example

Laptop

Quantity: 10

Cost: ₹50,000

Date: 01-May-2024


---

Result

Inventory quantity increases automatically.


---

Screen 4: Low Stock Alert

Purpose

Warn users before stock runs out.


---

Logic

If:

Current Stock ≤ Reorder Level

Show Alert


---

Example

Product	Stock	Reorder

Chair	8	10
Printer	7	10


Alert displayed.


---

Screen 5: Reports

Purpose

Generate inventory reports.


---

Filters

Select:

Start Date

End Date

Category

Supplier


---

Report Displays

Total Products

Total Quantity

Inventory Value

Stock Movements


---

Example

Category	Quantity

Electronics	70
Stationery	90
Furniture	13



---

SQL Workflow

Add Product

INSERT INTO products
(product_name, unit_price, quantity)
VALUES
('Laptop', 50000, 10);


---

Stock In

INSERT INTO stock_in
(product_id, quantity)
VALUES
(1, 10);

Quantity increases.


---

Stock Out

INSERT INTO stock_out
(product_id, quantity)
VALUES
(1, 2);

Quantity decreases.


---

Check Low Stock

SELECT *
FROM products
WHERE quantity <= reorder_level;


---

User Flow

Step 1

Login

⬇

Step 2

Open Dashboard

⬇

Step 3

Add Categories

⬇

Step 4

Add Suppliers

⬇

Step 5

Add Products

⬇

Step 6

Record Stock In

⬇

Step 7

Record Stock Out

⬇

Step 8

Monitor Inventory

⬇

Step 9

Check Low Stock Alerts

⬇

Step 10

Generate Reports


---

Short Project Description

Inventory Tracker (SQL) is a database management application designed to track products, suppliers, categories, stock-in transactions, and stock-out transactions. The system provides real-time inventory monitoring, low-stock alerts, product management, reporting tools, and inventory valuation features using SQL-based relational database architecture, making it suitable for retail stores, warehouses, and small business inventory management.

<img width="1536" height="1024" alt="5" src="https://github.com/user-attachments/assets/3f3907b2-e59c-4429-a8e9-c75db67846a3" />
