SQL command on MySQL



1.

use HPlus;

SELECT * FROM Customer WHERE CustomerID = 974;

2.

USE HPlus;

SELECT OrderID, TotalDue, Status, CustomerID FROM Orders WHERE TotalDue > 300 AND Status IN ('PAST DUE','DUE');

3.

use tutorial;

INSERT INTO Customer (FirstName, LastName) VALUE ('Jidapa', 'Dee');

4.

use tutorial;

DELETE FROM Customer WHERE CustomerID = 4;
SELECT * FROM Customer;

5.

USE tutorial;

UPDATE Orders2 SET OrderStatus = 'Paid' WHERE OrderID = 1;
SELECT * FROM orders2;

6.

use HPlus;

SELECT COUNT(OrderID) FROM Orders WHERE TotalDue > 300 AND Status IN ('PAST DUE','DUE');

7.

use HPlus;

SELECT SUM(TotalDue) FROM Orders WHERE TotalDue > 300 AND Status IN ('PAST DUE','DUE');

8.

USE HPlus;

SELECT Orders.OrderID, Customer.FirstName, Orders.Status
FROM Orders
INNER JOIN Customer ON Orders.CustomerID = Customer.CustomerID;

9.

USE HPlus;

SELECT Customer.FirstName, Customer.LastName, Orders.OrderID
FROM Customer
LEFT JOIN Orders ON Customer.CustomerID = Orders.CustomerID;

10.

USE HPlus;

SELECT Orders.OrderID, Salesperson.LastName, Salesperson.FirstName
FROM Orders
RIGHT JOIN Salesperson ON Orders.SalespersonID = Salesperson.SalespersonID;
