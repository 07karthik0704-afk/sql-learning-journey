## 🧠 SELECT Query – Revision Notes

---

### 📌 What is SELECT?

* Used to **retrieve (read) data from a table**

💡 Memory:
👉 “SELECT = get data”

---

## 📌 1. Select All Columns

```sql
SELECT * FROM table_name;
```

💡 Example:

```sql
SELECT * FROM students;
```

* Fetches **all columns + all rows**

---

## 📌 2. Select Specific Columns

```sql
SELECT column1, column2 FROM table_name;
```

💡 Example:

```sql
SELECT name, marks FROM students;
```

* Fetches only selected columns
* Faster & cleaner than `*`

---

## 📌 3. Column Alias (AS)

```sql
SELECT column_name AS new_name FROM table_name;
```

💡 Example:

```sql
SELECT name AS student_name FROM students;
```

* Renames column in output
* Does NOT change actual table

---

## 📌 4. Conditions (WHERE Clause)

👉 Used to filter data

```sql
SELECT * FROM table_name WHERE condition;
```

---

### 🔹 Comparison Operators

* `=` → equal
* `!=` → not equal
* `>` → greater than
* `<` → less than

💡 Example:

```sql
SELECT * FROM students WHERE marks > 80;
```

---

### 🔹 NULL Conditions

* `IS NULL` → checks empty value
* `IS NOT NULL` → checks non-empty

💡 Example:

```sql
SELECT * FROM students WHERE marks IS NULL;
```

---

## ⚠️ Important Notes

* ❌ Don’t write: `= NULL`
* ✅ Always use: `IS NULL`

---

## 🧠 Final Memory Summary

* `SELECT *` → all data
* `SELECT col1, col2` → specific data
* `AS` → rename column
* `WHERE` → filter data
* Operators → `= != > <`
* NULL → `IS NULL / IS NOT NULL`

---

## 💡 Pro Tip (🔥 Real Use)

👉 Combine everything:

```sql
SELECT name AS student_name, marks 
FROM students 
WHERE marks > 80;
```

👉 This is how real queries look in projects

---


## 🧠 UPDATE Query – Revision Notes

---

### 📌 What is UPDATE?

* Used to **modify existing data in a table**

💡 Memory:
👉 “UPDATE = change existing data”

---

## 📌 1. Basic Syntax

```sql
UPDATE table_name 
SET column_name = value 
WHERE condition;
```

💡 Example:

```sql
UPDATE students 
SET joindate = '2024-01-01' 
WHERE id = 1;
```

* Updates only rows that match the condition

---

## 📌 2. Update Multiple Columns

```sql
UPDATE table_name 
SET column1 = value1,
    column2 = value2
WHERE condition;
```

💡 Example:

```sql
UPDATE students 
SET name = 'Karthik',
    marks = 90
WHERE id = 1;
```

* Use **comma (,)** to update multiple columns

---

## ⚠️ VERY IMPORTANT

👉 If you don’t use `WHERE`:

```sql
UPDATE students SET marks = 100;
```

💥 This will update **ALL rows**

---

## 🧠 Safe Update Mode (MySQL)

### 📌 What is Safe Mode?

* Prevents updating or deleting data **without WHERE condition**
* Protects you from mistakes

---

### 📌 Disable Safe Mode

```sql
SET SQL_SAFE_UPDATES = 0;
```

👉 Allows update without strict conditions

---

### 📌 Enable Safe Mode

```sql
SET SQL_SAFE_UPDATES = 1;
```

👉 Restricts unsafe updates

---

👉 syntax:

```sql
SET SQL_SAFE_UPDATES = 0;
```

---

## 🧠 Final Memory Summary

* `UPDATE table SET col=value WHERE condition`
* Use comma → update multiple columns
* Without WHERE → updates all rows ⚠️
* Safe mode → prevents mistakes
* Disable → `SET SQL_SAFE_UPDATES = 0`

---

## 💡 Pro Tip (🔥 Interview Level)

👉 Always use:

```sql
SELECT * FROM table WHERE condition;
```

Before running UPDATE

👉 This ensures you update **correct rows only**

---


## 🧠 DELETE Query – Revision Notes

---

### 📌 What is DELETE?

* Used to **remove data (rows) from a table**

💡 Memory:
👉 “DELETE = remove data”

---

## 📌 1. Basic Syntax

```sql
DELETE FROM table_name 
WHERE condition;
```

💡 Example:

```sql
DELETE FROM employees 
WHERE id = 1;
```

* Deletes only the row that matches the condition

---

## ⚠️ VERY IMPORTANT

👉 If you don’t use `WHERE`:

```sql
DELETE FROM employees;
```

💥 This will delete **ALL rows in the table**

---

## 📌 Difference (Important)

| Command | What it does                            |
| ------- | --------------------------------------- |
| DELETE  | Removes data (rows only)                |
| DROP    | Deletes entire table (structure + data) |

---

## 🧠 Final Memory Summary

* `DELETE FROM table WHERE condition` → delete specific row
* Without `WHERE` → deletes all data ⚠️
* DELETE ≠ DROP

---

## 💡 Pro Tip (🔥 Must Follow)

Before DELETE, always check:

```sql
SELECT * FROM employees WHERE id = 1;
```

👉 This prevents accidental data loss

---

## ⚡ Real Talk

This command is **very powerful**—in real companies:

* One wrong DELETE = data gone 😬
* That’s why people double-check always

---




