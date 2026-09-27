# E-Commerce Order & Inventory Management System

A **MySQL-based E-Commerce Order & Inventory Management System** designed to simulate real-world database operations of an e-commerce business.

The project demonstrates practical **SQL and Database Developer skills** including relational database design, realistic business data, SQL queries, JOINs, aggregations, advanced SQL concepts, database programming, transactions, performance optimization, testing, and business reporting.

---

## Project Overview

This project models the core database operations of an e-commerce platform, covering the complete flow from **customers and products to orders, payments, shipments, inventory, returns, and customer support**.

It is designed as a practical database project to demonstrate how a Database Developer works with:

* Relational database design
* Business data modelling
* Data integrity
* SQL querying
* Data analysis
* Database programming
* Transaction management
* Performance optimization
* Testing
* Business reporting

---

## Business Workflow

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

# Key Features

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

# Database Design

Database:

```sql
ecommerce_db
```

The database contains **20 relational tables** designed using:

* Primary Keys
* Foreign Keys
* Unique Constraints
* NOT NULL Constraints
* CHECK Constraints
* Default Values
* Referential Integrity
* One-to-Many Relationships
* Business Status Management
* Timestamp-based tracking

---

# Database Tables

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

# SQL Development

The project contains SQL scripts covering different database development areas.

### Database Creation

```text
01_Create_Database.sql
```

Creates the `ecommerce_db` database.

### Table Design

```text
02_Create_Tables.sql
```

Creates the complete relational database structure with keys, constraints, relationships, and validation rules.

### Master Data

```text
03_Insert_Master_Data.sql
```

Contains business data for:

* Customers
* Addresses
* Categories
* Suppliers
* Products
* Warehouses
* Inventory
* Coupons

### Transactional Data

```text
04_Insert_Transactional_Data.sql
```

Contains realistic business transactions including:

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

# SQL Querying

The project demonstrates practical SQL queries used for retrieving and analyzing business data.

### Basic SQL

```text
05_Basic_SQL_Queries.sql
```

Concepts:

* SELECT
* DISTINCT
* WHERE
* ORDER BY
* LIMIT

### Filtering

```text
06_Filtering_Queries.sql
```

Concepts:

* AND
* OR
* IN
* BETWEEN
* LIKE
* IS NULL
* CASE

### JOINs

```text
07_Joins.sql
```

Concepts:

* INNER JOIN
* LEFT JOIN
* RIGHT JOIN
* Multiple-table JOINs

Example business relationships:

```text
Customers → Orders
Orders → Order Items
Products → Categories
Products → Inventory
Orders → Payments
Orders → Shipments
```

### Aggregate Queries

```text
08_Aggregate_Queries.sql
```

Concepts:

* COUNT()
* SUM()
* AVG()
* MIN()
* MAX()
* GROUP BY
* HAVING

These queries are used for business analysis such as:

* Total sales
* Customer order counts
* Product sales
* Average order value
* Inventory analysis

---

# Advanced SQL

The project also covers advanced SQL concepts:

### Subqueries

```text
09_Subqueries.sql
```

* Scalar subqueries
* Correlated subqueries
* EXISTS
* NOT EXISTS
* IN
* Derived tables

### Common Table Expressions

```text
10_CTE_Queries.sql
```

* CTEs
* Multiple CTEs
* Business analysis using CTEs

### Window Functions

```text
11_Window_Functions.sql
```

* ROW_NUMBER()
* RANK()
* DENSE_RANK()
* LAG()
* LEAD()
* Running totals
* PARTITION BY

---

# Database Programming

The project demonstrates database programming concepts using MySQL.

### Built-in Functions

```text
12_Built_In_Functions.sql
```

Includes:

* String functions
* Date functions
* Numeric functions
* NULL functions

### User-Defined Functions

```text
13_User_Defined_Functions.sql
```

Business calculations such as:

* Order total
* Discount calculation
* Profit calculation

### Stored Procedures

```text
14_Stored_Procedures.sql
```

Business operations such as:

* Customer order retrieval
* Inventory checking
* Order processing
* Return processing
* Sales analysis

### Triggers

```text
15_Triggers.sql
```

Database automation such as:

* Order status history
* Inventory transactions
* Price history
* Audit logging

### Views

```text
16_Views.sql
```

Business-oriented database views such as:

* Customer order summary
* Product sales summary
* Inventory status
* Order tracking
* Customer support summary

---

# Transaction Management

```text
17_Transactions.sql
```

Demonstrates:

```sql
START TRANSACTION;
COMMIT;
ROLLBACK;
SAVEPOINT;
```

Example:

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

Transaction handling helps maintain data consistency when multiple database operations are involved in a business process.

---

# Performance Optimization

```text
18_Indexes.sql
```

The project demonstrates database performance concepts using:

```sql
EXPLAIN
```

Indexes are applied to frequently searched, filtered, and joined columns.

---

# SQL Testing

```text
19_Test_Cases.sql
```

Database testing covers scenarios such as:

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

# Business Reporting

```text
20_Business_Reports.sql
```

SQL-based business reports include:

* Monthly sales analysis
* Customer analysis
* Top customers
* Product sales analysis
* Top products
* Low stock analysis
* Warehouse inventory analysis
* Payment analysis
* Return analysis
* Order fulfillment analysis

---

# Project Structure

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

# Technology Stack

| Technology      | Usage                          |
| --------------- | ------------------------------ |
| MySQL           | Relational Database            |
| SQL             | Database Queries & Analysis    |
| MySQL Workbench | Database Development & Testing |
| Git             | Version Control                |
| GitHub          | Project Repository             |

---

# Skills Demonstrated

```text
MySQL
SQL
Relational Database Design
Database Schema Design
Data Modelling
Primary Keys
Foreign Keys
Constraints
Data Integrity
Realistic Business Data
JOINs
Aggregate Functions
Filtering
Subqueries
CTEs
Window Functions
SQL Functions
Stored Procedures
Triggers
Views
Transactions
Indexes
EXPLAIN
SQL Testing
Business Reporting
Git
GitHub
```

---

# How to Run

### 1. Clone the repository

```bash
git clone https://github.com/KURUVALAKSHMANNA/E-Commerce-Order-Inventory-Management.git
```

### 2. Open MySQL Workbench

### 3. Execute the SQL scripts in sequence

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

### 4. Select the database

```sql
USE ecommerce_db;
```

### 5. Execute and test the SQL scripts

---

# Why This Project

This project is built to demonstrate practical database development skills through a realistic e-commerce business scenario.

It combines:

```text
Database Design
      ↓
Data Modelling
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

The project provides hands-on experience with the types of database operations commonly used in real-world business applications.

---

 # 👨‍💻 Author

**Lakshmanna Kuruva**

Aspiring Database Developer / SQL Developer

 Email: [kuruvalakshmanna4154@gmail.com](mailto:kuruvalakshmanna4154@gmail.com)

🔗 GitHub: [KURUVALAKSHMANNA](https://github.com/KURUVALAKSHMANNA)
