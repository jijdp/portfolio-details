SQL command on MySQL




1.

```sql
use HPlus;

SELECT * FROM Customer WHERE CustomerID = 974;
```
![sql1](https://github.com/jijdp/portfolio-details/assets/138129390/d8d6e349-b7ad-437a-af1d-947fcb0e9f36)

2.

```sql
USE HPlus;

SELECT OrderID, TotalDue, Status, CustomerID FROM Orders WHERE TotalDue > 300 AND Status IN ('PAST DUE','DUE');
```
![sql2](https://github.com/jijdp/portfolio-details/assets/138129390/a255101d-4170-4113-81c1-99c3d4cf4143)

3.

use tutorial;

INSERT INTO Customer (FirstName, LastName) VALUE ('Jidapa', 'Dee');
![sql3](https://github.com/jijdp/portfolio-details/assets/138129390/00c1cbe7-f1c3-43b4-9f12-39df23676492)

4.

use tutorial;

DELETE FROM Customer WHERE CustomerID = 4;
SELECT * FROM Customer;
![sql4](https://github.com/jijdp/portfolio-details/assets/138129390/476bdb56-81e4-42c9-88ba-492b9beb4e5b)

5.

USE tutorial;

UPDATE Orders2 SET OrderStatus = 'Paid' WHERE OrderID = 1;
SELECT * FROM orders2;
![sql5](https://github.com/jijdp/portfolio-details/assets/138129390/42bc2dbb-5156-4d75-a8f6-b59ed672b095)

6.

use HPlus;

SELECT COUNT(OrderID) FROM Orders WHERE TotalDue > 300 AND Status IN ('PAST DUE','DUE');
![sql6](https://github.com/jijdp/portfolio-details/assets/138129390/b9ee8e08-e5cb-42db-a443-40c8c48dfaab)

7.

use HPlus;

SELECT SUM(TotalDue) FROM Orders WHERE TotalDue > 300 AND Status IN ('PAST DUE','DUE');
![sql7](https://github.com/jijdp/portfolio-details/assets/138129390/9eab1a93-3148-48e3-b824-7817c7583e95)

8.

USE HPlus;

SELECT Orders.OrderID, Customer.FirstName, Orders.Status
FROM Orders
INNER JOIN Customer ON Orders.CustomerID = Customer.CustomerID;
![sql8](https://github.com/jijdp/portfolio-details/assets/138129390/49686497-ebc7-44b2-971f-e5d9b9f6e794)

9.

USE HPlus;

SELECT Customer.FirstName, Customer.LastName, Orders.OrderID
FROM Customer
LEFT JOIN Orders ON Customer.CustomerID = Orders.CustomerID;
![sql9](https://github.com/jijdp/portfolio-details/assets/138129390/a0ccebff-c6f4-4a71-be6e-5d2385239e3c)

10.

USE HPlus;

SELECT Orders.OrderID, Salesperson.LastName, Salesperson.FirstName
FROM Orders
RIGHT JOIN Salesperson ON Orders.SalespersonID = Salesperson.SalespersonID;
![sql10](https://github.com/jijdp/portfolio-details/assets/138129390/d8a9dbd0-f9cc-4614-921b-bf6d4528e343)

11.
USE HPlus;

SELECT Customer.LastName, Orders.OrderID
FROM Customer
CROSS JOIN Orders;
![sql11](https://github.com/jijdp/portfolio-details/assets/138129390/75f8e3a6-a2f6-46e4-a592-3c39bf6ec53d)

12.
use HPlus;

SELECT ProductName, MIN(Price) FROM Product GROUP BY ProductName;
![sql12](https://github.com/jijdp/portfolio-details/assets/138129390/771a919b-0c76-4764-9589-b2c457deda6d)

13.
use HPlus;

SELECT FirstName, LastName FROM Salesperson WHERE FirstName LIKE 'Ja%';
![sql13](https://github.com/jijdp/portfolio-details/assets/138129390/ae6f0e66-981c-4359-adaf-1756940f837e)

14.
use HPlus;

SELECT COUNT(LastName), City FROM Customer GROUP BY City;
![sql14](https://github.com/jijdp/portfolio-details/assets/138129390/a578f312-969f-4857-a293-bb640f39ddf7)

15.
use Hplus;

CALL GetOrderByStatus('past due');
![sql15](https://github.com/jijdp/portfolio-details/assets/138129390/7f2d04b8-d365-49c0-bc74-683e89a9d06f)

16.
use HPlus;

SHOW INDEX FROM Salesperson;
![sql16](https://github.com/jijdp/portfolio-details/assets/138129390/e7898b29-ae40-4e16-af7a-4cf3913e7333)
