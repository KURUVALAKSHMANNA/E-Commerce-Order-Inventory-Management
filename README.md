# E-Commerce Order & Inventory Management System

A real-world **MySQL database project** designed to simulate the database operations of an e-commerce platform.

This project is being developed step-by-step from database creation and relational schema design to realistic business data, advanced SQL, database programming, transactions, performance optimization, testing, and business reporting.

## Project Objective

The objective of this project is to demonstrate practical **Database Developer / SQL Developer** skills by building a complete relational database for an e-commerce business.

The project focuses on:

* Relational database design
* Data integrity
* Realistic business data
* SQL querying
* Advanced SQL
* Database programming
* Transaction management
* Performance optimization
* Testing
* Business reporting

---

# Business Scenario

The system represents an e-commerce company that manages customers, products, suppliers, warehouses, inventory, orders, payments, shipments, returns, reviews, coupons, and customer support.

### Main Order Flow

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

### Inventory Flow

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

### Supporting Processes

```text
Customer → Coupons

Product → Price History

Order → Order Status History

Customer → Reviews

Customer → Support Tickets

Database Changes → Audit Logs
```

---

# Technology Used

* **MySQL**
* **SQL**
* **MySQL Workbench**
* **Git**
* **GitHub**

---

# Database

Database name:

```sql
ecommerce_db
```

The database is designed using relational concepts such as:

* Primary Keys
* Foreign Keys
* Unique Constraints
* NOT NULL Constraints
* CHECK Constraints
* Default Values
* Referential Integrity
* One-to-Many Relationships
* Business Status Management

---

# Database Tables

The project contains 20 core tables.

| #  | Table                    | Purpose                          |
| -- | ------------------------ | -------------------------------- |
| 1  | `customers`              | Stores customer information      |
| 2  | `customer_addresses`     | Stores customer addresses        |
| 3  | `categories`             | Stores product categories        |
| 4  | `suppliers`              | Stores supplier information      |
| 5  | `products`               | Stores product details           |
| 6  | `warehouses`             | Stores warehouse information     |
| 7  | `inventory`              | Stores current inventory         |
| 8  | `inventory_transactions` | Tracks inventory movements       |
| 9  | `coupons`                | Stores discount coupons          |
| 10 | `orders`                 | Stores customer orders           |
| 11 | `order_items`            | Stores products within orders    |
| 12 | `payments`               | Stores payment information       |
| 13 | `shipments`              | Stores shipment information      |
| 14 | `returns`                | Stores return requests           |
| 15 | `return_items`           | Stores returned products         |
| 16 | `order_status_history`   | Tracks order status changes      |
| 17 | `product_price_history`  | Tracks product price changes     |
| 18 | `reviews`                | Stores customer reviews          |
| 19 | `audit_logs`             | Stores audit information         |
| 20 | `support_tickets`        | Stores customer support requests |

---

# Project Structure

```text
E-Commerce-Order-Inventory-Management/
│
├── SQL/
│   │
│   ├── 01_Create_Database.sql
│   ├── 02_Create_Tables.sql
│   ├── 03_Insert_Master_Data.sql
│   ├── 04_Insert_Transactional_Data.sql
│   │
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

# SQL Development Phases

## Phase 1 — Database Creation

**File:** `01_Create_Database.sql`

Creates the project database:

```sql
DROP DATABASE IF EXISTS ecommerce_db;
CREATE DATABASE ecommerce_db;
USE ecommerce_db;
```

---

## Phase 2 — Table Design

**File:** `02_Create_Tables.sql`

Creates the complete relational database structure.

The schema includes:

* Primary keys
* Foreign keys
* Constraints
* Relationships
* Default values
* Status fields
* Timestamp columns
* Data validation rules

---

## Phase 3 — Master Data

**File:** `03_Insert_Master_Data.sql`

The master dataset contains realistic business information for:

* Customers
* Customer addresses
* Categories
* Suppliers
* Products
* Warehouses
* Inventory
* Coupons

This data provides the foundation for the transactional part of the project.

---

## Phase 4 — Transactional Data

**File:** `04_Insert_Transactional_Data.sql`

This phase populates the database with realistic e-commerce transactions connected to the existing master data.

Planned transaction scenarios include:

* Multiple customer orders
* Multiple order items
* Different payment methods
* Different payment statuses
* Processing orders
* Shipped orders
* Delivered orders
* Cancelled orders
* Product returns
* Refunds
* Inventory movements
* Coupon usage
* Order status history
* Customer reviews
* Support tickets

---

# Advanced SQL

After the data population phases, the project will progressively implement advanced SQL concepts.

### Basic SQL

`05_Basic_SQL_Queries.sql`

* SELECT
* DISTINCT
* WHERE
* ORDER BY
* LIMIT

### Filtering

`06_Filtering_Queries.sql`

* AND
* OR
* IN
* BETWEEN
* LIKE
* IS NULL
* CASE

### JOINs

`07_Joins.sql`

* INNER JOIN
* LEFT JOIN
* RIGHT JOIN
* Multiple-table JOINs

### Aggregations

`08_Aggregate_Queries.sql`

* COUNT
* SUM
* AVG
* MIN
* MAX
* GROUP BY
* HAVING

### Subqueries

`09_Subqueries.sql`

* Scalar subqueries
* Correlated subqueries
* EXISTS
* NOT EXISTS
* IN
* Derived tables

### CTEs

`10_CTE_Queries.sql`

* Common Table Expressions
* Multiple CTEs
* Business analysis using CTEs

### Window Functions

`11_Window_Functions.sql`

* ROW_NUMBER
* RANK
* DENSE_RANK
* LAG
* LEAD
* Running totals
* PARTITION BY

---

# Database Programming

The project will also cover database programming concepts.

### Built-in Functions

`12_Built_In_Functions.sql`

Examples:

```text
String Functions
Date Functions
Numeric Functions
NULL Functions
```

### User-Defined Functions

`13_User_Defined_Functions.sql`

Business-specific functions will be developed for calculations such as:

```text
Order Total
Discount Calculation
Profit Calculation
```

### Stored Procedures

`14_Stored_Procedures.sql`

Procedures will be developed for operations such as:

```text
Customer Order Retrieval
Inventory Checking
Order Processing
Return Processing
Sales Analysis
```

### Triggers

`15_Triggers.sql`

Triggers will be used for database automation such as:

```text
Order Status History
Inventory Transactions
Price History
Audit Logging
```

### Views

`16_Views.sql`

Business-oriented views will be created for commonly required information.

Examples:

```text
Customer Order Summary
Product Sales Summary
Inventory Status
Order Tracking
Customer Support Summary
```

---

# Transactions

**File:** `17_Transactions.sql`

Transaction management will demonstrate:

```sql
START TRANSACTION;

