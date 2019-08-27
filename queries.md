# Database Queries

### Display the ProductName and CategoryName for all products in the database. Shows 76 records.
SELECT P.ProductName, C.CategoryName
FROM Products AS P
JOIN Categories AS C ON P.CategoryID = C.CategoryID


### Display the OrderID and ShipperName for all orders placed before January 9, 1997. Shows 161 records.
SELECT O.OrderID, S.ShipperName
FROM Orders AS O
JOIN Shippers AS S ON O.ShipperID = S.ShipperID


### Display all ProductNames and Quantities placed on order 10251. Sort by ProductName. Shows 3 records.
SELECT P.ProductName, OD.Quantity
FROM OrderDetails AS OD
JOIN Products as P ON OD.ProductID = P.ProductID
WHERE OD.OrderID = 10251
ORDER BY P.ProductName


### Display the OrderID, CustomerName and the employee's LastName for every order. All columns should be labeled clearly. Displays 196 records.
SELECT O.OrderID, CustomerName AS "Customer Name", LastName AS "Employee Last Name"
FROM Orders AS O
JOIN Customers AS C ON C.CustomerID = O.CustomerID
JOIN Employees AS E ON E.EmployeeID = O.EmployeeID


### (Stretch)  Displays CategoryName and a new column called Count that shows how many products are in each category. Shows 9 records.

### (Stretch) Display OrderID and a  column called ItemCount that shows the total number of products placed on the order. Shows 196 records. 