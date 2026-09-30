# E-Commerce Order & Inventory Management System

## 📌 Project Overview

The **E-Commerce Order & Inventory Management System** is a MySQL-based relational database project designed to simulate real-world e-commerce business operations.

The project demonstrates practical **SQL and Database Development** skills including relational database design, business data modeling, realistic transactional data, SQL querying, advanced SQL, database programming, transaction management, performance optimization, SQL testing, and business reporting.

---

## 🎯 Project Objective

The objective of this project is to design and implement a structured relational database for managing core e-commerce operations such as:

* Customer management
* Product and category management
* Supplier management
* Warehouse and inventory management
* Order processing
* Payment tracking
* Shipment management
* Returns and refunds
* Coupon management
* Product price history
* Customer reviews
* Customer support
* Order status tracking
* Audit logging

---

## 🛒 Business Workflow

### Order Management

```text
Customer
   ↓
Customer Address
   ↓
Order
   ↓
Order Items
   ↓
Payment
   ↓
Shipment
   ↓
Delivery
   ↓
Return / Refund
```

### Inventory Management

```text
Product
   ↓
Category
   ↓
Supplier
   ↓
Warehouse
   ↓
Inventory
   ↓
Inventory Transactions
```

### Supporting Operations

```text
Customer → Coupons

Product → Price History

Order → Order Status History

Customer → Reviews

Customer → Support Tickets

Database Changes → Audit Logs
```

---

# 🔑 Key Features

* Customer and address management
* Product and category management
* Supplier management
* Warehouse management
* Inventory management
* Inventory transaction tracking
* Customer order management
* Order item management
* Payment tracking
* Shipment management
* Return and refund management
* Coupon management
* Product price history
* Order status history
* Customer reviews
* Customer support tickets
* Audit logging
* SQL-based business analysis

---

# 🗄️ Database Design

**Database:** `ecommerce_db`

The database contains **20 relational tables** using:

* Primary Keys
* Foreign Keys
* Unique Constraints
* NOT NULL Constraints
* CHECK Constraints
* Default Values
* Referential Integrity
* One-to-Many Relationships
* Business Status Management
* Timestamp-based Tracking

---

## 📊 Database Tables

| #  | Table                    | Purpose                      |
| -- | ------------------------ | ---------------------------- |
| 1  | `customers`              | Customer information         |
| 2  | `customer_addresses`     | Customer address information |
| 3  | `categories`             | Product categories           |
| 4  | `suppliers`              | Supplier information         |
| 5  | `products`               | Product details              |
| 6  | `warehouses`             | Warehouse information        |
| 7  | `inventory`              | Current product stock        |
| 8  | `inventory_transactions` | Inventory movement history   |
| 9  | `coupons`                | Discount coupon information  |
| 10 | `orders`                 | Customer orders              |
| 11 | `order_items`            | Products included in orders  |
| 12 | `payments`               | Payment information          |
| 13 | `shipments`              | Shipment information         |
| 14 | `returns`                | Return requests              |
| 15 | `return_items`           | Returned products            |
| 16 | `order_status_history`   | Order status changes         |
| 17 | `product_price_history`  | Product price changes        |
| 18 | `reviews`                | Customer product reviews     |
| 19 | `audit_logs`             | Database audit information   |
| 20 | `support_tickets`        | Customer support requests    |

---

# 💻 SQL Development

## 1. Database Creation

**File:** `01_Create_Database.sql`

Creates the `ecommerce_db` database.

```sql
DROP DATABASE IF EXISTS ecommerce_db;
CREATE DATABASE ecommerce_db;
USE ecommerce_db;
```

---

## 2. Table Design

**File:** `02_Create_Tables.sql`

Creates the complete relational database structure with:

* Primary keys
* Foreign keys
* Constraints
* Relationships
* Validation rules
* Default values
* Status management

---

## 3. Master Data

**File:** `03_Insert_Master_Data.sql`

Contains realistic business data for:

* Customers
* Customer addresses
* Categories
* Suppliers
* Products
* Warehouses
* Inventory
* Coupons

---

## 4. Transactional Data

**File:** `04_Insert_Transactional_Data.sql`

Contains interconnected business transactions including:

* Orders
* Order items
* Payments
* Shipments
* Returns
* Inventory transactions
* Reviews
* Support tickets
* Order status history
* Coupon usage

---

# 🔎 SQL Querying

## 5. Basic SQL

**File:** `05_Basic_SQL_Queries.sql`

Concepts:

* `SELECT`
* `DISTINCT`
* `WHERE`
* `ORDER BY`
* `LIMIT`
* Column aliases
* Basic calculations

---

## 6. Filtering Queries

