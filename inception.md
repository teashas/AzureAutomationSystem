# Project Inception

_Group : Azure\
Date and location: Aug 4, 2022, Yavapai County ITS\
Group Members: Abe Zapeda, Jacob Rascon, Jeff Holverson, Jerry Struver, Joshua Diaz, Saima Teasha_

## 1. Introduction

I would like to create an automation system using the resources available in the Azure Portal. I want to make an automation system that notifies the Azure Active Directory persons about certain threats or alerts that they might need to know. the automation system would send out emails to the Azure Active Directory about the threat/alert, and will post a notification to the dashboard as well.

## 2. Initial value proposition and consumer segments

**IVP:** Azure Automation System (AAS) is a basic, simple automation system that is implemented into our Azure workspace to notify us against potential threats. 

**Initial Consumer Segments:**

- Azure RBAC Roles

## 3. Interviews Summary

### Interview 1:

**Summary:** 

**Interviewer:** Jacob Rascon\
**Interviewee:** Saima Teasha\
**When:** 08/04/2022 \
**Consumer Segments:** Azure Admin

**Key insights**
  - 

 **Hypotheses that were validated**
  - 

 **Assessment: Must have / Nice to have / Don’t care**
  - 

### Interview 2:

**Summary:** 

**Interviewer:** Jeff Holverson\
**Interviewee:** Saima Teasha\
**When:**  08/04/2022\
**Consumer segment:** Azure Contributor

**Key insights:**
  - 


**Hypotheses that were validated:**
  - 

**Assessment: Must have / Nice to have / Don’t care**
  - 

### Interview 3:

**Summary:** The system needs to be able to get information on all VM resources to report alerts back to the user. 

**Interviewer:** Joshua Diaz\
**Interviewee:** Saima Teasha\
**When:**  08/04/2022\
**Consumer segment:** Global Admin & Contributor

**Key insights:**
  - Subscribed to Infrastructure & Production (DEMO)
  - Global admin in Infrastructure
  - Contributor in Production (DEMO)
  - Some of the tasks performed in Azure Portal include contribition with the Bicep files deployed to Azure and AVD configuration.
  - Use the Service Now Application to send out alerts to the directory instead of the Azure Active Directory

**Hypotheses that were validated:**
  - The system sends out alerts instantly (but where do you draw the line?)

**Assessment: Must have / Nice to have / Don’t care**
  - Must be able to detect unauthorized Remote Desktop Access (RDA) threats. 
  - It would be nice to see if multiple VMs are being created and how many people are accessing each VM.
  - Don't care about multiple failed log in attempts.

### Interview 4: 
**Summary:** User can recieve alerts when there are potential threats on a service or database. 

**Interviewer:** Jerry Struver\
**Interviewee:** Saima Teasha\
**When:**  08/04/2022\
**Consumer segment:** Azure owner (mgmt level)

**Key insights:**
  - Has access to the Infrastructure subscription.
  - Tasks include:
    - Deployment of Bicep files using PowrShell.
    - Creation of the CLI Workspace.
    - SQL & database implementation (soon)

**Hypotheses that were validated:**
  - System is able to detect threats including service applications. 

**Assessment: Must have / Nice to have / Don’t care**
  - System must alert when a service is down and server alerts.
  - Might be nice to include SQL performance alerts.

### Interview 5: 
**Summary:** System that send out alerts but also allows you to view current Azure user roles. 

**Interviewer:** Abe Zapeda\
**Interviewee:** Saima Teasha\
**When:**  08/04/2022\
**Consumer segment:** Azure owner & administrator

**Key insights:**
  - Has access to Infrastructure & IT-Application subscriptions.
  - Tasks involve giving access permissions to Azure users and researching in the environment.

**Hypotheses that were validated:**
  - System needs to send alerts to users.

**Assessment: Must have / Nice to have / Don’t care**
  - Must be bale to access the VM informations. 
  - Might be nice to view user roles acress Azure for auditing purposes.
  - Don't care to go into too much detail if it is an outside user.

## 4. Final value proposition and consumer segments

**Final Value Proposition:**
Azure Automation System (AAS) is a simple single-purpose resource that sends alerts of threats on the Azure Portal. 

**Consumer segments:**
- Global Administrator
- Contributor
- Reaader
- Virtual Machine Login
- Azure owner
