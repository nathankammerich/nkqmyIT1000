# Nav Bar
[Home Page](README.md) \
[Page 2 (Links)](page2.md) \
[Page 3 (Images)](page3.md) \
[Page 4 (Classes)](page4.md) \
***Page 5 (Code)*** 

# Block of Code from my database class (SQL)

CREATE VIEW orderTotals AS
SELECT od.orderNumber, c.customerName, od.priceEach * od.quantityOrdered AS total
FROM orderdetails od, customers c, orders o
GROUP BY o.customerNumber = c.customerNumber, o.orderNumber = od.orderNumber;

SELECT *
FROM orderTotals
ORDER BY total DESC
LIMIT 15;