COMMIT;

ROLLBACK;

SAVEPOINT;
```

Example business process:

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

If an operation fails:

```text
ROLLBACK
```

---

# Performance Optimization

**File:** `18_Indexes.sql`

Database performance will be analyzed using:

```sql
EXPLAIN
```

Indexes will be created based on actual query requirements and frequently searched or joined columns.

---

# SQL Testing

**File:** `19_Test_Cases.sql`

Testing will cover:

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
* Business rule testing

---

# Business Reports

**File:** `20_Business_Reports.sql`

The final reporting phase will contain SQL-based business reports such as:

* Monthly Sales Report
* Top Customers
* Top Products
* Low Stock Report
* Warehouse Inventory Report
* Payment Analysis
* Return Analysis
* Order Fulfillment Analysis
* Customer Analysis
* Product Sales Analysis

---

# Project Execution Order

Run the SQL files in this order:

```text
01 → Create Database
02 → Create Tables
03 → Insert Master Data
04 → Insert Transactional Data
05 → Basic SQL
06 → Filtering
07 → JOINs
08 → Aggregations
09 → Subqueries
10 → CTEs
11 → Window Functions
12 → Built-in Functions
13 → User-Defined Functions
14 → Stored Procedures
15 → Triggers
16 → Views
17 → Transactions
18 → Indexes
19 → Testing
20 → Business Reports
```

---

# Current Project Status

| Phase                  | Status                |
| ---------------------- | --------------------- |
| Database Creation      | ✅ Completed           |
| Table Design           | ✅ Completed           |
| Master Data            | ✅ Completed           |
| Transactional Data     | 🔄 In Progress / Next |
| Basic SQL Queries      | ⏳ Pending             |
| Filtering Queries      | ⏳ Pending             |
| JOINs                  | ⏳ Pending             |
| Aggregate Queries      | ⏳ Pending             |
| Subqueries             | ⏳ Pending             |
| CTEs                   | ⏳ Pending             |
| Window Functions       | ⏳ Pending             |
| Built-in Functions     | ⏳ Pending             |
| User-Defined Functions | ⏳ Pending             |
| Stored Procedures      | ⏳ Pending             |
| Triggers               | ⏳ Pending             |
| Views                  | ⏳ Pending             |
| Transactions           | ⏳ Pending             |
| Indexes                | ⏳ Pending             |
| Test Cases             | ⏳ Pending             |
| Business Reports       | ⏳ Pending             |

---

# Skills Demonstrated

```text
MySQL
SQL
Relational Database Design
Database Schema Design
Primary Keys
Foreign Keys
Constraints
Data Integrity
JOINs
Aggregate Functions
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

### 3. Execute the SQL files in order

```text
01_Create_Database.sql
02_Create_Tables.sql
03_Insert_Master_Data.sql
04_Insert_Transactional_Data.sql
...
```

### 4. Select the database

```sql
USE ecommerce_db;
```

### 5. Execute and test the SQL scripts

---

# Project Goal

The goal is to build a complete real-world database system rather than a collection of isolated SQL queries.

The project progressively covers:

```text
Database Design
      ↓
Table Creation
      ↓
Master Data
      ↓
Transactional Data
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

---

# Author

**Lakshmanna Kuruva**

Aspiring Database Developer / SQL Developer
Email: kuruvalakshmanna4154@gmail.com
GitHub: [KURUVALAKSHMANNA](https://github.com/KURUVALAKSHMANNA)

---

## Project Status

This project is being developed incrementally. The README will be updated as each phase is completed.
