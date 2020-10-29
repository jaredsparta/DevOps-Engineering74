![](images/joins.png)


**What is it?**
- Can put data from several tables into one.
- It returns a table that:
    1. Has columns that are specified in the SELECT clause
    2. The rows are functions of data in the joined rows

- The left table is the table referred to in the FROM clause
- When joining three or more tables, it is the same syntax. Just remember that it joins tables line by line.
    - e.g. this would inner join t1 and t2 first AND THEN right join t3 to that table
    ```sql
        FROM t1
        INNER JOIN t2
        RIGHT JOIN t3
    ```

**Inner Join**
- Returns rows at the intersection of tables.
- i.e. the records that have matching values

**Left Join**
- Returns all records from the left table and the matched records from the right table

**Right Join**
- Returns all records from the right table and the matched records from the left table

---
**Used:**
- [Inner, Left, Right and Full Joins](http://www.sql-join.com/sql-join-types)

