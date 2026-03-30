# 📚 MySql Database Commands

A quick reference for basic MySQL database operations.

---

## 📌 1. Show Databases

```sql
SHOW DATABASES;
```

**Description:**
Displays all databases present in MySQL.

💡 **Memory Trick:**
👉 “Show me everything available”

---

## 📌 2. Create Database

```sql
CREATE DATABASE database_name;
```

**Description:**
Creates a new database.

💡 **Example:**

```sql
CREATE DATABASE student_db;
```

💡 **Tip:**
👉 Use meaningful names like `student_db`, `ecommerce_db`

---

## 📌 3. Use Database

```sql
USE database_name;
```

**Description:**
Selects the database to work on.

💡 **Example:**

```sql
USE student_db;
```

💡 **Memory Trick:**
👉 “Now I’m working inside this database”

---

## 📌 4. Alter Database

```sql
alter database read only = 1 ;
```

👉 “It will chnage only to the read only format mode”

```sql
alter database read only = 0 ;
```

👉 “By default it will be like above (edit mode)”

## ✅ Summary

| Command           | Purpose                        |
| ----------------- | ------------------------------ |
| `SHOW DATABASES`  | List all databases             |
| `CREATE DATABASE` | Create a new database          |
| `USE`             | Select a database to work with |
