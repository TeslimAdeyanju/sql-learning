# 🎓 SQL Code Portfolio: Aliases, Joins, and Aggregations 🚀

[![SQL](https://img.shields.io/badge/SQL-MySQL-blue)](https://www.mysql.com/) 
[![Portfolio](https://img.shields.io/badge/Portfolio-Data%20Analysis-informational)](https://github.com/yourusername)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

A collection of SQL queries designed to highlight essential SQL techniques such as **column and table aliases**, **join operations**, **aggregations**, and **conditional filtering**. This notebook is crafted to showcase practical skills and serve as a reference for SQL best practices, making it perfect for your data analysis or database management portfolio.

## 📂 Notebook Overview

The notebook is divided into several sections, each focusing on different aspects of SQL. Here’s a snapshot of what you’ll find:

### 1. 🎨 Column Aliases
   - Use column aliases to give **meaningful names** to columns, enhancing readability in query outputs.
   - Example:
     ```sql
     SELECT column_name AS descriptive_name FROM table_name;
     ```

### 2. 🗂️ Table Aliases
   - Simplify table references in complex queries using **table aliases**, especially in multi-table join scenarios.
   - Example:
     ```sql
     SELECT e.firstName, e.lastName FROM employees e ORDER BY e.firstName;
     ```

### 3. 🔗 Joins with Aliases
   - Master table joins with **aliases** to handle duplicate column names and reduce verbosity in the query.
   - Example:
     ```sql
     SELECT c.customerName, COUNT(o.orderNumber) AS total
     FROM customers c
     INNER JOIN orders o ON c.customerNumber = o.customerNumber
     GROUP BY c.customerName ORDER BY total DESC;
     ```

### 4. 📊 Aggregations and Filtering with HAVING
   - Learn to apply **aggregations** with aliases and use the `HAVING` clause for conditional filtering on grouped results.
   - Example:
     ```sql
     SELECT orderNumber AS `Order no.`, SUM(priceEach * quantityOrdered) AS Total
     FROM orderdetails
     GROUP BY orderNumber
     HAVING Total > 60000;
     ```

## 🎯 Purpose and Applications

This notebook serves dual purposes:
- 🚀 **Learning Tool**: Understand and practice fundamental SQL techniques essential for data manipulation and reporting.
- 🛠️ **Portfolio Piece**: Demonstrate practical SQL skills, enhancing readability, performing joins, aggregating data, and applying conditional filters for real-world scenarios.

These queries are fundamental for **data analysis**, **reporting**, and **database backend development**.

## 🚀 How to Use This Notebook

1. **Clone the Repository**: 
   ```bash
   git clone https://github.com/yourusername/sql-code-portfolio.git
