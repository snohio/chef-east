# Travelclick / Amadeus Sales Notes

## Introduction

| Name             | Title                         | Location              | LinkedIn                                                       | Notes                              |
| ---------------- | ----------------------------- | --------------------- | -------------------------------------------------------------- | ---------------------------------- |
| Mark Cassinelli  | Director                      | Portsmouth, NH        | [LI](https://www.linkedin.com/in/mark-cassinelli/)             | Head of the department             |
| Seneca Hinds     | DevOps Eng                    | Fort Lauderdale, FL   | [LI](https://www.linkedin.com/in/senecahinds/)                 | Responsible for the Infrastructure |
| Jonathan Scotto  | DevOps Eng                    | Orlando, FL           | [LI](https://www.linkedin.com/in/jonathan-scotto-92173343/)    | Technical Champion                 |
| Awad Bin Abdulla | DevOps Eng                    | Pittsburgh, PA        | [LI](https://www.linkedin.com/in/awad-bin-abdullah-02aab5222/) |                                    |
| Dennis Whitney   | Principal Solutions Architect | Dallas-Fort Worth, TX | [LI](https://www.linkedin.com/in/dennisrwhitney/)              |                                    |
| Natish Kapur     | Manager Platform Automation   | West Palm, FL         | [LI](https://www.linkedin.com/in/nitishkapur/)                 | Manages the Chef platform team     |

Alexandre Paradis - Automate and Tooling - Joined in June 2022
Yoandri Gallardo - 
Luis Bonetti - Director of Automation 

Natish - Focused on Azure
Thad - Focused on Azure

## Customer Success Meeting - 12/16/2021

Led by Alice Colvin

- Need to Update
- Have two Chef environments, one is 12.x (client too) and 14 / Client 15
- New model is following Policyfiles
- Migrating nodes from old to new.
- Need to update clients to 17 and we discussed how difficult it is.

Jonathan is in Orlando and Seneca is in Pembroke Pines.

### Followups

- Find a Coffee Talk time for Jonathan

## Customer Success Meeting - 07/27/2002

### Attendees

| Company      | Attendee        | Attendee       | Attendee          | Attendee    |
| ------------ | --------------- | -------------- | ----------------- | ----------- |
| **Amadeus**  | Mark Cassinelli | Seneca Hinds   | Awad Bin Abdullah |             |
| **Progress** | Alice Colvin    | Sean McGillick | Terrie Butcher    | Mike Butler |

- Alice is transitioning to Sean McGillick as CSM.
- Terrie joined to talk the Supportlink transition.
- I'm asking about changes. They need to add Awad.
  - They are growing. Nothing active material changes.
- They are having issues with Clients getting errors connecting to their existing Chef server.
- They are almost to the point of standing up their new Automate server.
- Extending On Prem Chef infrastructure. Moving Chicago data center to Azure.
- Hoping to get them to ChefConf

## New Discovery Call

### Amadeus Hospitality

- NMI (new markets)
- Travelclick
- Use terraform
- Chef Management - travelclick

Build out Inspec
Automate Patching
Lot of patching processes in place

## Incident on 2/3/2023

### [Case Number 01269683](https://progress.lightning.force.com/lightning/r/Case/5004Q00002iKpmJQAS/view)

I was pinged by Seneca to join a call in progress for an issue that they were having with a very legacy server that has about 600 nodes assigned to it.

### Who's on from TravelClick

![Who's On](images/travelclick.png)

### Outcome

- It seems that the server was running low on space and an individual moved items out of the postgresql folders to a "temp" folder and that seemed to be when they started having issues.
- The thinking is that Chef / Postgresql was trying to repopulate that data and it was recovering the database and using all of that storage again.
- Their team stopped Chef and move those folders back then restarted the services.
- It seemed to be rebuilding with using less storage than before.
- I have asked that they keep me up to date on the rebuild.
