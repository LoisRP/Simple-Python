# Project done for UBC Python course

This program consists of two Python files:
* query_orders_file.py
* find_elements_file.py
In addition, query_orders_file.py references northwind2.sqlite, a SQLite database file.

##Step 1:
Execute query_orders_file.py.

This generates the northwind_elements_demo.xml, based on a database query provided in the assignment. The results of the database query are transformed into XML, with the elements shaped by templates, and saved as the northwind_elements_demo.xml. In addition, any extended characters are replaced with characters in the Latin-1 character set.

##Step 2:
Execute find_elements_file.py. 

This file analyzes the contents of northwind_elements_demo.xml to find quantitative data. For example, which product had the highest quantity sold?

I answer these questions:
* What is the average total price of an order?
* What is the average number of products in an order?
* What is the order with the highest total cost, and what is the customer name and customer ID for that order?
* What is the product with the highest quantity sold, and what is the supplier name and supplier ID for that product?

To answer these questions, I do the following:

* Decompose the XML file into lists of elements. Each element in the file, other than nwind, ends up with a corresponding list, created with ElementTree. In addition, I create a customer ID list and customer name list with a length equal to the order details list, so that I can match up all three lists together.
* Count the number of orders.
* Count the number of order details.
* Sum up the total cost per order.
* Find the order with the highest cost.
* Find the customer for the highest-cost order.
* Find the average cost per order.
* Sum up the quantities sold for each product, and match the product to the supplier name and ID.

