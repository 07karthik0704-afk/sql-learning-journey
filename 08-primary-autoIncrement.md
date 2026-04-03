## 🧠 Primary Key

---

### 📌 What is Primary Key?

* Uniquely identifies each row in a table

💡 Combination of:
👉 **UNIQUE + NOT NULL**

---

## 📌 1. Normal Way (while creating table)

```sql
CREATE TABLE users (
  id INT PRIMARY KEY,
  name VARCHAR(50)
);
```

---

## 📌 2. Alter Way

```sql
ALTER TABLE users 
ADD PRIMARY KEY (id);
```

---

## ⚠️ Important Rules

* Only **one primary key per table**
* Cannot contain **NULL**
* No duplicate values

---

## 🧠 AUTO INCREMENT

---

### 📌 What is AUTO_INCREMENT?

* Automatically generates **incremented values**
* Used mostly with **Primary Key**

💡 Memory:
👉 “Next number automatically”

---

## 📌 1. Normal Way

```sql
CREATE TABLE users (
  id INT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(50)
);
```

---

## 📌 2. Alter Way

```sql
ALTER TABLE users 
MODIFY id INT AUTO_INCREMENT;
```

---

## 📌 Start from Specific Number

```sql
ALTER TABLE users AUTO_INCREMENT = 100;
```

👉 Next inserted row will start from **100**

---

## 🧠 Final Memory Summary

* PRIMARY KEY → UNIQUE + NOT NULL
* One per table
* AUTO_INCREMENT → auto number generation
* Can set starting value

---

## 💡 Pro Tip (🔥 Real World)

👉 Almost every table has:

```sql
id INT AUTO_INCREMENT PRIMARY KEY
```

👉 Why?

* Easy identification
* Fast queries
* Clean relationships (used in foreign keys later)

---

## ⚡ Real Understanding

Without Primary Key:
👉 Data becomes confusing 😬

With Primary Key:
👉 Each row has identity 💯

