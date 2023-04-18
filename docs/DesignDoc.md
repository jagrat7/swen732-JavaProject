---
geometry: margin=1in
---
# PROJECT Design Documentation

> _The following template provides the headings for your Design
> Documentation.  As you edit each section make sure you remove these
> commentary 'blockquotes'; the lines that start with a > character
> and appear in the generated PDF in italics._

## Team Information
* Team name: HOTEL MANAGEMENT SYSTEM
* Team members
* AVINASH AMUDALA
* GALEKWAN SANGO
* JAGRAT RAO
* SUSHANTH NAYAK

## Executive Summary

The Hotel Management System project aims to streamline and automate the daily operations of a hotel, ensuring a seamless experience for both guests and hotel staff. This comprehensive software solution caters to the needs of various user groups, including hotel guests, receptionists, housekeeping staff, and hotel managers. By addressing essential functionalities such as room booking, check-in/check-out processes, guest profile management, and housekeeping task management, this system will enhance the overall efficiency of the hotel operations and improve customer satisfaction.

### Purpose
The primary purpose of the Hotel Management System is to simplify and automate hotel management processes for the primary user groups, including hotel guests and hotel staff (receptionists, housekeeping staff, and hotel managers). Key user goals include enabling guests to easily book rooms, manage their profiles, and check-in/check-out, while empowering hotel staff to efficiently manage room availability, guest information, and housekeeping tasks.

### Glossary and Acronyms
Term	Definition
SPA	Single Page Application: A web application or website that dynamically updates a single HTML page as the user interacts with the app, improving user experience and reducing page load times.
HMS	Hotel Management System: A software solution designed to manage and automate hotel operations, including room booking, guest management, and housekeeping tasks.
API	Application Programming Interface: A set of rules, protocols, and tools for building software applications that enable communication between different software components.
GUI	Graphical User Interface: A visual representation of a software application that allows users to interact with the system using graphical elements such as buttons, icons, and windows.
CRUD	Create, Read, Update, and Delete: A set of common operations performed on data in a database, often used as a shorthand for the basic functionalities of a data-driven application.
DBMS	Database Management System: A software system that allows users to define, create, maintain, and control access to a database, enabling efficient data storage and retrieval.





## Requirements

Online Room Booking with Real-Time Availability
1.1. The system shall allow guests to search for room availability based on date, room type, and number of guests.
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

The Hotel Management System operates within the domain of the hospitality industry, specifically focused on hotels and their management processes. The primary goal of the system is to provide a seamless experience for both hotel guests and staff members by streamlining daily operations, such as room booking, guest check-in and check-out, and housekeeping task management.

![Domain Model](D:\classdia.jpg)

> _**[Sprint 2 & 4]** Provide a high-level overview of the domain for this application. You
> can discuss the more important domain entities and their relationship
> to each other._


## Architecture and Design

This section describes the application architecture.

### Summary

The following Tiers/Layers model shows a high-level view of the webapp's architecture.

![The Tiers & Layers of the Architecture](architecture-tiers-and-layers.png)

The e-store web application, is built using the Model–View–ViewModel (MVVM) architecture pattern. 

The Model stores the application data objects including any functionality to provide persistance. 

The View is the client-side SPA built with Angular utilizing HTML, CSS and TypeScript. The ViewModel provides RESTful APIs to the client (View) as well as any logic required to manipulate the data objects from the Model.

Both the ViewModel and Model are built using Java and Spring Framework. Details of the components within these tiers are supplied below.


### Overview of User Interface

This section describes the web interface flow; this is how the user views and interacts
with the e-store application.

> _Provide a summary of the application's user interface.  Describe, from
> the user's perspective, the flow of the pages in the web application._


### View Tier
> _**[Sprint 4]** Provide a summary of the View Tier UI of your architecture.
> Describe the types of components in the tier and describe their
> responsibilities.  This should be a narrative description, i.e. it has
> a flow or "story line" that the reader can follow._

> _**[Sprint 4]** You must  provide at least **2 sequence diagrams** as is relevant to a particular aspects 
> of the design that you are describing.  For example, in e-store you might create a 
> sequence diagram of a customer searching for an item and adding to their cart. 
> As these can span multiple tiers, be sure to include an relevant HTTP requests from the client-side to the server-side 
> to help illustrate the end-to-end flow._

> _**[Sprint 4]** To adequately show your system, you will need to present the **class diagrams** where relevant in your design. Some additional tips:_
 >* _Class diagrams only apply to the **ViewModel** and **Model** Tier_
>* _A single class diagram of the overall system will not be effective. Consider breaking down into smaller sections._
 >* _Correct labeling of relationships with proper notation for the relationship type, multiplicities, and navigation information will be important._
 >* _Include other details such as attributes and method signatures that you think are needed to support the level of detail in your discussion._

### ViewModel Tier
> _**[Sprint 4]** Provide a summary of this tier of your architecture. This
> section will follow the same instructions that are given for the View
> Tier above._

> _At appropriate places as part of this narrative provide one or more
> static models (UML class diagrams) with some details such as critical attributes and methods._


### Model Tier
> _**[Sprint 2..4]** Provide a summary of this tier of your architecture. This
> section will follow the same instructions that are given for the View
> Tier above._

> _At appropriate places as part of this narrative provide one or more
> static models (UML class diagrams) with some details such as critical attributes and methods._

### Static Code Analysis/Design Improvements
> _**[Sprint 4]** Discuss the quality of your **current** design along with recommending **future** refactoring and other design improvements based on your analysis and review of the design against the object-oriented design principles covered in class._

> _**[Sprint 4]** With the results from the Static Code Analysis exercise, 
> **Identify 3-4** areas within your code that have been flagged by the Static Code 
> Analysis Tool (SonarQube) and provide your analysis and recommendations.  
> Include any relevant screenshot(s) with each area_

## Testing
> _This section will provide information about the testing performed
> and the results of the testing._

### Acceptance Testing
> _**[Sprint 2 & 4]** Report on the number of user stories that have passed all their
> acceptance criteria tests, the number that have some acceptance
> criteria tests failing, and the number of user stories that
> have not had any testing yet. Highlight the issues found during
> acceptance testing and if there are any concerns._

### Unit Testing and Code Coverage
> _**[Sprint 4]** Discuss your unit testing strategy. Report on the code coverage
> achieved from unit testing of the code base. Discuss the team's
> coverage targets, why you selected those values, and how well your
> code coverage met your targets._

>_**[Sprint 2 & 4]** **Include images of your code coverage report.** If there are any anomalies, discuss
> those._
