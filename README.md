# 🎬 SQLBolt - Exercise 1

## 📌 Questions

1. **Find the title of each film**
2. **Find the director of each film**
3. **Find the title and director of each film**
4. **Find the title and year of each film**
5. **Find all the information about each film**

---

## 💻 Queries

### 1️⃣ Find the title of each film

```sql
SELECT title FROM Movies;
```

### 2️⃣ Find the director of each film

```sql
SELECT director FROM Movies;
```

### 3️⃣ Find the title and director of each film

```sql
SELECT title, director FROM Movies;
```

### 4️⃣ Find the title and year of each film

```sql
SELECT title, year FROM Movies;
```

### 5️⃣ Find all the information about each film

```sql
SELECT * FROM Movies;
```

---
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

### 2️⃣ Find movies released between 2000 and 2010

```sql
SELECT * FROM Movies
WHERE year BETWEEN 2000 AND 2010;
```

### 3️⃣ Find movies NOT released between 2000 and 2010

```sql
SELECT * FROM Movies
WHERE year NOT BETWEEN 2000 AND 2010;
```

### 4️⃣ Find the first 5 Pixar movies and their release year

```sql
SELECT title, year FROM Movies
LIMIT 5;
```

---
# 🎬 SQLBolt - Exercise 3

## 📌 Questions

1. **Find all the Toy Story movies**
2. **Find all the movies directed by John Lasseter**
3. **Find all the movies (and director) NOT directed by John Lasseter**
4. **Find all the WALL-* movies**

---

## 💻 Queries

### 1️⃣ Find all the Toy Story movies

```sql
SELECT * FROM Movies
WHERE title LIKE 'Toy Story%';
```

### 2️⃣ Find all movies directed by John Lasseter

```sql
SELECT * FROM Movies
WHERE director = 'John Lasseter';
```

### 3️⃣ Find movies NOT directed by John Lasseter

```sql
SELECT title, director FROM Movies
WHERE director != 'John Lasseter';
```

### 4️⃣ Find all WALL-* movies

```sql
SELECT * FROM Movies
WHERE title LIKE 'WALL-%';
```

---

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

### 2️⃣ List the last 4 movies (latest first)

```sql
SELECT * FROM Movies
ORDER BY year DESC
LIMIT 4;
```

### 3️⃣ List first 5 movies alphabetically

```sql
SELECT * FROM Movies
ORDER BY title ASC
LIMIT 5;
```

### 4️⃣ List next 5 movies alphabetically

```sql
SELECT * FROM Movies
ORDER BY title ASC
LIMIT 5 OFFSET 5;
```

---
# 🌎 SQLBolt - Exercise 5 (Review 1)

## 📌 Questions

1. **List all the Canadian cities and their populations**
2. **Order all the cities in the United States by their latitude from north to south**
3. **List all the cities west of Chicago, ordered from west to east**
4. **List the two largest cities in Mexico (by population)**
5. **List the third and fourth largest cities (by population) in the United States and their population**

---

## 💻 Queries

### 1️⃣ Canadian cities and their populations

```sql
SELECT city, population FROM north_american_cities
WHERE country = 'Canada';
```

### 2️⃣ US cities ordered by latitude (north → south)

```sql
SELECT * FROM north_american_cities
WHERE country = 'United States'
ORDER BY latitude DESC;
```

### 3️⃣ Cities west of Chicago (west → east)

```sql
SELECT * FROM north_american_cities
WHERE longitude < -87.6298
ORDER BY longitude ASC;
```

### 4️⃣ Two largest cities in Mexico

```sql
SELECT * FROM north_american_cities
WHERE country = 'Mexico'
ORDER BY population DESC
LIMIT 2;
```

### 5️⃣ 3rd and 4th largest US cities (by population)

```sql
SELECT city, population FROM north_american_cities
WHERE country = 'United States'
ORDER BY population DESC
LIMIT 2 OFFSET 2;
```

---






