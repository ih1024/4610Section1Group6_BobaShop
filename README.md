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
![Data_Model_Link](relationshipModel.png)


# SQL Queries 
1. List all customer names and total amount they have spent (simple)
2. Drinks listed by most to least popular (simple)
3. Average amount spent per order (simple)
4. Total revenue by payment type (simple)
5. Toppings listed by most to least popular (complex)
6. Top customer by total spending (complex)
7. List the Employee of the month for each month (most orders) (complex)
8. List the customer name and the number of orders they have made where the amount on the total order was greater than the average total for all customers. (complex)
9. Percentage of customers participating in the loyalty program vs. not participating (complex)
10. Revenue contribution by category (complex)
11. List number of employees managed by each managed if any

# Data Dictionary
Customer:
![Customer Table](customerTable.png)
Drink Customization:
![Drink Customization Table](drinkCustomizationTable.png)
Drinks:
![Drinks Table](drinksTable.png)
Employee:
![Employee Table](employeeTable.png)
Food:
![Food Table](foodTable.png)
Loyalty:
![Loyalty Table](loyaltyTable.png)
Order Lineitem:
![Order Lineitem Table](orderLineitemTable.png)
Orders:
![Orders Table](ordersTable.png)
Payments:
![Payments Table](paymentsTable.png)
