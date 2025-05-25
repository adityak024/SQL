# SQL
"Practice SQL problems and solutions — covers basics to advanced topics like joins, window functions, and data aggregation."

This repository contains foundational SQL scripts and examples using **MySQL**, covering key database operations and concepts including table creation, constraints, CRUD operations, joins, aggregate functions, window functions, normalization, and Common Table Expressions (CTEs).

---

## 📚 Topics Covered

- Creating Tables
- Adding Constraints (Primary Key, Foreign Key, Unique, Not Null)
- Inserting, Updating, and Deleting Data
- SQL Joins (INNER, LEFT, RIGHT, FULL)
- Aggregate Functions (`COUNT`, `AVG`, `SUM`)
- String and Date Functions (`UPPER`, `MONTH`)
- `GROUP BY` Clauses
- Window Functions (`ROW_NUMBER`, `RANK`, `LEAD`, `LAG`)
- Database Normalization (1NF, 2NF, 3NF)
- Common Table Expressions (CTEs)

---

## 🛠️ Technologies Used

- **MySQL** (Tested on version 8.0+)
- SQL Workbench / DBeaver / phpMyAdmin (any MySQL-compatible GUI)
- `.sql` files for each topic

---

## 📂 Folder Structure

sql-basics/
│
├── create_table.sql
├── constraints.sql
├── insert_update_delete.sql
├── joins.sql
├── aggregate_functions.sql
├── string_date_functions.sql
├── group_by.sql
├── window_functions.sql
├── normalization_notes.md
├── cte_examples.sql
└── sample_dataset.sql

yaml
Copy
Edit

---

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/sql-basics.git
cd sql-basics
2. Set Up MySQL
Ensure MySQL is installed and running. Use a MySQL client like Workbench or any other tool.

3. Import Scripts
Run the .sql files in the recommended order or as per your learning needs.

🔍 Examples
✅ Create Table
sql
Copy
Edit
CREATE TABLE employees (
    emp_id INT PRIMARY KEY,
    name VARCHAR(100),
    salary DECIMAL(10,2)
);
✅ Inner Join
sql
Copy
Edit
SELECT e.name, d.department_name
FROM employees e
INNER JOIN departments d ON e.dept_id = d.dept_id;
✅ Aggregate Function
sql
Copy
Edit
SELECT department_id, AVG(salary)
FROM employees
GROUP BY department_id;
✅ Window Function
sql
Copy
Edit
SELECT name, salary,
       RANK() OVER (ORDER BY salary DESC) as rank
FROM employees;
📖 Learning Notes
You’ll also find notes and comments in each script to explain the SQL syntax and logic, making it easy for beginners to follow.

