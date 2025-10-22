-----

# 🎓 Guided Learning Path: Programming, Efficiency, and Data Management

This repository documents a comprehensive, guided learning path covering three essential pillars in modern tech and data science: **Python Fundamentals**, **Computational Complexity**, and **SQL/Relational Databases**.

It serves as a detailed reference for core concepts, syntax rules, and practical application techniques.

-----

## 🐍 Module 1: Python Fundamentals

Mastering the foundational elements of the Python language—the rules of syntax, data handling, and control flow—for writing functional and readable scripts.

### 1.1 Python Structure & Syntax

| Concept | Description | Example |
| :--- | :--- | :--- |
| **Keywords** | Reserved words that have fixed meaning; cannot be used as variable names. | `def`, `if`, `while`, `True` |
| **Identifiers** | User-defined names for variables, functions, etc. Must start with a letter or `_`. | `user_score`, `data_2024` |
| **Indentation** | Python's mandatory **4-space indentation** to define code blocks (suites) following a colon (`:`). | `if x > 0:` $\rightarrow$ **Indented block** |
| **Expressions** | Code that **evaluates to a value** (can be used inside statements). | `(5 + 2) * 3` $\rightarrow$ Evaluates to `21` |
| **Statements** | An instruction that the interpreter executes to **perform an action**. | `x = 5`, `print("Hello")` |

### 1.2 Data Types and I/O

| Type | Description | Example | **Note** |
| :--- | :--- | :--- | :--- |
| **Integer (`int`)** | Whole numbers. | `count = 42` | |
| **Float (`float`)** | Numbers with a decimal component. | `pi = 3.14159` | |
| **String (`str`)** | Textual data, enclosed in quotes. | `name = "Alice"` | |
| **Boolean (`bool`)** | Logical state, strictly `True` or `False`. | `is_active = True` | |
| **Input/Output** | Getting user input (always a **string**) and displaying output. | `user = input("Name: ")` | Use `int()` or `float()` for numerical input\! |

### 1.3 Operators and Control Flow

| Feature | Operators/Keywords | Purpose | Example |
| :--- | :--- | :--- | :--- |
| **Arithmetic** | `**` (Exponent), `//` (Floor Div), `%` (Modulo) | Perform mathematical calculations. | `5 ** 2` $\rightarrow$ 25 |
| **Comparison** | `==`, `!=`, `>`, `<` | Used inside conditional logic to check relations. | `age >= 18` |
| **Logical** | `and`, `or`, `not` | Combine multiple Boolean conditions. | `(x > 10) and (y < 5)` |
| **`if/else`** | `if`, `elif`, `else` | Implements conditional decision-making. | `if score > 90: print('A')` |
| **`while` loop** | `while` | Executes a block of code repeatedly as long as the condition is `True`. | `while count < 5: count += 1` |

-----

## ⏱️ Module 2: Computational Complexity (Big O)

Analyzing the efficiency of algorithms to ensure solutions **scale** well, regardless of underlying hardware. Big O Notation measures **worst-case runtime** relative to input size ($\mathbf{N}$).

| Big O Notation | Name | Growth Rate | Scenario/Example |
| :--- | :--- | :--- | :--- |
| $\mathbf{O(1)}$ | **Constant Time** | **Fastest.** Time doesn't change with $\mathbf{N}$. | Accessing an element by index: `my_list[i]` |
| $\mathbf{O(\log N)}$ | **Logarithmic Time** | Time grows very slowly (cuts $\mathbf{N}$ in half each step). | **Binary Search** on a sorted array. |
| $\mathbf{O(N)}$ | **Linear Time** | Time grows directly proportional to $\mathbf{N}$. | A single loop iterating over all $\mathbf{N}$ items. |
| $\mathbf{O(N^2)}$ | **Quadratic Time** | Time grows by $\mathbf{N}$ squared. **Avoid for large datasets.** | A **nested loop** structure. |

-----

## 🗄️ Module 3: SQL and Databases

Mastering the language of data retrieval, manipulation, and management in Relational Database Management Systems (RDBMS).

### 3.1 Database Theory & Foundation

