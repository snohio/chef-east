# Etsy - Customer Notes

Etsy is a log time customer of ours. One of the longest tenured customers.

## The Players

Jeremy Tinley
Mason Richins

## Current Install

* Using A2HA
* GCP Managed Postgres
* GCP Elastic Search
* 7300 - with 1000 (ephemeral nodes) not checking in.
* 15 minute interval

* Infra Greenfield

## SaaS Trial

This was completed. They really did not work on it. Internally they had discussions with the security team and until there can be a secure tunnel between GCP and AWS, they are going to build it in house.

## Automate HA on GCP

In light of the outcome with the SaaS trial and discussions, Etsy built a new instance of Automate HA on GCP using some GCP services but not all. They worked with our engineering team and were instrumental with helping us deliver HA on GCP. They validated documentation and even made a commit or two to the code base to help. This is for their greenfield instance of Chef and we'll want to follow up on how that is going.
