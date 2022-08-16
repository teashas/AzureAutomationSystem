# Project - D3 Design

_Group : Azure\
Date and location: Aug 11, 2022, Yavapai County ITS\
Group Members: Saima Teasha_

## 1. Introduction

The Automation Alert System is a automation system where Azure RBAC users can get emails directly to their mailbox once an alert is triggererd on Azure. The Automation System also forwards all alert sent to Microsoft Sentinel to the Azure dashboard. 

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
