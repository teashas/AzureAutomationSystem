# Project - D2 Requirements

_Group : Azure\
Date and location: Aug 4, 2022, Yavapai County ITS\
Group Members: Saima Teasha_

## 1. Position 

***1.1 Problem Statement***

The problem of establishing an activity log affects the RBAC roles; the impact of which is users have no alerts to recieve in the system.

***1.2 Product Position Statement***

For RBAC role users who struggle to keep up with daily changes in the environment. the Automation Alert System is a simple automation system that relieves user stress with automated alerts sent to their desktops. Unlike other automated system our product is primarily influenced by the Azure workspace and does not require any desktop setup.  

***1.3 Value Proposition & Customer Segment***

<ins>***Value Proposition***</ins>

 The Automation Alert System is a automated system where RBAC users can easily get notified of any sudden changes to the environment.

<ins>***Consumer Segment***</ins>

Our consumer segments are RBAC role users who may need to make changes to the Azure environment.

## 2. Stakeholders
<ins>***RBAC Role Users:***</ins>
The RBAC role users are a stakeholder because they will be the primary audience and will be using the automated system. The users are the key stakeholders for this project.

<ins>***Project Manager:***</ins>
In charge of assigning tasks on the team and making sure that each phase meets its deadline. The project manager is Saima.  

<ins>***Developers:***</ins>
These are the people putting in the time and effort into the project so that the team can produce the best possible product. The developers are the ones who test the demo and make adjustments to the system accordingly.

## 3. Functional Requirements 
 - Log all data in the VM.
 - Transfer log change data from VM to Log Analytics Workspace.
 - Transfer log change data from Log Analytics Workspace to Sentinel.
 - Send log alert email to RBAC roles.
 - Send log alert to Azure dashboard.

## 4. Non-Functional Requirements
- Compatibility - Compatible with any web browser
- Quality Code - Multiple other coders are satisfied with the readability of the code to make future changes
- Readability - 7 out of 10 people are comfortable with the readability of the site


## 5. MVP
The minimum viable product of our system would allow automatically log data and report unusual activities back to the user.

The features it would validate are:
- Detect activity in the workspace 
- Log activity
- Transfer unusual behaviors 
- Deploy alerts to each RBAC user
