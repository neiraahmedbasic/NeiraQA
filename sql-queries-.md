# SQL Queries – Week 6

This document contains basic SQL queries for Week 6 homework, executed on the `hogwarts` database. Tasks cover SELECT, DELETE, aggregation, filtering, sorting, and usage of operators like IN, UNION, and HAVING.

---

### 1. Characters with known patronus

```sql
SELECT fname, lname, patronus 
FROM characters 
WHERE patronus IS NOT NULL AND patronus != 'Unknown';
```

---

### 2. Characters with last name ending in 'e'

```sql
SELECT lname
FROM characters 
WHERE lname LIKE '%e';
```

---

### 3. Sum of all characters' ages

```sql
SELECT SUM(age) AS ukupne_godine
FROM characters 
WHERE age IS NOT NULL;
```

---

### 4. Characters sorted by age (descending)

```sql
SELECT fname, lname, age 
FROM characters 
ORDER BY age DESC;
```

---

### 5. Characters aged between 50 and 100

```sql
SELECT fname, age
FROM characters 
WHERE age BETWEEN 50 AND 100;
```

---

### 6. Unique ages of characters

```sql
SELECT DISTINCT age 
FROM characters 
WHERE age IS NOT NULL;
```

---

### 7. Gryffindor characters older than 30

```sql
SELECT * 
FROM characters 
WHERE faculty = 'Gryffindor' AND age > 30;
```

---

### 8. First three unique faculty names

```sql
SELECT DISTINCT faculty
FROM characters 
LIMIT 3;
```

---

### 9. Names starting with 'N' and 5 letters long or starting with 'L'

```sql
SELECT fname
FROM characters
WHERE (fname LIKE 'N____' OR fname LIKE 'L%');
```

---

### 10. Average age of characters

```sql
SELECT AVG(age) AS prosecne_godine
FROM characters 
WHERE age IS NOT NULL;
```

---

### 11. Delete character with ID = 11

```sql
DELETE FROM characters
WHERE char_id = 11;
```

---

### 12. Last names containing the letter 'a'

```sql
SELECT lname
FROM characters 
WHERE lname LIKE '%a%'; 
```

---

### 13. Rename column 'fname' to alias 'Half-Blood Prince'

```sql
SELECT fname AS 'Half-Blood Prince' 
FROM characters;
```

---

### 14. Patronus names sorted alphabetically (excluding unknown)

```sql
SELECT char_id, patronus
FROM characters
WHERE patronus IS NOT NULL AND patronus != 'Unknown' 
ORDER BY patronus ASC;
```

---

### 15. Characters with last name Crabbe, Granger, or Diggory

```sql
SELECT fname, lname 
FROM characters 
WHERE lname IN ('Crabbe', 'Granger', 'Diggory');
```

---

### 16. Minimum age among characters

```sql
SELECT MIN(age) AS minimalne_godine
FROM characters 
WHERE age IS NOT NULL;
```

---

### 17. Combine character names and book titles (UNION)

```sql
SELECT fname
FROM characters 

UNION 

SELECT book_name 
FROM library;
```

---

### 18. Faculties with more than 1 character

```sql
SELECT faculty, COUNT(*) AS broj_likova 
FROM characters 
GROUP BY faculty 
HAVING COUNT(*) > 1;
```

---

**Database:** `hogwarts`