**File:** `06_Filtering_Queries.sql`

Concepts:

* `AND`
* `OR`
* `IN`
* `NOT IN`
* `BETWEEN`
* `LIKE`
* `NOT LIKE`
* `IS NULL`
* `IS NOT NULL`
* `CASE`

---

## 7. JOIN Operations

**File:** `07_Joins.sql`

Concepts:

* `INNER JOIN`
* `LEFT JOIN`
* `RIGHT JOIN`
* Multiple-table JOINs

Business relationships include:

```text
Customers → Orders
Orders → Order Items
Products → Categories
Products → Inventory
Orders → Payments
Orders → Shipments
```

---

## 8. Aggregate Queries

**File:** `08_Aggregate_Queries.sql`

Concepts:

* `COUNT()`
* `SUM()`
* `AVG()`
* `MIN()`
* `MAX()`
* `GROUP BY`
* `HAVING`

Business analysis includes:

* Total sales
* Customer order counts
* Product sales
* Average order value
* Inventory analysis

---

# 🚀 Advanced SQL

## 9. Subqueries

**File:** `09_Subqueries.sql`

Concepts:

* Single-row subqueries
* Multi-row subqueries
* Correlated subqueries
* `EXISTS`
* `NOT EXISTS`
* `IN`
* `ANY`
* `ALL`
* Derived tables

Business problems include:

* Customers spending above average
* Products above average price
* Customers with orders
* Products without sales
* Product and customer comparisons

---

## 10. Common Table Expressions

**File:** `10_CTE_Queries.sql`

Concepts:

* CTEs
* Multiple CTEs
* CTE-based business analysis

Examples include:

* Customer spending analysis
* Product sales analysis
* Inventory analysis
* Monthly sales analysis

---

## 11. Window Functions

**File:** `11_Window_Functions.sql`

Concepts:

* `ROW_NUMBER()`
* `RANK()`
* `DENSE_RANK()`
* `LAG()`
* `LEAD()`
* Running totals
* `PARTITION BY`

Business use cases include:

* Product ranking
* Customer ranking
* Category-wise ranking
* Sales comparisons
* Price history analysis

---

# ⚙️ Database Programming

## 12. Built-in Functions

**File:** `12_Built_In_Functions.sql`

Includes:

### String Functions

* `CONCAT()`
* `UPPER()`
* `LOWER()`
* `SUBSTRING()`
* `LENGTH()`
* `TRIM()`

### Numeric Functions

* `ROUND()`
* `CEIL()`
* `FLOOR()`
* `ABS()`

### Date Functions

* `CURDATE()`
* `NOW()`
* `YEAR()`
* `MONTH()`
* `DAY()`
* `DATEDIFF()`
* `TIMESTAMPDIFF()`

### NULL Functions

* `COALESCE()`
* `IFNULL()`

---

## 13. User-Defined Functions

**File:** `13_User_Defined_Functions.sql`

Business calculations include:

* Order total
* Discount calculation
* Profit calculation

---

## 14. Stored Procedures

**File:** `14_Stored_Procedures.sql`

Database procedures cover business operations such as:

* Customer order retrieval
* Inventory checking
* Order processing
* Return processing
* Sales analysis

---

## 15. Triggers

**File:** `15_Triggers.sql`

Database automation includes:

* Order status history
* Inventory transactions
* Product price history
* Audit logging

---

## 16. Views

**File:** `16_Views.sql`

Business-oriented views include:

* Customer order summary
* Product sales summary
* Inventory status
* Order tracking
* Customer support summary

---

# 🔄 Transaction Management

**File:** `17_Transactions.sql`

The project demonstrates:

```sql
START TRANSACTION;

COMMIT;

ROLLBACK;

SAVEPOINT;
```

Example business flow:

```text
Place Order
    ↓
Check Inventory
    ↓
Reserve Stock
    ↓
Create Order
    ↓
Process Payment
    ↓
Commit Transaction
```

Transaction management helps maintain data consistency when multiple database operations are involved in a business process.

---

# ⚡ Performance Optimization

**File:** `18_Indexes.sql`

Performance concepts include:

* Index creation
* Index selection
* Query optimization
* `EXPLAIN`
* Indexes on frequently searched columns
* Indexes on filtering columns
* Indexes supporting JOIN operations

Example:

```sql
EXPLAIN
SELECT *
FROM orders
WHERE customer_id = 10;
```

---

# 🧪 SQL Testing

**File:** `19_Test_Cases.sql`

Testing covers:

* Primary key validation
* Foreign key validation
* Duplicate records
* NULL handling
* Invalid values
* Order total validation
* Payment validation
* Inventory validation
* Return validation
* Trigger testing
* Stored procedure testing
* Business rule validation

