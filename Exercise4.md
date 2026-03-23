# 🎬 SQLBolt - Exercise 4

## 📌 Questions

1. **List all directors of Pixar movies (alphabetically), without duplicates**
2. **List the last four Pixar movies released (most recent to least)**
3. **List the first five Pixar movies sorted alphabetically**
4. **List the next five Pixar movies sorted alphabetically**

---

## 💻 Queries

### 1️⃣ List all directors (alphabetically, no duplicates)

```sql
SELECT DISTINCT director FROM Movies
ORDER BY director ASC;
```

### 📊 Output

| Director       |
| -------------- |
| Andrew Stanton |
| Brad Bird      |
| Brenda Chapman |
| Dan Scanlon    |
| John Lasseter  |
| Lee Unkrich    |
| Pete Docter    |

---

### 2️⃣ List the last 4 movies (latest first)

```sql
SELECT * FROM Movies
ORDER BY year DESC
LIMIT 4;
```

### 📊 Output

| ID | Title               | Director       | Year | Length (minutes) |
| -- | ------------------- | -------------- | ---- | ---------------- |
| 12 | Monsters University | Dan Scanlon    | 2013 | 110              |
| 5  | Brave               | Brenda Chapman | 2012 | 102              |
| 2  | Cars 2              | John Lasseter  | 2011 | 120              |
| 8  | Toy Story 3         | Lee Unkrich    | 2010 | 103              |

---

### 3️⃣ List first 5 movies alphabetically

```sql
SELECT * FROM Movies
ORDER BY title ASC
LIMIT 5;
```

### 📊 Output

| ID | Title        | Director       | Year | Length (minutes) |
| -- | ------------ | -------------- | ---- | ---------------- |
| 11 | A Bug's Life | John Lasseter  | 1998 | 95               |
| 5  | Brave        | Brenda Chapman | 2012 | 102              |
| 4  | Cars         | John Lasseter  | 2006 | 117              |
| 2  | Cars 2       | John Lasseter  | 2011 | 120              |
| 3  | Finding Nemo | Andrew Stanton | 2003 | 107              |

---

### 4️⃣ List next 5 movies alphabetically

```sql
SELECT * FROM Movies
ORDER BY title ASC
LIMIT 5 OFFSET 5;
```

### 📊 Output

| ID | Title               | Director      | Year | Length (minutes) |
| -- | ------------------- | ------------- | ---- | ---------------- |
| 1  | Monsters, Inc.      | Pete Docter   | 2001 | 92               |
| 12 | Monsters University | Dan Scanlon   | 2013 | 110              |
| 14 | Ratatouille         | Brad Bird     | 2007 | 115              |
| 6  | Toy Story           | John Lasseter | 1995 | 81               |
| 7  | Toy Story 2         | John Lasseter | 1999 | 93               |

---

## 🚀 Notes

* `DISTINCT` → remove duplicates
* `ORDER BY` → sorting
* `ASC` / `DESC` → order
* `LIMIT` → number of rows
* `OFFSET` → skip rows
