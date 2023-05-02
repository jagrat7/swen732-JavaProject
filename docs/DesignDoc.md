---
geometry: margin=1in
---
# ClassiqueHotelier: Hotel Management System 
## Project Design Documentation

## Team Information
* Team name: Hotel Management System

* Team members:
  * Avinash Amudala
  * Galekwan Sango
  * Sushanth Nayak
  * Jagrat Rao


## Executive Summary

The Hotel Management System project aims to streamline and automate the daily operations of a hotel, ensuring a seamless experience for both guests and hotel staff. This comprehensive software solution caters to the needs of various user groups, including hotel guests, receptionists, housekeeping staff, and hotel managers. By addressing essential functionalities such as room booking, check-in/check-out processes, guest profile management, and housekeeping task management, this system will enhance the overall efficiency of the hotel operations and improve customer satisfaction.

### Purpose
The primary purpose of the Hotel Management System is to simplify and automate hotel management processes for the primary user groups, including hotel guests and hotel staff (receptionists, housekeeping staff, and hotel managers). Key user goals include enabling guests to easily book rooms, manage their profiles, and check-in/check-out, while empowering hotel staff to efficiently manage room availability, guest information, and housekeeping tasks.

### Glossary and Acronyms
| Term   | Definition                                                                                                                                                                                                                                                                              |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SPA    | Single Page Application: A web application or website that dynamically updates a single HTML page as the user interacts with the app, improving user experience and reducing page load times.                                                                                       |
| HMS    | Hotel Management System: A software solution designed to manage and automate hotel operations, including room booking, guest management, and housekeeping tasks.                                                                                                                     |
| API    | Application Programming Interface: A set of rules, protocols, and tools for building software applications that enable communication between different software components.                                                                                                           |
| GUI    | Graphical User Interface: A visual representation of a software application that allows users to interact with the system using graphical elements such as buttons, icons, and windows.                                                                                             |
| CRUD   | Create, Read, Update, and Delete: A set of common operations performed on data in a database, often used as a shorthand for the basic functionalities of a data-driven application.                                                                                                  |
| DBMS   | Database Management System: A software system that allows users to define, create, maintain, and control access to a database, enabling efficient data storage and retrieval.                                                                                                        |





## Requirements

Online Room Booking with Real-Time Availability
*  1.1. The system shall allow guests to search for room availability based on date, room type, and number of guests.
1.2. The system shall display real-time room availability to guests.
1.3. The system shall enable guests to book a room and provide necessary information, such as name, contact information, and payment details.
1.4. The system shall send confirmation emails to guests upon successful booking.

Guest Check-In and Check-Out Automation
2.1. The system shall allow receptionists to check-in guests upon arrival by verifying their booking details and identification.
2.2. The system shall enable receptionists to check-out guests upon departure, calculate the final bill, and process payments.
2.3. The system shall update room availability status after guest check-in and check-out.

Guest Profile Management
3.1. The system shall store guest information, including personal details, contact information, and booking history.
3.2. The system shall allow receptionists to search, view, and update guest profiles.
3.3. The system shall allow guests to view and update their profiles through a secure online portal.

Housekeeping Task Management
4.1. The system shall automatically generate housekeeping tasks based on room status and guest needs.
4.2. The system shall allow housekeeping staff to view, update, and complete assigned tasks.
4.3. The system shall notify receptionists and housekeeping staff of urgent tasks or special requests.

Reporting and Analytics
5.1. The system shall provide an admin dashboard to display key performance indicators, such as occupancy rate, revenue, and average length of stay.
5.2. The system shall generate customizable reports on booking, revenue, and guest data for specified date ranges.
5.3. The system shall provide data visualization tools to help management analyze trends and make informed decisions.

System Security and Data Privacy
6.1. The system shall enforce secure user authentication and role-based access control.
6.2. The system shall encrypt sensitive data, such as payment information and guest personal details.
6.3. The system shall comply with relevant data privacy regulations and industry best practices for data storage and processing.

### Definition of MVP
The Minimum Viable Product (MVP) for the Hotel Management System is a functional and user-friendly platform that enables guests to book rooms online, while allowing hotel staff to manage guest check-ins, check-outs, guest profiles, and housekeeping tasks efficiently.

### MVP Features
Online Room Booking with Real-Time Availability
Guest Check-In and Check-Out Automation
Guest Profile Management
Housekeeping Task Management

