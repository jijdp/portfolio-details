SQL command on MySQL
1.Basic Create Database
![image]()

2.

use HPlus;

SELECT * FROM Customer WHERE CustomerID = 974;

3.

USE HPlus;

SELECT OrderID, TotalDue, Status, CustomerID FROM Orders WHERE TotalDue > 300 AND Status IN ('PAST DUE','DUE');

4.

use tutorial;

INSERT INTO Customer (FirstName, LastName) VALUE ('Jidapa', 'Dee');

5.

use tutorial;

DELETE FROM Customer WHERE CustomerID = 4;
SELECT * FROM Customer;

6.

USE tutorial;

UPDATE Orders2 SET OrderStatus = 'Paid' WHERE OrderID = 1;
SELECT * FROM orders2;

7.

use HPlus;

SELECT COUNT(OrderID) FROM Orders WHERE TotalDue > 300 AND Status IN ('PAST DUE','DUE');

8.

use HPlus;

SELECT SUM(TotalDue) FROM Orders WHERE TotalDue > 300 AND Status IN ('PAST DUE','DUE');

9.

USE HPlus;

SELECT Orders.OrderID, Customer.FirstName, Orders.Status
FROM Orders
INNER JOIN Customer ON Orders.CustomerID = Customer.CustomerID;

10.

USE HPlus;

SELECT Customer.FirstName, Customer.LastName, Orders.OrderID
FROM Customer
LEFT JOIN Orders ON Customer.CustomerID = Orders.CustomerID;

USE HPlus;

SELECT Orders.OrderID, Salesperson.LastName, Salesperson.FirstName
FROM Orders
RIGHT JOIN Salesperson ON Orders.SalespersonID = Salesperson.SalespersonID;
