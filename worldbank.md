# World Bank

[SalesForce](https://chef.lightning.force.com/lightning/r/Account/0018000001H7mq8AAB/view)

## Players

### World Bank Peeps

| name                                | title               | location         | email                             | LinkedIn                                                             | Notes |
| ----------------------------------- | ------------------- | ---------------- | --------------------------------- | -------------------------------------------------------------------- | ----- |
| Kote Motipalli                      | System Engineer     | Chantilly, VA    | kmotipalli@worldbankgroup.org     | [LI](https://www.linkedin.com/in/koteswara-rao-motipalli-85926621a/) |       |
| Mohamed Jain                        |                     |                  | mhassanibrahim@worldbankgroup.org | N/A                                                                  |       |
| George Metry                        | Program Manager     |                  |                                   | [LI](https://www.linkedin.com/in/george-metry/)                      |       |
| Frederico De Oliveira Shinohara     | IT Officer          | Washington, DC   | fshinohara@worldbankgroup.org>    | [LI](https://www.linkedin.com/in/fredericoshinohara/)                |       |
| Mahendran Ragupathi                 |                     |                  | mragupathi@worldbankgroup.org     |                                                                      |       |
| Kumaresh Babu                       | Information Officer | India            | kbabu@worldbankgroup.org          |                                                                      |       |
| Srividhya Janardhanan               |                     |                  | sjanardhanan@worldbankgroup.org   | [LI](https://www.linkedin.com/in/kumaresh-babu-0492ba32/)            |       |
| Violeta Patrutoiu                   |                     | Sophia, Bulgaria | vpatrutoiu@worldbankgroup.org     | [LI]                                                                 |       |
| Strahil Nikolov                     |                     | Sophia, Bulgaria | snikolov@worldbankgroup.org       | [LI]                                                                 |       |
| Ping Yuan Lu                        |                     |                  |                                   |                                                                      |       |
| Mohamed Jainulabideen Hassanibrahim |                     |                  |                                   |                                                                      |       |


### Chef Folks

| name             | title | Notes |
| ---------------- | ----- | ----- |
| Tom DeYulia      | (AM)  |       |
| Mike Butler      | (SA)  |       |
| Harish Govardhan | (CSM) |       |

## Background

- Automate is early 2022
- Chef Infra is old
- They are using Berks & Roles/Environment
- They have 15-20 cookbooks
- They have 4500 or so servers (3200 prod) (1500 np)
- Licensed for 5,500
- They have Automate 1 running Workflow and need to migrate to AZDO
- vRealize 7.6 Plug-In
- Checking in every 4 hours Windows | 15 minutes on Linux

## CS Meeting 5/20/22

- Looking for a CA to discuss advantages of Policyfiles over Roles / Environments
- Chef Client upgrade to 17. 50% done.
- vRealize migration to 8.6 ( in the next few months )
- Need to build a pipeline in AzDO

### Need a couple of plans for updates / migrations

- Need to upgrade from Workflow to Azure DevOps
- Move from Roles / Env. to Policy Files
- Upgrade or move Chef Infra

## Demo'd Policyfiles

- We gave a presentation of Policyfiles and then showed them in action

## CS Meeting 6/17/22

- Promoted ChefConf
- Trying to expand but looking for ways into Cloud Configuration.
  - They already use Inspec to scan their cloud resources.
  - They want to be able to correct user and other configuration anomalies with Chef on the HOST side of their cloud configurations
- Starting to look at upgrade from Chef Server 12.03 to 14.16.19
  - They are going to start upgrading in July - first with Non Prod
  - Suggestion to email us when they have a date just so that we are in the know.
- Unhappy with the quality of Support.
  - They want someone on the phone and not email / ticket exchanges.
  - Suggested to them to be sure to let Tom, Harish and I know if they are struggling.

## CS Meeting 9/23/22

- Need to update to version 3.x and then 4.x
- Still need help with Azure DevOps pipeline

## CS Meeting 11/18/22

- WB folks didn't show

## CS Meeting 4/21/23

Violeta and Fredrico are taking over Chef - running it from Bulgaria.

They will be coming to DC on Monday for a weeks worth of meetings.
I'm going to try to get out and see them. Things are going to be tight.

## In Person Meetings 4/26/23

Microsoft Engagement
Azure DevOps - Code Management / Pipeline
Bug in kitchen for Azure Deprecation

Secret
Pipeline chef export secret. (Corey)
chef_vault - vs azure_key_vault

Harish - bi-weekly meetings - maybe include Jeffery.

Bugs are sitting out to long
Fred and Palo

Project to OpenSCAP
Vendor Provided Remediation

Contributions to github are going unheard (hunter86bg)

**Interested in subscription training**

*Courier*

More complex examples available.
Document on Attribute in Policyfiles
Look at https://docs.chef.io/chef_compliance_phase/

Send links to snohio cookbooks
`default['audit']['waiver_file'] = 'C:\chef\waiver-win.yaml'`