### Enhancements
Reporting and Analytics: We have implemented an admin dashboard that displays key performance indicators, such as occupancy rate, revenue, and average length of stay, to help management make informed decisions. Additionally, the system can generate customizable reports and provide data visualization tools for better trend analysis.
System Security and Data Privacy: We have enforced secure user authentication and role-based access control to protect sensitive information. Sensitive data, such as payment information and guest personal details, are encrypted to comply with relevant data privacy regulations and industry best practices for data storage and processing.
Responsive User Interface: We have developed a responsive user interface that adapts to various screen sizes and devices, ensuring a seamless experience for guests and staff members across desktops, tablets, and mobile phones.
Integration with External Services: The system can be integrated with popular payment gateways, email service providers, and other third-party services to streamline the booking process and improve overall efficiency.


## Application Domain
![](../../Users/Avinash/Downloads/WhatsApp Image 2023-04-26 at 9.30.05 PM.jpeg)
The Hotel Management System operates within the domain of the hospitality industry, specifically focused on hotels and their management processes. The primary goal of the system is to provide a seamless experience for both hotel guests and staff members by streamlining daily operations, such as room booking, guest check-in and check-out, and housekeeping task management.

The domain model for the Hotel Management System consists of several key entities and their relationships, which are outlined below:

Guest: Represents a person who books a room in the hotel. The guest has attributes such as name, contact information, and payment details.

Room: Represents a hotel room available for booking. A room has attributes like room number, room type, capacity, and status (available, booked, or unavailable).

Booking: Represents a reservation made by a guest. A booking has attributes such as booking ID, guest details, room details, check-in and check-out dates, and payment status.

Receptionist: Represents a hotel staff member responsible for managing guest check-ins and check-outs. A receptionist has attributes like name, employee ID, and contact information.

Housekeeper: Represents a hotel staff member responsible for maintaining the cleanliness and orderliness of hotel rooms. A housekeeper has attributes like name, employee ID, and contact information.

Housekeeping Task: Represents a specific cleaning or maintenance task assigned to a housekeeper. A housekeeping task has attributes like task ID, room number, task description, and task status (completed or pending).

Report: Represents a collection of data and statistics related to hotel operations, such as occupancy rate, revenue, and average length of stay. A report has attributes like report ID, report type, and time range.

These entities interact with each other to form the core functionality of the Hotel Management System. For example, a guest books a room, which creates a booking record associated with the guest and the room. The receptionist checks in the guest upon arrival and checks them out upon departure. The housekeeper receives housekeeping tasks to maintain the cleanliness of rooms, and the management can access reports to analyze hotel performance and make data-driven decisions.


## Architecture and Design

This section describes the application architecture for the Hotel Management System.

### Summary

The Hotel Management System is designed using a three-tier architecture, which consists of the presentation, business logic, and data storage layers. This architecture allows for the separation of concerns, making the system more modular, maintainable, and scalable.

Presentation Layer
The presentation layer is responsible for providing a user interface (UI) through which hotel guests and staff can interact with the system. This layer is developed using modern web technologies such as HTML, CSS, and JavaScript, along with frameworks like Bootstrap and Vue.js for responsive design and interactivity. The UI is designed to be user-friendly and intuitive, catering to the needs of various user groups, including guests, receptionists, housekeepers, and hotel management.

Business Logic Layer
The business logic layer is responsible for implementing the core functionality of the Hotel Management System, such as room booking, guest management, housekeeping task management, and reporting. This layer is developed using Java and follows the principles of object-oriented programming (OOP) to ensure a clean and modular design. Key classes and their relationships are modeled based on the domain model described in the Application Domain section.

The business logic layer also includes a set of application programming interfaces (APIs) that expose its functionality to the presentation layer. This allows for a clear separation between the UI and the underlying business logic, making the system easier to maintain and extend in the future.

Data Storage Layer
The data storage layer is responsible for persisting the system's data, such as guest information, room bookings, and housekeeping tasks. This layer uses a relational database management system (RDBMS) such as MySQL or PostgreSQL to store the data in a structured and efficient manner. The database schema is designed to ensure data consistency, integrity, and ease of querying.

The business logic layer communicates with the data storage layer using a data access object (DAO) pattern, which abstracts the underlying database operations and allows for easy swapping of the data storage technology if needed in the future.

By utilizing a three-tier architecture, the Hotel Management System achieves a high degree of modularity, maintainability, and scalability, ensuring the system can easily adapt to the changing needs of the hotel industry.

## Overview of User Interface

This section describes the web interface flow of the Hotel Management System. From the user's perspective, the flow of the pages in the web application is designed to be intuitive and user-friendly, catering to the needs of various user groups, including guests, receptionists, housekeepers, and hotel management.


### Model:
The Model layer consists of classes that represent the business entities and the business logic of the application. For the hotel management system, the Model includes the following classes:

