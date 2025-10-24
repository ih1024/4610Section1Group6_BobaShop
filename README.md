# Team Name
59925_GroupProject1 - Tapioca Chews 

# Team Members 
1. Jay Tran
2. Sulema Gonzalez
3. Iris Huang
4. Abby Simmavanh
5. Julia Tardy

# Scenario
Tapioca Chews is a small but growing bubble tea shop located in downtown Athens. They’ve recently expanded their operations, adding online ordering, new fruit tea drinks, and new employees. Up to now they’ve been keeping track of orders and inventory using spreadsheets, but as the business grows, it’s becoming hard to manage efficiently and as questions arise such as order questions it is hard to answer. To modernize their operations, the owners want us to create an SQL database that stores and tracks all the key information about their business.
Since there is only one store location for Tapioca Chews, the owner wants to keep track of customers, menu items, orders, drinks, food, drink customizations, loyalty, payments, employees, and suppliers. More specifically, for customers, we want their first name, last name, phone, and email. For menu items we want drinks and food. For orders, we want to store the customer involved, the employee involved, and the time the interaction took place. As a small boba shop, we only have 2 bases: milk tea and fruit tea. We also offer food in two categories: dessert and appetizers. Tapioca Chews also offers add-ons for various prices. To encourage customer returns, we have started a rewards program and will need to track a customer’s points balance and the date they enrolled in the loyalty program. With that being said, we also need to collect information about payments made, such as the date, the payment type, and whether the amount was paid in full. In order to run Tapioca Chews, we need employees and we want to track employee first name, last name, phone, address, date starting, pay rate. 


# Entities 
1. Customers
2. Menu Items
3. Orders
4. Drinks
5. Food
6. Drink_Customizations
7. Loyalty
8. Payments
9. Employee
10. Tapioca Chews


# Data Model 
Explanation of Data Model: 

Our model is a hypothetical Boba Shop named Tapioca Chews. The Tapioca_Chews entity represents the physical store, which contains a unique storeId, street, city, and zipcode. Currently, the owners of Tapioca Chews have a singular brick-and-mortar location. That singular location contains many employees, which is why we have established a non-identifying one-to-many relationship, because the location can still exist without employees. Each Employee has their own unique employee number (empNo) as well as information stored on the employee, such as first name (firstName), last name (lastName), phone, and address. Additionally, there is a supervisor (superNo), and they are an employee who also manages other employees, which is why there is a recursive relationship. 

Each employee can take many orders from a customer, and the customer can also place multiple orders, which creates the associative entity “Orders”. In the Orders entity, we have a unique orderId as well as a TIMESTAMP for the date the order was made. The Customer entity contains a unique customerId, their last name (lastName), their first name (firstName), their phone, and email. One customer is allowed a singular loyalty account, which creates an identifying one-to-one relationship because there can not be a loyalty account for a customer who does not exist. In the Loyalty entity, we have their points balance (pointBal). 

Every order can have many items within that order, which generates an identifying one-to-many relationship, as the order can not exist without the order items. We have Drinks, Food, and Drink_Customizations entities that feed into the Order_Lineitem entity, which creates three one-to-many non-identity relationships, as you do not have to order everything, and null values are acceptable. The Drink_Customizations entity has a toppingId primary key as well as a price attribute. The Drinks entity has an itemId (PK) and attributes of category and price. The Food entity has a foodId (PK) and a foodName, and a price. 

At the end of the order, we expect payments, which lead to the creation of the Payments entity. This entity has a non-identifying one-to-many relationship with Orders because you can use multiple forms of payment for the same order. The attributes in the entity are as follows: paymentType, amount, and paidDate, as well as a unique paymentId. 

![Data_Model_Link](relationshipModel.png)


# SQL Queries 
1. List number of employees managed by each managed if any (simple)
2. Drinks listed by most to least popular (simple)
3. Average amount spent per order (simple)
4. Total revenue by payment type (simple)
5. Toppings listed by most to least popular (complex)
6. Top customer by total spending (complex)
7. List the Employee of the month for each month (most orders) (complex)
8. List the customer name and the number of orders they have made where the amount on the total order was greater than the average total for all customers. (complex)
9. Percentage of customers participating in the loyalty program vs. not participating (complex)
10. Revenue contribution by category (complex)

# Data Dictionary
1. Customer:
![Customer Table](customerTable.png)
2. Drink Customization:
![Drink Customization Table](drinkCustomizationTable.png)
3. Drinks:
![Drinks Table](drinksTable.png)
4. Employee:
![Employee Table](employeeTable.png)
5. Food:
![Food Table](foodTable.png)
6. Loyalty:
![Loyalty Table](loyaltyTable.png)
7. Order Lineitem:
![Order Lineitem Table](orderLineitemTable.png)
8. Orders:
![Orders Table](ordersTable.png)
9. Payments:
![Payments Table](paymentsTable.png)

# Data Base Information 
ns_F25MIST4610_59925_Group6

Additional information: Each query listed above is marked in the database using stored procedures which can be called using the following format: CALL TP_Qx;
