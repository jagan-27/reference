#### SQL

- Select all customers that starts with the letter "a":
```sql
SELECT * FROM Customers
WHERE CustomerName LIKE 'a%';
```
- Return all customers that ends with 'a':

```sql
SELECT * FROM Customers
WHERE CustomerName LIKE '%a';
```

- Return all customers that contains the phrase 'or'

```sql
SELECT * FROM Customers
WHERE CustomerName LIKE '%or%';
```

- The FULL OUTER JOIN keyword returns all matching records from both tables whether the other table matches or not. So, if there are rows in "Customers" that do not have matches in "Orders", or if there are rows in "Orders" that do not have matches in "Customers", those rows will be listed as well.


| CustomerName                        | OrderID |
|-------------------------------------|---------|
| Null                                | 10309   |
| Null                                | 10310   |
| Alfreds Futterkiste                | Null    |
| Ana Trujillo Emparedados y helados | 10308   |
| Antonio Moreno Taquería            | Null    |

- sample query

```sql
SELECT COUNT(CustomerID), Country
FROM Customers
GROUP BY Country
HAVING COUNT(CustomerID) > 5
ORDER BY COUNT(CustomerID) DESC;
```
