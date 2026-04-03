## 🧠 Foreign Key – Revision Notes

---

### 📌 What is Foreign Key?

* Used to create a **relationship between two tables**

💡 Memory:
👉 “Connect one table to another”

---

### 📌 Why Foreign Key?

* Ensures **data integrity**
* Prevents invalid data

👉 Example:

* `orders` table refers to `users` table
* Order cannot exist without a valid user

---

## 📌 1. Normal Way (while creating table)

```sql id="2g6l7d"
CREATE TABLE orders (
  id INT PRIMARY KEY,
  user_id INT,
  FOREIGN KEY (user_id) REFERENCES users(id)
);
```

---

## 📌 2. Alter Way

```sql id="r5n0bx"
ALTER TABLE orders 
ADD CONSTRAINT fk_user 
FOREIGN KEY (user_id) REFERENCES users(id);
```

---

## 📌 3. Drop Foreign Key

```sql id="8h1c9n"
ALTER TABLE orders 
DROP FOREIGN KEY fk_user;
```

---

## 🧠 Final Memory Summary

* FOREIGN KEY → connects two tables
* Ensures valid data
* Cannot delete parent if child exists
* Can drop using constraint name
* Can control behavior (CASCADE, etc.)

