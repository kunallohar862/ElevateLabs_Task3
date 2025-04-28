# ElevateLabs_Task3


# SQL Concepts and Practice

This repository contains concise explanations and examples of essential SQL concepts for database querying, data aggregation, joining tables, creating views, and optimizing performance.

## Topics Covered

- SELECT, WHERE, ORDER BY, GROUP BY
- JOINS (INNER, LEFT, RIGHT)
- Subqueries
- Aggregate Functions (SUM, AVG)
- Creating Views
- Query Optimization with Indexes

---

## 1. SELECT, WHERE, ORDER BY, GROUP BY

Basic data retrieval and organization.

```sql
-- SELECT specific columns
SELECT name, age FROM students;

-- Filter records
SELECT name FROM students WHERE age > 18;

-- Sort records
SELECT * FROM students ORDER BY age DESC;

-- Group records for aggregation
SELECT department, COUNT(*) FROM employees GROUP BY department;
