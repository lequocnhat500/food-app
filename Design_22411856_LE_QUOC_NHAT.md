# DESIGN

## 1. Introduction
1.1 Summary
최근 배달 음식 시장이 크게 성장하면서 많은 사람들이 모바일 애플리케이션을 이용하여 음식을 주문하고 있다. 하지만 음식점마다 주문 방식이 다르거나 메뉴 정보를 확인하기 어려운 경우가 있으며, 주문 이후 배송 상태를 확인하기 불편한 경우도 존재한다.
본 프로젝트는 이러한 불편함을 해결하기 위한 Food Ordering System을 설계하는 것을 목표로 한다. 사용자는 회원가입 및 로그인을 통해 서비스를 이용할 수 있으며, 음식점의 메뉴를 조회하고 원하는 음식을 주문할 수 있다. 또한 결제를 진행한 후 주문 상태를 실시간으로 확인할 수 있다.
음식점 관리자는 메뉴를 등록하거나 수정할 수 있으며, 고객의 주문을 관리할 수 있다. 이를 통해 고객과 음식점 모두가 효율적으로 서비스를 이용할 수 있도록 한다.
본 문서는 Analysis 단계에서 정의한 요구사항을 바탕으로 작성된 Design 문서이다. 시스템을 실제로 구현하기 위해 필요한 Class Diagram, Sequence Diagram, State Machine Diagram을 설계하고 각 구성 요소의 역할을 설명한다.

1.2 Important Points of Design
본 시스템을 설계하면서 다음 사항들을 중요하게 고려하였다.
사용자가 쉽고 직관적으로 주문할 수 있는 구조
메뉴 조회부터 결제까지 자연스럽게 연결되는 흐름
음식점 관리자가 메뉴와 주문을 효율적으로 관리할 수 있는 기능
주문 상태를 실시간으로 확인할 수 있는 구조
향후 기능 확장이 가능한 객체지향 설계
특히 사용자와 음식점 관리자의 역할을 명확하게 분리하여 시스템의 유지보수성과 확장성을 높이는 것을 목표로 하였다.

1.3 Use Case Overview
Figure 1 shows the use case diagram of the Food Ordering System.
The system consists of two main actors: Customer and Restaurant Manager. Customers can register accounts, log in, browse menus, place orders, make payments, and track order status. Restaurant Managers are responsible for managing menus and customer orders.
The use case diagram summarizes the major functions provided by the system and illustrates the interactions between users and the application. These use cases are used as the basis for designing the sequence diagrams presented in the following sections.
The main customer functions include Register, Login, Browse Menu, Place Order, Make Payment, and Track Order. Administrative functions include Manage Menu and Manage Orders.
By defining these use cases, the overall system requirements can be clearly identified before moving to the design phase.

## 2. Class Diagram
2.1 Class Diagram Overview
Figure 2 shows the overall class structure of the Food Ordering System. The system consists of six main classes: Customer, RestaurantManager, Restaurant, Menu, Order, and Payment.
The Customer class represents users who order food through the application. RestaurantManager is responsible for managing restaurant information, menus, and customer orders. Restaurant and Menu classes are used to store food-related information that customers can browse before placing orders.
The Order class manages customer order information and delivery status. The Payment class processes payment transactions associated with customer orders.
The relationships between classes are designed based on the main business flow of the system. Customers create orders, orders are connected to payments, restaurants provide menus, and restaurant managers manage restaurant operations. This structure improves maintainability and makes future expansion easier.

2.2 Customer Class
The Customer class represents users who use the application to order food. Customers can register an account, log in to the system, browse menus, place orders, and track delivery status. This class contains customer information such as name, email, and password.
2.3 RestaurantManager Class
The RestaurantManager class represents restaurant administrators. Managers can manage menus and customer orders through the system. This class helps restaurants update menu information and process incoming orders efficiently.
2.4 Restaurant Class
The Restaurant class stores restaurant information including restaurant name and address. Customers can browse restaurant information before selecting menu items.
2.5 Menu Class
The Menu class contains food item information such as menu name and price. Restaurant managers can add, modify, or remove menu items when necessary.
2.6 Order Class
The Order class manages order information created by customers. It stores order status and order date information. This class plays an important role in tracking the order lifecycle.
2.7 Payment Class
The Payment class is responsible for processing customer payments. It stores payment information and verifies transaction results before confirming orders.

## 3. Sequence Diagram
3.1 Register Sequence Diagram
Figure 3.1 shows the registration process of the Food Ordering System.
First, the customer enters registration information through the registration page. The system validates the input data and checks whether the account information is valid. If validation is successful, a new account is created and stored in the database. Finally, the system returns a success message to the customer and completes the registration process.
This sequence ensures that only valid user information is stored in the system database.

