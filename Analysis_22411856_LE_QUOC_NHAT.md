## Analysis

## 1. Introduction
1.1 Purpose

The purpose of this document is to analyze the requirements of the Food Ordering System before implementation. This analysis document identifies the main functions of the system, user requirements, and business processes.
The system is designed to provide a convenient environment where customers can order food online and track their orders. Restaurant managers can manage menu information and customer orders through the same platform.
The results of this analysis will be used as the basis for the design and implementation phases.

1.2 System Overview

The Food Ordering System is an application that connects customers and restaurants.
Customers can create accounts, browse restaurant menus, place food orders, make payments, and check delivery status. Restaurant managers can update menu information and process customer orders.
The system aims to simplify the ordering process and improve communication between customers and restaurants.
1.3 Actors
Customer
The Customer is the primary user of the system. Customers can search menus, place orders, make payments, and track deliveries.
Restaurant Manager
The Restaurant Manager is responsible for maintaining restaurant information. Managers can modify menu items and update order status during processing.

## 2. Functional Requirements
FR01 Register
Customers must be able to create a new account using personal information such as email and password.
The system validates the entered information before creating the account.

FR02 Login
Registered users must be able to log into the system using their account credentials.
The system verifies the entered information before granting access.
FR03 Browse Menu
Customers must be able to view restaurant information and available menu items.

Menu information includes food names and prices.

FR04 Place Order
Customers must be able to select food items and create an order.

The system stores the order information in the database.

FR05 Make Payment
Customers must be able to complete payment after creating an order.

The system verifies payment information and records the transaction result.

FR06 Track Order
Customers must be able to check the current status of their orders.
The system displays information such as preparing, delivering, or delivered.

FR07 Manage Menu
Restaurant Managers must be able to add, update, and remove menu items.
The system stores all menu modifications in the database.

FR08 Manage Orders
Restaurant Managers must be able to view customer orders and update order status.
The updated information must be visible to customers.

## 3. Non-Functional Requirements
NFR01 Security
User information and payment information must be protected from unauthorized access.
Authentication is required before accessing system functions.

NFR02 Performance
The system should respond to user requests within a reasonable time.
Menu loading and order processing should not cause significant delays.

NFR03 Availability
The system should be available whenever customers want to place orders.
System downtime should be minimized.

NFR04 Usability
The user interface should be simple and easy to understand.
Customers should be able to complete food orders without difficulty.

NFR05 Maintainability
The system should be designed so that future updates and modifications can be performed easily.
Object-oriented design principles should be applied.

## 4. Use Case Analysis
Use Case Diagram Overview

Figure shows the use case diagram of the Food Ordering System.
The system contains two primary actors: Customer and Restaurant Manager. Customers can register accounts, log in, browse restaurant menus, place orders, make payments, and track delivery status. Restaurant Managers are responsible for managing menu information and processing customer orders.
The use case diagram provides a high-level view of the system requirements and user interactions. Each use case represents a functional requirement that the system must support.
The identified use cases will be analyzed in detail in the following sections and will serve as the basis for the design phase.

UC01 Register
Item	        Description
Use Case	    Register
Primary       Actor	Customer
Description	  Create a new account
Precondition	Customer does not have an account
Postcondition	New account is created
The Register use case allows new users to join the system. The customer enters personal information and submits the registration form. The system validates the information and stores the account in the database.

UC02 Login
Item	          Description
Use Case	      Login
Primary         Actor	Customer
Description	    Access the system
Precondition	  Registered account exists
Postcondition	  User session is created
The Login use case verifies customer credentials. After successful authentication, the customer can access the services provided by the system.

UC03 Browse Menu
Item	          Description
Use Case	      Browse Menu
Primary         Actor	Customer
Description	     View menu information
Precondition	  User is logged in
Postcondition	  Menu information displayed
Customers can browse restaurant menus before placing orders. The system retrieves menu information and displays it on the screen.

UC04 Place Order
Item	        Description
Use Case	    Place Order
Primary       Actor	Customer
Description	  Create a food order
Precondition	Menu items selected
Postcondition	Order created
Customers select food items and confirm their purchase. The system generates a new order record.

UC05 Make Payment
Item	        Description
Use Case	    Make Payment
Primary       Actor	Customer
Description	  Complete payment
Precondition	Order exists
Postcondition	Payment completed
Customers choose a payment method and complete the transaction. The payment result is stored by the system.

UC06 Track Order
Item	        Description
Use Case	    Track Order
Primary       Actor	Customer
Description	  Check delivery status
Precondition	Order exists
Postcondition	Current status displayed
Customers can monitor the progress of their orders until delivery is completed.

UC07 Manage Menu
Item	         Description
Use Case	      Manage Menu
Primary         Actor Restaurant Manager
Description	    Maintain menu information
Precondition	  Manager logged in
Postcondition	  Menu updated
Restaurant managers can add new menu items, modify prices, and remove unavailable items.

UC08 Manage Orders
Item	        Description
Use Case	    Manage Orders
Primary       Actor Restaurant Manager
Description	  Process customer orders
Precondition	Orders exist
Postcondition	Order status updated
Managers can review customer orders and update their current processing status

## 5. Analysis Class Diagram
Analysis Class Diagram Overview

Figure 1 shows the analysis class diagram of the Food Ordering System.
The analysis model consists of six major classes: Customer, RestaurantManager, Restaurant, Menu, Order, and Payment.
These classes were identified based on the functional requirements and use case analysis. The Customer class represents users who order food, while the RestaurantManager class represents users who manage restaurant operations. Restaurant and Menu classes store restaurant-related information. The Order class manages customer orders and the Payment class handles payment transactions.
The relationships between these classes represent the main business processes of the system and provide the foundation for the design phase.

Customer
The Customer class represents users who order food through the application. Customers interact with the system by browsing menus, placing orders, and tracking deliveries.

Responsibilities
·  Register account
·  Login
·  Browse menus
·  Place orders
·  Track orders

Restaurant Manager
The Restaurant Manager class represents administrators responsible for restaurant operations.

Responsibilities
·  Manage menu items
·  Manage customer orders
·  Update order status

Restaurant
The Restaurant class stores restaurant information used by customers during menu browsing.

Responsibilities
·  Store restaurant information
·  Provide menu data

Menu
The Menu class contains food item information.

Responsibilities
·  Store menu details
·  Maintain food prices

Order
The Order class manages customer order information.

Responsibilities
·  Store order records
·  Manage order status

Payment
The Payment class handles payment processing.

Responsibilities
·  Process payment transactions
·  Verify payment results

## 6. References
[1] Software Engineering Lecture Notes.
[2] Ian Sommerville, Software Engineering.
[3] UML Distilled, Martin Fowler.
[4] Java Documentation.
[5] MySQL Documentation.
[6] GitHub Documentation.
[7] Visual Paradigm User Guide.
[8] Baemin Application.
[9] Yogiyo Application.
