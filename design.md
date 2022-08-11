# Project - D3 Design

_Group : Azure\
Date and location: Aug 11, 2022, Yavapai County ITS\
Group Members: Saima Teasha_

## 1. Introduction

The Automation Alert System is a automation system where gamers can easily create and share their Pokemon teams without accessing the game. The system has four main software components which are, creating teams, viewing teams, deleting teams, and sharing teams. Creating a team allows the app user to select six pokemon out of the inventory database, choose specific battle moves for each Pokemon, and then save that team under a team name. Viewing teams on the web application prompts the system to retrieve all the user’s team as an overview. Deleting an existing team would look similar to viewing teams, except it will display a delete button and will ask the user to confirm their choice if they select to delete the team. The team will be removed and will not show in the web application any longer. To share a team, the user must select a team to share and the system will display all the shareable social media platforms. After the user selects one of the platforms, the system will redirect them to the associated link.
The team is using the “create a team” use case because that is one of the first actions that the server can do. All the other use cases would have a similar class diagram, but the use cases and sequence diagram will differ from this use case.

## 2. Architechture 

![Architecture](https://github.com/teashas/AzureAutomationSystem/blob/main/images/systemArchitecture.png)

## 3. Class Diagram

![Class Diagram](https://github.com/teashas/AzureAutomationSystem/blob/main/images/classDiagram.PNG)

## 4. Sequence Diagram

![Sequence Diagram](https://github.com/teashas/AzureAutomationSystem/blob/main/images/sequenceDiagram.PNG)

<ins>***Use Case: Start Virtual Machine***</ins> 

Actor: User 

Description: User tries to turn on virtual machine.

Preconditions: The user is logged into the system and can access resources.

Post-conditions: An alert is posted on VM dashboard and emailed to admins.

Main Flow: 

<o1> 
  
- User signs into Azure using MFA.
  
- The system displays a list of all resources.
  
- The user selects to turn on VM.
  
- The system logs activity and send it to Log Analytics.
  
- The system forwards log to Sentinel.
  
- Sentinel creates Alerts.
  
- Sends alert to dashboard. 
  
- Send out alert email to Azure admin.
  
</ol>

## 5. Design Pattern

The system follows a behavioral design pattern because the system identifies common communication patterns between the object classes and validates these paterns. This pattern increases flexibility in communication. More specifically, it uses an observer design pattern. The observer pattern is a software design pattern in which an object, named the subject, maintains a list of its dependents, called observers, and notifies them automatically of any state changes, usually by calling one of their methods.

## 6. Design Principles

- Single Responsibility Principle: The resource class only stores resource information.

- Open/Closed Principle: Our code follows the Open/Closed Principle because our code allows for users to start/stop VMs and view others VMs without modifying user access.

- Liskov Substitution Principle: Our code follows the Liskov Substitution Principle because the Azure is available on Windows and Linux computers.

- Interface Segregation principle: Our code follows the Interface Segregation Principle because we have one interface which is responsible for input from the user, and one interface responsible for sending alerts.

- Dependency Inversion Principle:  Our code follows the Dependency Inversion principle because the classes which stores resources and the class which the logs activities do not directly rely on each other. 
