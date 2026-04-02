## 🧠 Constraints 

---

### 📌 What are Constraints?

* Rules applied on columns to **control data**
* Ensure **data accuracy & integrity**

💡 Memory:
👉 “Constraints = restrictions for clean data”

---

## 📌 1. UNIQUE

👉 Ensures all values in a column are **different**

---

### 🔹 Normal Way (while creating table)

```sql
CREATE TABLE users (
  id INT,
  email VARCHAR(50) UNIQUE
);
```

---

### 🔹 Alter Way

```sql
ALTER TABLE users 
ADD CONSTRAINT unique_email UNIQUE (email);
```

---

## 📌 2. NOT NULL

👉 Column **cannot store NULL (empty value)**

---

### 🔹 Normal Way

```sql
CREATE TABLE users (
  id INT,
  name VARCHAR(50) NOT NULL
);
```

---

### 🔹 Alter Way

```sql
ALTER TABLE users 
MODIFY name VARCHAR(50) NOT NULL;
```

---

## 📌 3. CHECK

👉 Restricts values based on a condition

---

### 🔹 Normal Way

```sql
CREATE TABLE students (
  marks INT CHECK (marks >= 0)
);
```

---

### 🔹 Alter Way

```sql
ALTER TABLE students 
ADD CONSTRAINT chk_marks CHECK (marks >= 0);
```

---

## 📌 4. DEFAULT

👉 Sets a default value if none is provided

---

### 🔹 Normal Way

```sql
CREATE TABLE users (
  status VARCHAR(20) DEFAULT 'active'
);
```

---

### 🔹 Alter Way

```sql
ALTER TABLE users 
ALTER status SET DEFAULT 'active';
```

---

## 📌 5. Drop Constraint

```sql
ALTER TABLE table_name 
DROP CONSTRAINT constraint_name;
```

⚠️ Note:

* Syntax may vary slightly in MySQL
* Sometimes:

```sql
ALTER TABLE table_name DROP INDEX constraint_name;
```

---

## 🧠 Final Memory Summary

* UNIQUE → no duplicate values
* NOT NULL → no empty values
* CHECK → condition-based restriction
* DEFAULT → auto value
* ALTER → add/modify constraints

---

## 💡 Pro Tip (🔥 Important)

👉 Always give constraint names:

```sql
CONSTRAINT unique_email UNIQUE (email)
```

👉 Helps in:

* Dropping easily
* Debugging
* Professional code

---

## ⚡ Real Understanding

Without constraints:
👉 Data becomes messy 😬

With constraints:
👉 Data becomes reliable 💯


