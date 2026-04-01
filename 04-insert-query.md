# 🧠 INSERT Query – Revision Notes

---

## 📌 What is INSERT?

* Used to **add data into a table**

💡 Memory:
👉 INSERT = put data inside table

---

## 📌 1. Insert Single Row

### 🔹 Syntax

```sql
INSERT INTO table_name VALUES (value1, value2, value3);
```

### 🔹 Example

```sql
INSERT INTO students VALUES (1, 'Karthik', 85.50, '2003-05-10');
```

### 🔹 Points

* Must follow **column order**
* All values required

---

## 📌 2. Insert Multiple Rows

### 🔹 Syntax

```sql
INSERT INTO table_name VALUES 
(value1, value2, value3),
(value1, value2, value3);
```

### 🔹 Example

```sql
INSERT INTO students VALUES 
(2, 'Rahul', 78.00, '2002-03-12'),
(3, 'Anu', 92.25, '2003-07-21');
```

### 🔹 Points

* Insert multiple rows in one query
* Faster than writing multiple INSERTs

---

## 📌 3. Insert with Specific Columns

### 🔹 Syntax

```sql
INSERT INTO table_name (column1, column2) 
VALUES (value1, value2);
```

### 🔹 Example

```sql
INSERT INTO students (id, name) 
VALUES (4, 'Priya');
```

### 🔹 Points

* You can insert only selected columns
* Other columns → NULL or default

---

## ⚠️ Common Mistakes (Important)

* ❌ INSERT INTO table VALUES(...) → correct
* ❌ inser, intto → must be INSERT INTO
* ❌ wrong order of values → causes errors

---

## 🧠 Final Memory Summary

* INSERT INTO table VALUES(...) → single row
* INSERT INTO table VALUES(...),(...); → multiple rows
* INSERT INTO table (cols) VALUES(...); → specific columns

---

## 💡 Pro Tip (🔥)

### 🔹 Best Practice

```sql
INSERT INTO students (id, name, marks, dob) 
VALUES (1, 'Karthik', 85.50, '2003-05-10');
```

### 🔹 Why?

* Safer
* No confusion with column order
* Used in real projects

---
