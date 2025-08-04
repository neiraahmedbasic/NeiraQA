# SQL Queries – Week 6

This document contains basic SQL queries for Week 6 homework, executed on the `hogwarts` database. Tasks cover SELECT, DELETE, aggregation, filtering, sorting, and usage of operators like IN, UNION, and HAVING.

---
### 1. Display first name, last name, and patronus of characters with known patronus:
```sql
SELECT fname, lname, patronus 
FROM characters 
WHERE NOT patronus = 'Unknown' AND patronus IS NOT NULL;
```

### 2. Display last names ending with 'e':
```sql
SELECT lname
FROM characters 
WHERE lname LIKE '%e';
```

### 3. Calculate total age of all characters:
```sql
SELECT SUM(age) AS "Total age"
FROM characters;
```

### 4. List characters ordered by age descending:
```sql
SELECT fname, lname, age 
FROM characters 
ORDER BY age DESC;
```

### 5. Characters aged between 50 and 100:
```sql
SELECT fname, age
FROM characters 
WHERE age BETWEEN 50 AND 100;
```

### 6. List unique ages:
```sql
SELECT DISTINCT age 
FROM characters;
```

### 7. Gryffindor characters older than 30:
```sql
SELECT * 
FROM characters 
WHERE faculty = 'Gryffindor' AND age > 30;
```

### 8. Display first 3 unique faculties:
```sql
SELECT DISTINCT faculty
FROM characters 
LIMIT 3;
```

### 9. Names starting with 'N' and 5 letters or starting with 'L':
```sql
SELECT fname
FROM characters
WHERE (fname LIKE 'N____' OR fname LIKE 'L%');
```

### 10. Average age of characters:
```sql
SELECT AVG(age) AS "Average age"
FROM characters;
```

### 11. Delete character with ID = 11:
```sql
DELETE FROM characters
WHERE id = 11;
```

### 12. Last names containing the letter 'a':
```sql
SELECT lname
FROM characters 
WHERE lname LIKE '%a%'; 
```

### 13. Alias `fname` as 'Half-Blood Prince':
```sql
SELECT fname AS "Half-Blood Prince" 
FROM characters;
```

### 14. List known patronuses with character ID (sorted):
```sql
SELECT char_id, patronus
FROM characters
WHERE NOT patronus = 'Unknown' AND patronus IS NOT NULL
ORDER BY patronus ASC;
```

### 15. Names of characters with specific last names:
```sql
SELECT fname, lname 
FROM characters 
WHERE lname IN ('Crabbe', 'Granger', 'Diggory');
```

### 16. Display minimal age:
```sql
SELECT MIN(age) AS minimal_age
FROM characters;
```

### 17. Combine character names and book titles:
```sql
SELECT fname AS name
FROM characters 
UNION 
SELECT book_name AS name
FROM library;
```

### 18. Faculties with more than one character:
```sql
SELECT faculty, COUNT(*) AS student_count
FROM characters 
GROUP BY faculty 
HAVING COUNT(*) > 1;

**Database:** `hogwarts`
