# 🎬 SQLBolt - Exercise 3

## 📌 Questions

1. **Find all the Toy Story movies**
2. **Find all the movies directed by John Lasseter**
3. **Find all the movies (and director) NOT directed by John Lasseter**
4. **Find all the WALL-* movies**

---

## 💻 Queries

### 1️⃣ Find all the Toy Story movies

```sql id="w9y7r2"
SELECT * FROM Movies
WHERE title LIKE 'Toy Story%';
```

### 📊 Output

| ID | Title       | Director      | Year | Length (minutes) |
| -- | ----------- | ------------- | ---- | ---------------- |
| 1  | Toy Story   | John Lasseter | 1995 | 81               |
| 3  | Toy Story 2 | John Lasseter | 1999 | 93               |
| 11 | Toy Story 3 | Lee Unkrich   | 2010 | 103              |

---

### 2️⃣ Find all movies directed by John Lasseter

```sql id="u0xq6p"
SELECT * FROM Movies
WHERE director = 'John Lasseter';
```

### 📊 Output

| ID | Title        | Director      | Year | Length (minutes) |
| -- | ------------ | ------------- | ---- | ---------------- |
| 1  | Toy Story    | John Lasseter | 1995 | 81               |
| 2  | A Bug's Life | John Lasseter | 1998 | 95               |
| 3  | Toy Story 2  | John Lasseter | 1999 | 93               |
| 7  | Cars         | John Lasseter | 2006 | 117              |
| 12 | Cars 2       | John Lasseter | 2011 | 120              |

---

### 3️⃣ Movies NOT directed by John Lasseter

```sql id="axn3tb"
SELECT title, director FROM Movies
WHERE director != 'John Lasseter';
```

### 📊 Output

| Title               | Director       |
| ------------------- | -------------- |
| Monsters, Inc.      | Pete Docter    |
| Finding Nemo        | Andrew Stanton |
| The Incredibles     | Brad Bird      |
| Ratatouille         | Brad Bird      |
| WALL-E              | Andrew Stanton |
| Up                  | Pete Docter    |
| Toy Story 3         | Lee Unkrich    |
| Brave               | Brenda Chapman |
| Monsters University | Dan Scanlon    |
| WALL-G              | Brenda Chapman |

---

### 4️⃣ Find all WALL-* movies

```sql id="7f1kzs"
SELECT * FROM Movies
WHERE title LIKE 'WALL-%';
```

### 📊 Output

| ID | Title  | Director       | Year | Length (minutes) |
| -- | ------ | -------------- | ---- | ---------------- |
| 9  | WALL-E | Andrew Stanton | 2008 | 104              |
| 87 | WALL-G | Brenda Chapman | 2042 | 97               |

---

## 🚀 Notes

* `LIKE` → pattern matching
* `%` → wildcard
* `'Toy Story%'` → starts with Toy Story
* `'WALL-%'` → starts with WALL-
* `!=` → not equal
