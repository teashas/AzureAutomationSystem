# Project - D3 Design

_Group : Azure\
Date and location: Aug 4, 2022, Yavapai County ITS\
Group Members: Abe Zapeda, Jacob Rascon, Jeff Holverson, Jerry Struver, Joshua Diaz, Saima Teasha_

## 1. Introduction

The Automation Alert System is a automation system where gamers can easily create and share their Pokemon teams without accessing the game. The system has four main software components which are, creating teams, viewing teams, deleting teams, and sharing teams. Creating a team allows the app user to select six pokemon out of the inventory database, choose specific battle moves for each Pokemon, and then save that team under a team name. Viewing teams on the web application prompts the system to retrieve all the user’s team as an overview. Deleting an existing team would look similar to viewing teams, except it will display a delete button and will ask the user to confirm their choice if they select to delete the team. The team will be removed and will not show in the web application any longer. To share a team, the user must select a team to share and the system will display all the shareable social media platforms. After the user selects one of the platforms, the system will redirect them to the associated link.
The team is using the “create a team” use case because that is one of the first actions that the server can do. All the other use cases would have a similar class diagram, but the use cases and sequence diagram will differ from this use case.

## 2. Architechture 

## 3. Class Diagram

![Use Case](https://github.com/teashas/CS-386-Project/blob/main/images/projectClassDiagram.PNG)

## 4. Sequence Diagram

![Sequence Diagram](https://github.com/teashas/CS-386-Project/blob/main/images/projectSequenceDiagram.PNG)

<ins>***Use Case: Create team***</ins> 

Actor: User 

Description: User creates a team of Pokemon 

Preconditions: The user is logged into the system 

Post-conditions: A new team of Pokemon is created with the associated user 

Main Flow: 

<o1> 
  
- The user selects to create a new team 
  
- The system displays a list of all Pokemon
  
- The user selects multiple Pokemon 
  
- The system displays the selected Pokemon
  
- The user creates the new team
  
- The system registers the new team with the associated user
</ol>

## 5. Design Pattern


## 6. Design Principles

- Single Responsibility Principle: The Pokemon class only stores pokemon information.

- Open/Closed Principle: Our code follows the Open/Closed Principle because our code allows for users to create teams and view others teams without editing those teams.

- Liskov Substitution Principle: Our code follows the Liskov Substitution Principle because the IOS app is available in desktop and mobile app forms for IOS products.

- Interface Segregation principle: Our code follows the Interface Segregation Principle because we have one interface which is responsible for input from the client, and one interface responsible for the making of teams.

- Dependency Inversion Principle:  Our code follows the Dependency Inversion principle because the classes which make the pokemon teams and the class which the pokemon are stored do not directly rely on each other. 
