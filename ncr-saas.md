# NCR SasS

## The Players

- Rodney Mountain | Wichita Falls, KC (Technical Expert)
- Daniel De Vore (Chef Champion)

## Scope

## Backstory

So it is quite messy. Former leadership there was in love with Chef until a couple of decisions had been made along the way.  First was the move from Roles and Environments to Policyfiles (I fell ya there.) Next we the decision to 

## 01/05/22 Meeting - Client 14 Upgrade Critical

- Learned that they were told that they couldn't move past Client 14.
- We need to learn some back story as to what happened at NCR and now that the key players are out, let's fix the relationship.
- Need to validate how many nodes they are actually supporting.
- There are different groups at NCR.
- Will work to clear up some misconceptions and other stuff in a technical deep dive in two weeks

## 01/18/2022 Meeting - Technical Deep Dive

### Chef Development 17.x

Looking like they are stuck with getting Kitchen with Azure because of a secrets management connectivity from Azure to core Secrets environment.

Cookstyle helped out a lot!

### Chef Infra / Automate Server

Chef Client - Run Time (15 / 1h / as needed)
Chef Version 12.17.15

Rodney to find who has root access for the Chef Server / Automate

Mike to make a query of Chef Nodes and the client version (simply)

### Pipeline Updates

The whole pipeline needs rebuilt anyway.

## Technical BS Session 05/05/2022

### Couple of notes

- I think we at least have a good idea of steps that need to happen to update cookbooks. 
They have a lot of work to do. Their existing pipeline is not terribly solid, they don't really know it well, and want to move it to Azure DevOps. They are currently using Git Actions. (which isn't a bad thing, Rodney knows Azure DevOps a bit better. *
- I talked with them about lift and shift. They don't really want to go there and discussed a few ways to use the existing platform, mostly just creating new repos, new policy groups and then updating the pipeline to chef push to those new groups
- We dove in to their use of Databags a bit - they are using them to hold attributes. They are not encrypted and don't contain secrets, only attribute data. They seem to be pretty comfortable on that process. I understand that we're pushing away from databags, but really don't know what the alternative for them would be. They entertained the idea of putting the attributes in the policyfiles but it was a conscious decision at the time to not to. *
- Toward the end of the call, I asked about versions because they really were pushing to not touch their existing Infra server and "not wanting to use Automate". When we looked, they are at 12.16.14 and Rodney kinda had the "Ah hah" moment of "Yeah, we really do need to update Chef Server" from a vulnerability standpoint. That is something that they are going to noodle. A bit of my worry is that - they have been running without changes for a long time, they have PCI findings for Chef 14 on servers and need to start updating cookbooks and client versions and pipelines. The Chef Server is going to see changes that they haven't had for a long time. These changes could impact the stability of the Infra server that they haven't seen. Standing up new systems with Automate on them with the Chef-Automate installer makes sense to me, but that leads back to a lift and shift idea. *
- They are using their own internal Supermarket as their source for all of their cookbooks in the policyfiles. Curious the future there. I was not really sure how it actually gets pushed to Supermarket (in general) but discussed that could be anywhere, including Github itself.
- Relationship wise, I think it was a good technical discussion and feel they are happy with the attention, but they really have a bit of work ahead of them. They have suffered from reductions in staff and are more in an SRE model and don't have folks to do the busy work. ProServ / Managed Services is not in the scope - that is something that NCR just doesn't do.

### Some take away's for us

- Those lines above that are * - I would really appreciate someone like Collin to give an hour of his time to answer the questions that are just beyond me.  
- It probably would be a good idea to pay them a visit and get a day of their time with road map info, modernization discussions, and whiteboard their plan going forward. I know we are a bit away from their next renewal but some attention now when they are in the thick of making a decision on the next few years will help to keep them a solid customer.

Me:

> More of a business question, do you have Azure spend that goes unused?
> We have a deal with Azure Marketplace and can place private offerings there.

DEVO:

>Anything that falls into scope of Chef 17 upgrade and costs more $ will be a hard fight to get approval.  For this year, we need to keep things under our current license we are paid up for.  However, I will comment that it’s easier for one to put something into Azure spend vs a PO.

ME:

> Yeah, I get that. Just keep that in mind.. Something to consider when working on that side with Tom DeYulia.