| Concept | Description |
| :--- | :--- |
| **RDBMS & SQL** | Understanding why an organized, relational system is needed for large, interconnected data. |
| **ACID Properties** | Guarantees of transaction reliability: **Atomicity** (all-or-nothing), **Consistency** (maintains rules), **Isolation** (handles concurrency), **Durability** (changes are permanent). |
| **Inspection Commands** | Used to set the working database and view structure: **`USE [db_name]`**, **`SHOW TABLES`**, **`DESCRIBE [table]`**. |

### 3.2 Basic Querying, Filtering, and Sorting

| Clause/Command | Purpose | Example |
| :--- | :--- | :--- |
| **`SELECT / FROM`** | Specifies columns (`*` for all) and the source table. | `SELECT name, email FROM CUSTOMER` |
| **`WHERE`** | Filters **rows** based on a condition. | `WHERE City = 'London' AND Age > 18` |
| **`NULL` Handling** | The special state of unknown data. Cannot use `=` or `!=`. | `WHERE Email IS NULL` / `IS NOT NULL` |
| **`ORDER BY`** | Sorts the result set (default `ASC`). | `ORDER BY Price DESC, Name ASC` |
| **`LIMIT / OFFSET`**| Controls the number of rows returned and allows pagination. | `LIMIT 10 OFFSET 20` |
| **`DISTINCT`** | Removes duplicate values from the selected column(s). | `SELECT DISTINCT City FROM CUSTOMER` |

### 3.3 Aggregation and Grouping

Aggregate functions summarize data, and grouping clauses organize the summary.

| Clause/Function | Purpose | Example |
| :--- | :--- | :--- |
| **`COUNT(*)`** | Counts **all rows** (records). | `SELECT COUNT(*) FROM Orders` |
| **`COUNT(col)`** | Counts only rows where `col` is **not NULL**. | `SELECT COUNT(Phone) FROM CUSTOMER` |
| **`MIN / MAX / AVG / SUM`** | Calculates the minimum, maximum, average, or total sum of a numerical column. | `SELECT AVG(Salary), MAX(Age)` |
| **`GROUP BY`** | Groups rows with identical values to apply aggregation. | `SELECT City, COUNT(*) FROM CUSTOMER GROUP BY City` |
| **`HAVING`** | Filters the **results of the `GROUP BY`** (can use aggregate functions). | `HAVING COUNT(*) > 5` |
| **Keyword Order**| Logical execution order: **FROM $\rightarrow$ WHERE $\rightarrow$ GROUP BY $\rightarrow$ HAVING $\rightarrow$ SELECT $\rightarrow$ ORDER BY $\rightarrow$ LIMIT** | N/A |

### 3.4 Joins (Connecting Data)

Joins combine data from two or more tables based on related columns (Foreign Keys).

| Join Type | Description |
| :--- | :--- |
| **`INNER JOIN`** | Returns rows where there is a **match in both** tables. The intersection. |
| **`LEFT JOIN`** | Returns **all rows from the left** table, and matching rows from the right (returns `NULL` for right-side non-matches). |
| **`RIGHT JOIN`** | Returns **all rows from the right** table, and matching rows from the left (returns `NULL` for left-side non-matches). |
| **`FULL OUTER JOIN`**| Returns matched and unmatched rows from **both** tables (unsupported in MySQL). |
| **`NATURAL JOIN`**| Automatically joins on all columns with identical names and types (use with caution). |

-----

## ⚙️ Project Setup and Execution

To replicate the SQL querying examples, you will need a running database instance and the loaded IMDB dataset.

### Prerequisites

1.  **Python:** Ensure **Python 3.x** is installed.
2.  **RDBMS:** Install **MySQL** (or a similar system like PostgreSQL).

### Database Setup Steps

1.  **Download Data:** Obtain the necessary IMDB dataset files for the "Load IMDB data" portion of the curriculum.
2.  **Access Server:** Log in via the terminal or a GUI client:
    ```bash
    mysql -u [your_user] -p
    ```
3.  **Execute Scripts:** Run the setup and data loading scripts provided in the project files to populate the database tables used in Module 3.

-----

## 📄 License & Contribution

This repository is intended for **educational and personal use**. Suggestions for improvements, clarifications, or code efficiency are welcome.

**Happy Querying\!**

-----
