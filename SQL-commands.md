# SQL Commands
Some notes on useful and most used SQL commands.

Start MySQL on Terminal
```
sudo /usr/local/mysql/support-files/mysql.server start
```

Stop MySQL
```
sudo /usr/local/mysql/support-files/mysql.server stop
```

Restart MySQL
```
sudo /usr/local/mysql/support-files/mysql.server restart
```

Create Table
```
CREATE TABLE name (ID INT(6) AUTO_INCREMENT PRIMARY KEY, FirstName VARCHAR(30), SurnameVARCHAR(30), GenderVARCHAR(1));
```

Insert Data
```
INSERT INTO UEM.testing (`ID`, `First Name`, `Surname`, `Gender`) 
VALUES ('1', 'David', 'Tofan', 'M'),
('2', 'Name 2', 'Surname 2', 'F'),
('3', 'Name 3', 'Surname 3', 'M');
```

SUM Data
```
SELECT SUM(column) FROM table;
```
Count Data
```
SELECT COUNT(column) FROM table;
```

```
SELECT column, COUNT(*) AS new_column_name 
FROM table 
GROUP BY column;
```

```
SELECT column, COUNT(*) AS new_column_name 
FROM table WHERE column=“condition”
GROUP BY column, column2 DESC;
```

Total Data
```
SELECT SUM(column) / COUNT(*) AS new_column_name FROM table;
```

New Column Names
```
SELECT column AS new_column_name, 
column2 AS new_column_name
FROM table;
```

Average, Maximum, Minimum Data
```
SELECT AVG(column) AS new_column_name FROM table;
```

```
SELECT MAX(column) AS new_column_name FROM table;
```

```
SELECT MIN(column) AS new_column_name FROM table;
```

Calculate Data (2 requests)
```
SELECT column, column2, column3 / 
(SELECT SUM(column3) FROM table) * number AS new_column_name FROM table;
```

Distinct or Unique Data
```
SELECT DISTINCT column FROM table;
```

View Two Tables
```
SELECT * FROM table1, table2;
```

Update Values
```
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;
```

Alter / Add / Change Column Name
```
ALTER TABLE table CHANGE column new_column_name VARCHAR(30);
```

```
ALTER TABLE table ADD COLUMN column INT AFTER columnN;
```

Delete Record
```
DELETE FROM `table_name` [WHERE condition];
```

View Like
```
SELECT column1, column2, ...
FROM table_name
WHERE columnN LIKE pattern;
```

Delete entirely Table
```
DROP TABLE table_name;
```

Union of 2 tables
```
SELECT * FROM table UNION ALL SELECT * FROM table2;
```

InnerJoin to relate tables
```
SELECT * FROM table1 INNER JOIN table2
on table1.column = table2.column
```