Holder: This class holds the data structures representing the different types of rooms (luxury double rooms, deluxe double rooms, luxury single rooms, and deluxe single rooms) and their availability.
Customer: This class represents a customer who books a room, and it contains customer details such as name, contact information, and food orders.
Food: This class represents a food item that a customer can order. It contains properties such as the food's name, price, and quantity.
The Model layer is also responsible for implementing the business rules and operations related to hotel room booking, food ordering, and room checkout. These operations can be implemented as methods within the corresponding classes or as separate classes or services.

### View:
The View layer is responsible for displaying the data from the Model and capturing user input. In the hotel management system, the View can be a graphical user interface (GUI) or a command-line interface (CLI). The View layer consists of components like:

Room Details: Displays the features and pricing of the different types of rooms.
Room Availability: Shows the availability status of each room type.
Booking Form: Allows users to book a room by entering their personal information and selecting a room type.
Food Ordering Form: Enables customers to order food items from the available menu.
Checkout Form: Handles the room checkout process, including calculating the final bill and deallocating the room.
### ViewModel:
The ViewModel layer acts as the intermediary between the View and the Model. It exposes the data and commands that the View needs to interact with the Model. The ViewModel contains properties and methods that represent the available actions and data required by the View. In the hotel management system, the ViewModel can include properties and methods like:

DisplayRoomDetailsCommand: Displays room details based on the selected room type.
DisplayRoomAvailabilityCommand: Shows room availability for each room type.
BookRoomCommand: Books a room by creating a new Customer object and updating the corresponding room's availability in the Holder class.
OrderFoodCommand: Allows customers to order food items by updating their food orders in the Customer class.
CheckoutCommand: Processes the room checkout, including calculating the final bill, deallocating the room, and updating the room's availability in the Holder class.
The ViewModel interacts with the HotelManagement class (or another coordinating class or service), which is responsible for orchestrating the actions and updates between the Model and the ViewModel.

By following the MVVM architecture, the hotel management system achieves a clear separation of concerns between the data and business logic (Model), the user interface (View), and the coordination and communication between the Model and the View (ViewModel). This separation makes the system more maintainable, scalable, and testable. It also helps to simplify the development process and improve the overall structure of the application.

In the context of the hotel management system, the ViewModel will contain properties and commands that represent the available actions (display room details, display room availability, book a room, order food, and check out). The ViewModel will interact with the HotelManagement class, which serves as the primary coordinator for the system, to perform the required actions.

Here's how the MVVM pattern would be applied to the hotel management system:

The user interacts with the View by selecting an action or entering data.
The View communicates the user's input to the ViewModel, which processes the input and updates the Model (Holder, Customer, and Food classes) accordingly.
The ViewModel listens for changes in the Model and updates the View to display the results of the user's actions.
The View displays the updated information to the user.
By using the MVVM pattern, you can separate the concerns of the data, user interface, and application logic, making the system more maintainable and testable. For client-side applications or frameworks that support the MVVM pattern, this architecture can simplify the development process and improve the overall structure of the application.
![](D:/Room_Booking_sequence-swen32.png)
### Deployment and Scalability
The Hotel Management System is designed to be deployed on a web server, allowing users to access the application through their web browsers. The system can be deployed on a cloud-based platform, such as AWS or Azure, which provides the flexibility to scale the system resources based on the demand and usage patterns.

The application architecture follows a multi-tier design, separating the concerns of user interface, application logic, and data management. This separation allows the system to scale horizontally by adding more instances of the web server and database server as needed. Additionally, the use of caching and load balancing techniques can further improve the system's performance and scalability.

To ensure the system's security, the Hotel Management System uses secure communication protocols, such as HTTPS, and implements role-based access control to restrict access to sensitive information and operations. The system also employs best practices for secure data storage and handling, including encryption and hashing of sensitive data.

In conclusion, the Hotel Management System is designed with scalability, performance, and security in mind, ensuring a smooth and reliable experience for its users while accommodating the growth and changing needs of the hotel business.
![](../../Users/Avinash/Downloads/WhatsApp Image 2023-04-26 at 9.29.49 PM.jpeg)
### Static Code Analysis/Design Improvements
Static code analysis is a crucial part of the software development process, as it helps identify potential issues and vulnerabilities in the codebase. It involves analyzing the source code without executing the program, thus allowing developers to detect issues early in the development cycle. This section will discuss the importance of static code analysis and how it can lead to design improvements in the Hotel Management System.
![](../../Users/Avinash/Downloads/WhatsApp Image 2023-04-26 at 9.30.00 PM.jpeg)
Importance of Static Code Analysis
Detect potential bugs and vulnerabilities: Static code analysis tools can identify problematic code patterns, security vulnerabilities, and other issues that could lead to runtime errors or security breaches. By addressing these issues early, developers can prevent bugs from reaching the production environment, thus reducing the risk of costly incidents and system downtime.

