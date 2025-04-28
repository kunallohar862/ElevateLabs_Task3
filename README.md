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


## 2. JOINS (INNER, LEFT, RIGHT)

Combine data from multiple tables based on relationships.

-- INNER JOIN
SELECT s.name, c.course_name
FROM students s
INNER JOIN courses c ON s.course_id = c.course_id;

-- LEFT JOIN
SELECT s.name, c.course_name
FROM students s
LEFT JOIN courses c ON s.course_id = c.course_id;

-- RIGHT JOIN
SELECT s.name, c.course_name
FROM students s
RIGHT JOIN courses c ON s.course_id = c.course_id;

## 3. Subqueries

Use a query within another query

SELECT name
FROM students
WHERE department_id = (
    SELECT department_id
    FROM departments
    WHERE department_name = 'Computer Science'
);

## 4. Aggregate Functions (SUM, AVG)

Summarize and analyze data

-- Calculate total salary
SELECT SUM(salary) FROM employees;

-- Calculate average age
SELECT AVG(age) FROM students;


## 5. Creating Views

Simplify complex queries and reuse results.

-- Create a view
CREATE VIEW student_summary AS
SELECT department_id, AVG(age) AS avg_age
FROM students
GROUP BY department_id;

-- Query the view
SELECT * FROM student_summary WHERE avg_age > 20;

## 6. Query Optimization with Indexes

Improve the performance of queries using indexes

-- Create an index
CREATE INDEX idx_student_age ON students(age);

## Conclusion

Mastering these SQL fundamentals ensures efficient data handling, complex query building, and optimized database performance — essential skills for real-world software development and data analysis