3.2 Login Sequence Diagram
Figure 3.2 shows the login process of the Food Ordering System.
The customer enters an ID and password on the login page. The login information is sent to the system for verification. The system checks the user information stored in the database. If the information is correct, the login request is approved and the customer is redirected to the main page. This process ensures that only authorized users can access the system functions.

3.3 Browse Menu Sequence Diagram
Figure 3.3 shows the menu browsing process.
When the customer selects the browse menu function, the system requests menu information from the restaurant. The restaurant returns the available menu data, including food names and prices. The system then displays the menu information to the customer.
This function allows customers to easily explore available food items before placing an order.

3.4 Place Order Sequence Diagram
Figure 3.4 shows the order creation process.
The customer first selects food items and adds them to the cart. After reviewing the selected items, the customer confirms the order. The order system creates a new order record and stores it in the database. Once the order is successfully saved, a confirmation message is displayed.
This sequence is responsible for generating customer orders and initiating the ordering process. 

3.5 Make Payment Sequence Diagram
Figure 3.5 shows the payment process.
The customer sends a payment request after placing an order. The payment system forwards the request to the bank server for verification. If the payment is approved, the payment system returns a success result to the customer.
This process ensures that all payment transactions are completed securely before the order is processed.

3.6 Track Order Sequence Diagram
Figure 3.6 shows the order tracking process.
The customer requests the current order status through the application. The system retrieves the latest order information from the order database. After receiving the information, the system displays the current status to the customer.
This feature allows customers to monitor the progress of their orders in real time.

3.7 Manage Menu Sequence Diagram
Figure 3.7 shows the menu management process.
The restaurant manager adds or updates menu information through the menu management interface. The menu manager sends the updated information to the database and stores the changes. After the operation is completed successfully, the manager receives a confirmation message.
This function helps restaurants maintain accurate menu information for customers.

3.8 Manage Orders Sequence Diagram
Figure 3.8 shows the order management process.
The restaurant manager first views the list of customer orders. The system retrieves order information from the database and displays it. The manager can then update the order status according to the current processing stage. The updated status is saved in the database and the operation is completed successfully.
This process enables restaurant managers to handle customer orders efficiently

## 4. State Machine Diagram
Figure 10 shows the state transitions of a customer using the Food Ordering System.
The process begins with the Register state, where a new customer creates an account. After registration, the customer enters the Login state to access the system. Once authenticated, the customer can browse available menus and select food items.
When the customer decides to purchase food, the process moves to the Place Order state. After the order is confirmed, the customer proceeds to the Payment state. Once payment is completed successfully, the customer can track the order status through the Track Order state.
Finally, when the order is delivered, the process reaches the Delivered state and the transaction is completed.
The state machine diagram provides a simple representation of the overall customer workflow within the Food Ordering System.

## 5. Implementation Requirements
5.1 Hardware Requirements
The following hardware environment is recommended for implementing the Food Ordering System.
Processor: Intel Core i5 or higher
Memory: 8GB RAM or higher
Storage: 256GB SSD or higher
Network: Stable Internet Connection
The hardware requirements are sufficient for development, testing, and deployment of the system.

5.2 Software Requirements
The following software tools will be used during development.
Item	                  Description
Operating System	      Windows 11
Programming Language	   Java
IDE                   	Eclipse IDE
Database	              MySQL
Version                 Control	GitHub
UML Tool	              Visual Paradigm
Web Server	            Apache Tomcat
These tools provide an efficient environment for implementing and maintaining the system.

5.3 Development Environment
The Food Ordering System will be implemented using Java and MySQL. Eclipse IDE will be used for coding and debugging. GitHub will be used for source code management and version control.
Visual Paradigm is used to design UML diagrams including Use Case Diagrams, Class Diagrams, Sequence Diagrams, and State Machine Diagrams.
The database will store customer information, restaurant information, menu data, orders, and payment records.

## 6. Glossary
Term	            Description
Customer	        A user who orders food through the application
Restaurant         Manager	A user who manages menus and customer orders
Restaurant	      A food service provider registered in the system
Menu	            A collection of food items available for ordering
Order	            A customer request for food items
Payment          	A transaction performed to complete an order
Delivery	        The process of transporting food to customers
Database	        A storage system used to manage application data
Authentication	  The process of verifying user identity
Session	           A temporary connection created after successful login
UML	               Unified Modeling Language used for software design
GitHub	            Platform used for source code management
Visual             Paradigm	UML modeling tool used in this project

## 7. References
[1] Software Engineering Lecture Notes, Kyungpook National University.
[2] Ian Sommerville, Software Engineering, 10th Edition.
[3] UML Distilled, Martin Fowler.
[4] Java Platform Standard Edition Documentation.
[5] MySQL Documentation.
[6] Apache Tomcat Documentation.
[7] GitHub Documentation.
[8] Visual Paradigm User Guide.
[9] Baemin Food Delivery Application.
[10] Yogiyo Food Delivery Application.