Improve code quality and maintainability: Static analysis helps enforce coding standards and best practices, ensuring that the codebase is consistent, clean, and easy to understand. This, in turn, leads to increased maintainability and a smoother development process.

Enhance code performance: Some static analysis tools can identify performance bottlenecks or suboptimal code structures, allowing developers to optimize their code for better performance and resource utilization.

Facilitate code reviews: Integrating static code analysis into the development process can make code reviews more effective by automatically flagging potential issues, allowing reviewers to focus on the overall design and architecture.
![](../../Users/Avinash/Downloads/WhatsApp Image 2023-04-26 at 9.29.42 PM.jpeg)
Design Improvements in the Hotel Management System
By incorporating static code analysis into the development process, the following design improvements can be made to the Hotel Management System:

Refactor code for better modularity and cohesion: Analyzing the codebase can help identify areas where classes or methods are too large or have too many responsibilities. By breaking down these components into smaller, more focused units, the system's overall design becomes more modular and easier to maintain.

Optimize data structures and algorithms: Static analysis can reveal opportunities to use more efficient data structures or algorithms, leading to improved performance and reduced resource usage.

Eliminate code duplication: Detecting and removing duplicated code helps to reduce the overall size of the codebase and minimize the risk of introducing inconsistencies or bugs during maintenance.

Improve exception handling: Proper exception handling is critical for a robust application. Static analysis can identify areas where exceptions are not handled correctly, allowing developers to implement more robust error handling and recovery mechanisms.

Enhance security: By detecting potential security vulnerabilities, such as SQL injection or cross-site scripting (XSS) attacks, developers can take the necessary steps to harden the application and protect sensitive data.

### Acceptance Testing
Acceptance testing is a crucial phase in the software development lifecycle, as it ensures that the developed system meets the specified requirements and satisfies the needs of the users. In the context of the Hotel Management System, acceptance testing involves verifying the functionality, usability, and reliability of the system from the perspective of the end-users, such as hotel staff and guests. This section will outline the process of acceptance testing for the Hotel Management System.

Overview of Acceptance Testing Process
Define acceptance criteria: The first step in the acceptance testing process is to establish a set of clear and measurable criteria that the system must meet to be considered acceptable. These criteria should be based on the system requirements and user stories defined during the requirements gathering phase.

Develop test cases and scenarios: Based on the acceptance criteria, create a comprehensive set of test cases and scenarios that cover all the major functionalities of the system. These test cases should be designed to mimic real-world usage scenarios and verify that the system behaves as expected under various conditions.

Prepare test data and environment: Set up a test environment that closely resembles the production environment in which the system will be deployed. This includes configuring hardware, software, and network components, as well as preparing realistic test data to be used during the testing process.

Execute test cases: Execute the defined test cases and scenarios, documenting the results and any issues encountered during the testing process. This may involve manual testing, automated testing, or a combination of both, depending on the complexity of the system and the resources available.

Evaluate test results and identify issues: Analyze the test results to determine whether the system meets the defined acceptance criteria. If any issues are found, report them to the development team for resolution.

Retest and verify fixes: Once issues have been addressed, retest the system to ensure that the fixes have been implemented correctly and that no new issues have been introduced.

Obtain stakeholder approval: Upon successful completion of the acceptance testing process, present the test results to the stakeholders for review and approval. If the system is deemed acceptable, it can be moved into the deployment phase.

Sample Acceptance Test Cases for Hotel Management System
Here are some example test cases that can be used as a starting point for acceptance testing of the Hotel Management System:

Verify that a user can create a new room with valid information (room number, room type, and room rate).
Verify that a user cannot create a room with duplicate room numbers or invalid information.
Verify that a user can view the list of all rooms and filter them by room type or availability.
Verify that a user can create a new guest profile with valid information (name, contact details, and identification).
Verify that a user can search for a guest by name or identification and view their profile.
Verify that a user can create a new booking with valid information (room, guest, check-in and check-out dates, and payment details).
Verify that a user cannot create a booking with conflicting dates or invalid information.
Verify that a user can check-in a guest with a valid booking and update the room's availability status.
Verify that a user can check-out a guest, calculate the total charges, and update the room's availability status.
Verify that a user can create, assign, and manage housekeeping tasks for rooms.
Verify that a user can generate reports on room occupancy, revenue, and housekeeping performance.

