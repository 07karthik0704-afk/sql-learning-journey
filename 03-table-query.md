# 🧠 Table Queries 

Core SQL concepts for working with tables.

---

## 📌 1. Create Table

```sql
CREATE TABLE table_name (
  column1 datatype,
  column2 datatype
);
```

💡 **Example:**

```sql
CREATE TABLE students (
  id INT,
  name VARCHAR(50),
  marks DECIMAL(5,2),
  dob DATE
);
```

* Used to create a new table
* Define columns and their data types

---

## 📌 2. Common Data Types

* **INT** → whole numbers
* **VARCHAR(n)** → text (variable length)
* **DECIMAL(p,s)** → numbers with precision

  * `p` = total digits
  * `s` = digits after decimal
* **DATE** → date values (`YYYY-MM-DD`)

💡 **Example:**

```sql
marks DECIMAL(5,2); -- 999.99
```

---

## 📌 3. Select (Read Data)

```sql
SELECT * FROM table_name;
```

* Fetch all data from table

💡 **Specific columns:**

```sql
SELECT name, marks FROM students;
```

---

## 📌 4. Rename Table

```sql
RENAME TABLE old_name TO new_name;
```

💡 **Example:**

```sql
RENAME TABLE students TO student_data;
```

---

## 📌 5. Drop Table

```sql
DROP TABLE table_name;
```

⚠️ **Warning:** Deletes table completely (structure + data)

---

## 📌 6. Alter Table

Used to modify an existing table.

---

### ➕ Add Column

```sql
ALTER TABLE table_name ADD column_name datatype;
```

---

### ✏️ Rename Column

```sql
ALTER TABLE table_name RENAME COLUMN old_name TO new_name;
```

---

### 🔄 Modify Column

```sql
ALTER TABLE table_name MODIFY column_name datatype;
```

---

### 📍 Position Control

👉 **FIRST**

```sql
ALTER TABLE table_name MODIFY column_name datatype FIRST;
```

👉 **AFTER another column**

```sql
ALTER TABLE table_name MODIFY column_name datatype AFTER column_name;
```

---

### ❌ Drop Column

```sql
ALTER TABLE table_name DROP COLUMN column_name;
```

---

## 🧠 Final Memory Summary

* **CREATE** → create table
* **SELECT** → read data
* **RENAME** → rename table
* **DROP** → delete table
* **ALTER** → change structure

  * ADD
  * MODIFY
  * RENAME
  * DROP

---

## 💡 Pro Tip (🔥 Interview Level)

👉 **Difference: DROP vs DELETE**

* `DROP TABLE` → removes entire table
* `DELETE` → removes only data (we’ll learn later)
