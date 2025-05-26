### 1. What is PostgreSQL?
**Answer:**  
PostgreSQL is an open-source object-relational database management system that combines the power of relational databases with the flexibility of object-oriented programming.

_PostgreSQL_ is often referred to by its short nickname **'Postgres'**. It is an advanced open-source Object Relational Database Management System (ORDBMS).

---

### 2. What is the purpose of a database schema in PostgreSQL?
**Answer:**  
In our database, the main goal is to retrieve the stored data as meaningful information. Without maintaining proper serial order and relationships, simply storing data doesn't qualify as a database.  
By definition, a database must store data in a structured, relational manner. This is essential for managing data correctly in large-scale projects.  
Otherwise, various types of **redundancy** and **anomalies** may occur.  
Therefore, designing a proper **database schema** is one of the best ways to store data efficiently.

---

### 3. Explain the Primary Key and Foreign Key concepts in PostgreSQL.

#### ✅ Primary Key:
- A primary key is a unique identifier for each record in a table.
- It cannot accept `NULL` values, and each table can have only one primary key.
- It can consist of a **single column** or **multiple columns** (composite key).

**Example:**  
A `Users` table with fields `UserID`, `Username`, `Email` – here, `UserID` can serve as the **primary key**.

🔹 Primary keys help with quick data retrieval and make search operations efficient.

#### 🔗 Foreign Key:
- A foreign key is a field (or group of fields) in one table that references the **primary key** of another table.
- It creates a relationship between two tables and enforces **referential integrity**.

**Example:**  
An `Orders` table might include a `CustomerID` field as a foreign key that points to `CustomerID` in the `Customers` table.

---

### 4. What is the difference between the VARCHAR and CHAR data types?

#### 🔸 CHAR:
- **Fixed-length** data type.
- Always allocates the same space even if the string is shorter.
- Short strings are **padded with spaces**.

#### 🔸 VARCHAR:
- **Variable-length** data type.
- Only stores the actual string length.
- **Space-efficient** – does not pad short strings.

**Summary Table:**

| Feature          | CHAR                         | VARCHAR                          |
|------------------|------------------------------|----------------------------------|
| Length           | Fixed                        | Variable                         |
| Storage          | Always same size             | Depends on string length         |
| Padding          | Yes, with spaces             | No padding                       |
| Use Case         | Short, fixed-length strings  | Variable-length strings          |

---

### 5. Explain the purpose of the WHERE clause in a SELECT statement.
**Answer:**  
The `WHERE` clause in a `SELECT` statement is used to **filter** the rows returned by the query.

It allows you to specify conditions that each row must satisfy to be included in the result set.

✅ **Key Uses:**
- Filtering Data
- Specific Data Retrieval
- Query Efficiency

---

### 6. What are the LIMIT and OFFSET clauses used for?
**Answer:**  
The `LIMIT` and `OFFSET` clauses control how many rows a query returns and from which point it starts.

#### ✅ LIMIT:
- Sets the **maximum number of rows** returned.

#### ✅ OFFSET:
- Skips a number of rows **before** starting to return data.

**Example:**
```sql
SELECT * FROM table LIMIT 10 OFFSET 20;
