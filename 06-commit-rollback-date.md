## 🧠 Transactions (COMMIT & ROLLBACK)

---

### 📌 What is a Transaction?

* A **group of SQL operations** executed together

💡 Memory:
👉 “All succeed or all fail”

---

## 📌 1. Auto Commit Mode

### 🔹 By Default:

* MySQL runs with:

```sql
AUTOCOMMIT = 1;
```

* Every query is **saved immediately**

---

### 🔹 Disable Auto Commit

```sql
SET AUTOCOMMIT = 0;
```

* Changes are **not saved automatically**
* You control when to save

---

## 📌 2. COMMIT

```sql
COMMIT;
```

* Permanently saves changes

💡 Memory:
👉 “CONFIRM changes”

---

## 📌 3. ROLLBACK

```sql
ROLLBACK;
```

* Undo changes (before commit)

💡 Memory:
👉 “GO BACK”

---

## 🔄 Example Flow (Important 🔥)

```sql
SET AUTOCOMMIT = 0;

UPDATE students SET marks = 100 WHERE id = 1;

ROLLBACK;  -- undo change

UPDATE students SET marks = 95 WHERE id = 1;

COMMIT;  -- save change
```

---

## ⚠️ Important Rules

* After `COMMIT` → cannot undo ❌
* `ROLLBACK` works only **before commit**
* Works with:

  * INSERT
  * UPDATE
  * DELETE

---

## 🧠 Final Memory Summary

* `SET AUTOCOMMIT = 0` → manual control
* `COMMIT` → save changes
* `ROLLBACK` → undo changes
* No commit → changes not permanent

---

## 💡 Pro Tip (🔥 Real World)

👉 Transactions are used in:

* Banking systems 💰
* Payment apps 💳

Example:

* Money deducted
* But not added to receiver → ❌
  👉 Transaction ensures both happen or none

---

## 🧠 Date & Time Functions – Revision Notes

---

### 📌 1. Current Date

```sql
CURRENT_DATE();
```

* Returns today’s date
* Format: `YYYY-MM-DD`

💡 Example:

```sql
SELECT CURRENT_DATE();
```

👉 Output:
`2026-04-01` (example)

---

### 📌 2. Current Date & Time

```sql
NOW();
```

* Returns current date **and** time
* Format: `YYYY-MM-DD HH:MM:SS`

💡 Example:

```sql
SELECT NOW();
```

👉 Output:
`2026-04-01 18:30:25`

---

### 📌 3. Current Time

```sql
CURRENT_TIME();
```

* Returns only time
* Format: `HH:MM:SS`

💡 Example:

```sql
SELECT CURRENT_TIME();
```

👉 Output:
`18:30:25`

---

## 🧠 Final Memory Summary

* `CURRENT_DATE()` → only date 📅
* `NOW()` → date + time 🕒
* `CURRENT_TIME()` → only time ⏰

---

## 💡 Real Use (🔥 Important)

👉 Auto insert date while adding data:

```sql
INSERT INTO students (name, joindate)
VALUES ('Karthik', CURRENT_DATE());
```

👉 Store exact timestamp:

```sql
INSERT INTO logs (action_time)
VALUES (NOW());
```

---

## ⚡ Pro Tip

* `NOW()` is most commonly used in real projects
* Useful for:

  * login time
  * order time
  * record creation

---