---

# 📊 Business Reporting

**File:** `20_Business_Reports.sql`

SQL-based business reports include:

* Monthly sales analysis
* Customer analysis
* Top customers
* Product sales analysis
* Top products
* Low-stock analysis
* Warehouse inventory analysis
* Payment analysis
* Return analysis
* Order fulfillment analysis

---

# 📁 Project Structure

```text
E-Commerce-Order-Inventory-Management/
│
├── SQL/
│   ├── 01_Create_Database.sql
│   ├── 02_Create_Tables.sql
│   ├── 03_Insert_Master_Data.sql
│   ├── 04_Insert_Transactional_Data.sql
│   ├── 05_Basic_SQL_Queries.sql
│   ├── 06_Filtering_Queries.sql
│   ├── 07_Joins.sql
│   ├── 08_Aggregate_Queries.sql
│   ├── 09_Subqueries.sql
│   ├── 10_CTE_Queries.sql
│   ├── 11_Window_Functions.sql
│   ├── 12_Built_In_Functions.sql
│   ├── 13_User_Defined_Functions.sql
│   ├── 14_Stored_Procedures.sql
│   ├── 15_Triggers.sql
│   ├── 16_Views.sql
│   ├── 17_Transactions.sql
│   ├── 18_Indexes.sql
│   ├── 19_Test_Cases.sql
│   └── 20_Business_Reports.sql
│
└── README.md
```

---

# 🛠️ Technology Stack

| Technology          | Usage                          |
| ------------------- | ------------------------------ |
| **MySQL**           | Relational Database            |
| **SQL**             | Database Queries & Analysis    |
| **MySQL Workbench** | Database Development & Testing |
| **Git**             | Version Control                |
| **GitHub**          | Project Repository             |

---

# 🧠 Skills Demonstrated

### Database

* Relational Database Design
* Database Schema Design
* Data Modeling
* Primary Keys
* Foreign Keys
* Constraints
* Referential Integrity
* Data Integrity
* Realistic Business Data

### SQL

* Basic SQL
* Filtering
* JOINs
* Aggregate Functions
* Subqueries
* CTEs
* Window Functions

### Database Programming

* MySQL Functions
* User-Defined Functions
* Stored Procedures
* Triggers
* Views
* Transactions

### Performance

* Indexes
* `EXPLAIN`
* Query Optimization

### Testing & Reporting

* SQL Testing
* Business Rule Validation
* Business Reporting
* Data Analysis

### Tools

* MySQL Workbench
* Git
* GitHub

---

# ▶️ How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/KURUVALAKSHMANNA/E-Commerce-Order-Inventory-Management.git
```

### 2. Open MySQL Workbench

Open the project SQL files in MySQL Workbench.

### 3. Execute the SQL Scripts in Sequence

```text
01_Create_Database.sql
02_Create_Tables.sql
03_Insert_Master_Data.sql
04_Insert_Transactional_Data.sql
05_Basic_SQL_Queries.sql
06_Filtering_Queries.sql
07_Joins.sql
08_Aggregate_Queries.sql
09_Subqueries.sql
10_CTE_Queries.sql
11_Window_Functions.sql
12_Built_In_Functions.sql
13_User_Defined_Functions.sql
14_Stored_Procedures.sql
15_Triggers.sql
16_Views.sql
17_Transactions.sql
18_Indexes.sql
19_Test_Cases.sql
20_Business_Reports.sql
```

### 4. Select the Database

```sql
USE ecommerce_db;
```

### 5. Execute and Test the SQL Scripts

Execute each script in the specified order and verify the database results.

---

# 💼 Project Highlights

This project demonstrates practical database development through a realistic e-commerce business scenario.

It combines:

```text
Database Design
      ↓
Data Modeling
      ↓
Realistic Business Data
      ↓
SQL Queries
      ↓
Advanced SQL
      ↓
Database Programming
      ↓
Transactions
      ↓
Performance Optimization
      ↓
Testing
      ↓
Business Reporting
```

The project provides hands-on experience with relational database design, SQL development, database programming, data analysis, transaction management, performance optimization, and business reporting.

---

# 🔗 GitHub Repository

**E-Commerce Order & Inventory Management System**

https://github.com/KURUVALAKSHMANNA/E-Commerce-Order-Inventory-Management

---

# 👨‍💻 Author

**Lakshmanna Kuruva**

B.Tech – Computer Science and Engineering

**GitHub:**
https://github.com/KURUVALAKSHMANNA

**LinkedIn:**
https://www.linkedin.com/in/lakshmanna-kuruva-749250334/
