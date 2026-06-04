Conceptualization

## 1. Introduction
1.1 Business Purpose
The purpose of the Food Ordering System is to provide a convenient platform for customers to order food online. Many customers prefer ordering food through mobile applications instead of visiting restaurants directly. However, different restaurants often use different ordering methods, making the process inconvenient.
This system aims to simplify food ordering by providing a single platform where customers can browse menus, place orders, make payments, and track delivery status.
Restaurant managers can also manage menu information and customer orders through the system. This improves communication between customers and restaurants and increases operational efficiency.

1.2 Problem Statement
Traditional food ordering methods often require customers to contact restaurants directly or use multiple applications. Customers may have difficulty checking menu information, comparing prices, or tracking order status.
Restaurants also face challenges when managing customer orders and updating menu information. Manual processing can lead to delays and mistakes.
The Food Ordering System is proposed to solve these problems by providing an integrated platform for food ordering and restaurant management.

## 2. System Overview
The Food Ordering System consists of two main actors:
Customer
Restaurant Manager
Customers can register accounts, log in, browse restaurant menus, place food orders, make payments, and track order status.
Restaurant Managers can manage menu information and process customer orders.
The system is designed to improve convenience for customers while supporting efficient restaurant operations.

## 3. Stakeholders
Customer
Customers use the application to search for food, place orders, and monitor delivery status.
Interests
·  Easy ordering process
·  Fast payment
·  Accurate order tracking

Restaurant Manager
Restaurant managers maintain menu information and handle customer orders.
Interests
·  Efficient order processing
·  Easy menu management
·  Accurate customer information

## 4. Use Case Diagram
4.1 Use Case Overview
Figure shows the use case diagram of the Food Ordering System.
The system contains two primary actors: Customer and Restaurant Manager. Customers can register accounts, log in, browse menus, place orders, make payments, and track order status. Restaurant Managers can manage menu information and customer orders.
The use case diagram provides a high-level view of the interactions between users and the system.

4.2 Use Case List
UC01 Register
Actor: Customer
Description: The customer creates a new account by providing personal information such as email and password.
Precondition: The customer does not already have an account.
Postcondition: A new customer account is successfully created.

UC02 Login
Actor: Customer, Restaurant Manager
Description: The user enters account credentials to access the system.
Precondition: A valid account already exists.
Postcondition: The user is authenticated and gains access to the system.

UC03 Browse Menu
Actor: Customer
Description: The customer views restaurant information and available menu items.
Precondition: The customer is logged into the system.
Postcondition: Menu information is displayed.

UC04 Place Order
Actor: Customer
Description: The customer selects food items and submits an order request.
Precondition: Menu items have been selected.
Postcondition: A new order record is created.

UC05 Make Payment
Actor: Customer
Description: The customer completes payment for an existing order.
Precondition: An order has already been created.
Postcondition: Payment is verified and recorded.

UC06 Track Order
Actor: Customer
Description: The customer checks the current status of an order.
Precondition: The customer has an active order.
Postcondition: The latest order status is displayed.

UC07 Manage Menu
Actor: Restaurant Manager
Description: The restaurant manager adds, updates, or removes menu items.
Precondition: The manager is logged into the system.
Postcondition: Menu information is updated.

UC08 Manage Orders
Actor: Restaurant Manager
Description: The restaurant manager views and updates customer orders.
Precondition: Customer orders exist in the system.
Postcondition: Order status is updated successfully.

## 5. Concept of Operation
Register
Customers create a new account by entering personal information. The system validates the information and stores the account in the database.

Login
Customers and restaurant managers access the system using registered credentials.

Browse Menu
Customers can view restaurant information and browse available menu items.

Place Order
Customers select food items and submit an order request. The system creates an order record.

Make Payment
Customers complete payment using an available payment method. The system verifies the transaction before confirming the order.
Track Order
Customers can monitor the current status of their orders.

Manage Menu
Restaurant managers can add, update, and remove menu items.

Manage Orders
Restaurant managers can view customer orders and update order status.

## 6. Benefits of the System
The Food Ordering System provides several benefits.

Customer Benefits
·  Easy food ordering process
·  Convenient payment service
·  Real-time order tracking
·  Access to restaurant information

Restaurant Benefits
·  Efficient order management
·  Simplified menu maintenance
·  Better communication with customers
·  Reduced manual work

## 7. Glossary
Term	                    Description
Customer	        User who orders food through the application
Restaurant         Manager	User who manages menus and orders
Restaurant	        Food service provider
Menu	              List of food items available for ordering
Order	             Customer request for food
Payment	          Transaction process for an order
Delivery	        Transportation of food to customers
Database	        Storage system for application data
Authentication	  Process of verifying user identity

## 8. References
[1] Software Engineering Lecture Notes.
[2] UML Distilled, Martin Fowler.
[3] Java Documentation.
[4] MySQL Documentation.
[5] GitHub Documentation.
[6] Baemin Food Delivery Application.
[7] Yogiyo Food Delivery Application.
