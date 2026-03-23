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

