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

### 📊 Output

| Title               |
| ------------------- |
| Toy Story           |
| A Bug's Life        |
| Toy Story 2         |
| Monsters, Inc.      |
| Finding Nemo        |
| The Incredibles     |
| Cars                |
| Ratatouille         |
| WALL-E              |
| Up                  |
| Toy Story 3         |
| Cars 2              |
| Brave               |
| Monsters University |

---

### 2️⃣ Find the director of each film

```sql
SELECT director FROM Movies;
```

### 📊 Output

| Director       |
| -------------- |
| John Lasseter  |
| John Lasseter  |
| John Lasseter  |
| Pete Docter    |
| Andrew Stanton |
| Brad Bird      |
| John Lasseter  |
| Brad Bird      |
| Andrew Stanton |
| Pete Docter    |
| Lee Unkrich    |
| John Lasseter  |
| Brenda Chapman |
| Dan Scanlon    |

---

### 3️⃣ Find the title and director of each film

```sql
SELECT title, director FROM Movies;
```

### 📊 Output

| Title               | Director       |
| ------------------- | -------------- |
| Toy Story           | John Lasseter  |
| A Bug's Life        | John Lasseter  |
| Toy Story 2         | John Lasseter  |
| Monsters, Inc.      | Pete Docter    |
| Finding Nemo        | Andrew Stanton |
| The Incredibles     | Brad Bird      |
| Cars                | John Lasseter  |
| Ratatouille         | Brad Bird      |
| WALL-E              | Andrew Stanton |
| Up                  | Pete Docter    |
| Toy Story 3         | Lee Unkrich    |
| Cars 2              | John Lasseter  |
| Brave               | Brenda Chapman |
| Monsters University | Dan Scanlon    |

---

### 4️⃣ Find the title and year of each film

```sql
SELECT title, year FROM Movies;
```

### 📊 Output

| Title               | Year |
| ------------------- | ---- |
| Toy Story           | 1995 |
| A Bug's Life        | 1998 |
| Toy Story 2         | 1999 |
| Monsters, Inc.      | 2001 |
| Finding Nemo        | 2003 |
| The Incredibles     | 2004 |
| Cars                | 2006 |
| Ratatouille         | 2007 |
| WALL-E              | 2008 |
| Up                  | 2009 |
| Toy Story 3         | 2010 |
| Cars 2              | 2011 |
| Brave               | 2012 |
| Monsters University | 2013 |

---

### 5️⃣ Find all the information about each film

```sql
SELECT * FROM Movies;
```

### 📊 Output

| ID | Title               | Director       | Year | Length (minutes) |
| -- | ------------------- | -------------- | ---- | ---------------- |
| 1  | Toy Story           | John Lasseter  | 1995 | 81               |
| 2  | A Bug's Life        | John Lasseter  | 1998 | 95               |
| 3  | Toy Story 2         | John Lasseter  | 1999 | 93               |
| 4  | Monsters, Inc.      | Pete Docter    | 2001 | 92               |
| 5  | Finding Nemo        | Andrew Stanton | 2003 | 107              |
| 6  | The Incredibles     | Brad Bird      | 2004 | 116              |
| 7  | Cars                | John Lasseter  | 2006 | 117              |
| 8  | Ratatouille         | Brad Bird      | 2007 | 115              |
| 9  | WALL-E              | Andrew Stanton | 2008 | 104              |
| 10 | Up                  | Pete Docter    | 2009 | 101              |
| 11 | Toy Story 3         | Lee Unkrich    | 2010 | 103              |
| 12 | Cars 2              | John Lasseter  | 2011 | 120              |
| 13 | Brave               | Brenda Chapman | 2012 | 102              |
| 14 | Monsters University | Dan Scanlon    | 2013 | 110              |

---

## 🚀 Notes

* `SELECT` → choose columns
* `*` → all columns
* Multiple columns → comma separated
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

### 📊 Output

| City     | Population |
| -------- | ---------- |
| Toronto  | 2795060    |
| Montreal | 1717767    |

---

### 2️⃣ US cities ordered by latitude (north → south)

```sql
SELECT * FROM north_american_cities
WHERE country = 'United States'
ORDER BY latitude DESC;
```

### 📊 Output

| City         | Country       | Population | Latitude  | Longitude   |
| ------------ | ------------- | ---------- | --------- | ----------- |
| Chicago      | United States | 2718782    | 41.878114 | -87.629798  |
| New York     | United States | 8405837    | 40.712784 | -74.005941  |
| Philadelphia | United States | 1553165    | 39.952584 | -75.165222  |
| Los Angeles  | United States | 3884307    | 34.052234 | -118.243685 |
| Phoenix      | United States | 1513367    | 33.448377 | -112.074037 |
| Houston      | United States | 2195914    | 29.760427 | -95.369803  |

---

### 3️⃣ Cities west of Chicago (west → east)

```sql
SELECT * FROM north_american_cities
WHERE longitude < -87.629798
ORDER BY longitude ASC;
```

### 📊 Output

| City                | Country       | Population | Latitude  | Longitude   |
| ------------------- | ------------- | ---------- | --------- | ----------- |
| Los Angeles         | United States | 3884307    | 34.052234 | -118.243685 |
| Phoenix             | United States | 1513367    | 33.448377 | -112.074037 |
| Guadalajara         | Mexico        | 1500800    | 20.659699 | -103.349609 |
| Mexico City         | Mexico        | 8555500    | 19.432608 | -99.133208  |
| Ecatepec de Morelos | Mexico        | 1742000    | 19.601841 | -99.050674  |
| Houston             | United States | 2195914    | 29.760427 | -95.369803  |

---

### 4️⃣ Two largest cities in Mexico

```sql
SELECT * FROM north_american_cities
WHERE country = 'Mexico'
ORDER BY population DESC
LIMIT 2;
```

### 📊 Output

| City                | Country | Population | Latitude  | Longitude  |
| ------------------- | ------- | ---------- | --------- | ---------- |
| Mexico City         | Mexico  | 8555500    | 19.432608 | -99.133208 |
| Ecatepec de Morelos | Mexico  | 1742000    | 19.601841 | -99.050674 |

---

### 5️⃣ 3rd and 4th largest US cities (by population)

```sql
SELECT city, population FROM north_american_cities
WHERE country = 'United States'
ORDER BY population DESC
LIMIT 2 OFFSET 2;
```

### 📊 Output

| City    | Population |
| ------- | ---------- |
| Chicago | 2718782    |
| Houston | 2195914    |

---

## 🚀 Notes

* `ORDER BY latitude DESC` → north to south
* `ORDER BY longitude ASC` → west to east
* `LIMIT` + `OFFSET` → ranking
* West → more negative longitude

