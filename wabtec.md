# Customer - Wabtec

## Background

Customer since 2018 when they were divested from GE
Renewal is 3/31/2024
ARR $120,500
1800 Nodes
Effortless
Gitlab-CI

## The People

| Name                      | Title                      | Location                      | Email Address                  | Reports to? | LinkedIn                                                              |
| :------------------------ | :------------------------- | :---------------------------- | :----------------------------- | :---------- | --------------------------------------------------------------------- |
| Tony Pasquarette          | Enterprise Cloud Architect | Enterprise Cloud Architecture | anthony.pasquarette@wabtec.com |             |                                                                       |
| John Paice                | Azure Architect            | Enterprise Cloud Architecture | john.paice@wabtec.com          |             |                                                                       |
| Eric McKee                | Enterprise Cloud Architect | Enterprise Cloud Architecture | eric.mckee@wabtec.com          | John        | [LI](https://www.linkedin.com/in/unixarchitect/)                      |
| Michael Worsham           | Operations Team            |                               | michael.worsham@wabtec.com     |             |                                                                       |
| Nagendra Kumar Avanigadda | Sr. Devops Engineer        | Bengaluru, Karnataka          |                                | John        | [LI](https://www.linkedin.com/in/nagendra-kumar-avanigadda-6971384a/) |

Dave Birchill

https://www.linkedin.com/in/ingetomlin/

### Internal Links to Notes and Such

[SharePoint 2021 Massardo Notes](https://progresssoftware-my.sharepoint.com/:w:/g/personal/massardo_progress_com/EdF5qMYQLWxItqkshpUtPy4BltI85DNHl0a3Yc-OY1yF7w?e=xlulfh)

> The group we work with was originally the GE Transportation group. They were divested from GE in 2018 and Westinghouse Air Brake Technologies (Wabtec) purchased them. During their last renewals, we’ve included PS that the team used to build out their effortless process. We’ve also spent a lot of CS time with them to build out effective pipelines and processes to ship changes for their base tools package.
>
> They are finishing the last tasks from the migration out of the GE subscriptions and data centers. Once that is complete, they are prioritizing several Chef projects.

**Environment:**

* ~1800 nodes
* Effortless Pattern
* Gitlab-ci
* They have their own Automate HA pattern.
* Automatic Automate updates. Reboot every three months
* Linux (Amazon 2, Centos 7, RHEL 7 and 8) and Windows
* They are using Chef in the Effortless pattern. This is covered under the "Limited Habitat Usage" license as of now. See image below.

[hab sup status](images/wabtec-hab-usage.jpg)

## Monthly Customer Success Meeting - 12/16/2021

Eric McKee, Collin MCNeese (CA), Rahul Rai (CSM), Tom Sanchez (AM)

* PostgreSQL - Using Amazon and they are upgrading their instance.
* Lot of discussions on new releases and underlying infra.
* Dave Birchel - Replaced John

## CS Sync Call | 2/10/22

* Eric was not on the call.
* There were discussions on 16 to 17 migrations.
* On Latest infra server. It's the bundled instance.

## CS Sync Call | 07/28/2022

* Currently using AWS Open Search - Elastic Search v. 6.8 with Automate 2.
* Need help migrating to AWS Open Search - native 1.2
* I gave them the push to our documentation which can help them, they may need a CA to handhold.

## CS Sync Call | 01/27/2023

OK! So, Eric and Nagendra are looking for 1000-1500 licenses for Habitat only for a new roll out in Azure.

## CS Sync Call 2/9/2023

Antivirus, Monitoring tools and more are being delivered and managed with Habitat.

This is a discussion I had with Tom on Slack about pricing for them.

> So real quick on my thoughts on the numbers and then I'll let you alone with Wabtec..
> Currently they are paying 36% of list for Compliance Automation. List = $189, their price $70 / per node. ($105k total).
> Inflation and all, a renewal and proper licensing at 40% of list for Enterprise Automation List = $250, their price would be $100 / per node. ($150k total)
> Habitat alone, 45% of List for Chef App Delivery (stand alone) = $200 List, their price would be = $90.
> We could suggest that they just do 3000 node license of Enterprise Automation and bring it in between $275k and $300k.
> They HAVE done a multi-year in the past and maybe you could do a ramp up as a part of their renewal $200k this year and $315k next. That would handle inflation for next year and give negotiation space.
> I'd really like to get them using Inspec even if they are only doing App Delivery with Habitat.
> All just food for thought.. IF you have any questions or comments, let me know, otherwise it's between you and Wabtec and Spencer. :slightly_smiling_face:
> Oh, and they might come back and say their non-compliance is our fault, which probably isn't entirely inaccurate. Previous AE's should have known that. But that also happens when they get a new person every year and the SKU's and products change every year.
> And maybe validate that I am correct about "Limited Use", but I'm 98% sure, know that when I was the customer.

## CS Sync Call 4/6/2023

## CS Sync Call 5/4/2023

* Attendees
  * Eric McKee
  * Nagendra
  * Rahul Rai
  * Tom DeYulia
  * Mike Butler

* TO CHECK:
  * Automate 4.5.37 uses 13.5 PostGresQL
  * Amazon is going to force upgrade 13.9 - September 15th, 2023

* Run cookbook plus habitat package demo
* Client 18.2.7 RHEL 9 Compatible

## CS Sync Call 12/14/2023

* 18.3.0
* AMS EMR 1500 - 3000 / mo
* 2700 Active clients
* Using Tanium (with cookbook?)
* 10k records of new builds / month
* Need ARM! AWS Gravaton 4
* Lambda
