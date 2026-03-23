# 🎬 SQLBolt - Exercise 2

## 📌 Questions

1. **Find the movie with a row id of 6**
2. **Find the movies released between the years 2000 and 2010**
3. **Find the movies NOT released between the years 2000 and 2010**
4. **Find the first 5 Pixar movies and their release year**

---

## 💻 Queries

### 1️⃣ Find the movie with id = 6

```sql
SELECT * FROM Movies
WHERE id = 6;
```

### 📊 Output

| ID | Title           | Director  | Year | Length (minutes) |
| -- | --------------- | --------- | ---- | ---------------- |
| 6  | The Incredibles | Brad Bird | 2004 | 116              |

---

### 2️⃣ Movies released between 2000 and 2010

```sql
SELECT * FROM Movies
WHERE year BETWEEN 2000 AND 2010;
```

### 📊 Output

| ID | Title           | Director       | Year | Length (minutes) |
| -- | --------------- | -------------- | ---- | ---------------- |
| 4  | Monsters, Inc.  | Pete Docter    | 2001 | 92               |
| 5  | Finding Nemo    | Andrew Stanton | 2003 | 107              |
| 6  | The Incredibles | Brad Bird      | 2004 | 116              |
| 7  | Cars            | John Lasseter  | 2006 | 117              |
| 8  | Ratatouille     | Brad Bird      | 2007 | 115              |
| 9  | WALL-E          | Andrew Stanton | 2008 | 104              |
| 10 | Up              | Pete Docter    | 2009 | 101              |
| 11 | Toy Story 3     | Lee Unkrich    | 2010 | 103              |

---

### 3️⃣ Movies NOT released between 2000 and 2010

```sql
SELECT * FROM Movies
WHERE year NOT BETWEEN 2000 AND 2010;
```

### 📊 Output

| ID | Title               | Director       | Year | Length (minutes) |
| -- | ------------------- | -------------- | ---- | ---------------- |
| 1  | Toy Story           | John Lasseter  | 1995 | 81               |
| 2  | A Bug's Life        | John Lasseter  | 1998 | 95               |
| 3  | Toy Story 2         | John Lasseter  | 1999 | 93               |
| 12 | Cars 2              | John Lasseter  | 2011 | 120              |
| 13 | Brave               | Brenda Chapman | 2012 | 102              |
| 14 | Monsters University | Dan Scanlon    | 2013 | 110              |

---

### 4️⃣ First 5 Pixar movies and their release year

```sql
SELECT title, year FROM Movies
LIMIT 5;
```

### 📊 Output

| Title          | Year |
| -------------- | ---- |
| Toy Story      | 1995 |
| A Bug's Life   | 1998 |
| Toy Story 2    | 1999 |
| Monsters, Inc. | 2001 |
| Finding Nemo   | 2003 |

---

## 🚀 Notes

* `WHERE` → filter data
* `BETWEEN` → range select
* `NOT` → opposite condition
* `LIMIT` → restrict rows
