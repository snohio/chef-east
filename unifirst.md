# Unifirst - Customer

## The People

| Name           | Role | Location | email |
| -------------- | ---- | -------- | ----- |
| Wayne Agostino |

## How do they use Chef

1000 Nodes

50% windows / linux (Oracle Enterprise)
Not really using Manage but have it installed

Chef Infra Server (don't have versions)
Chef Automate (don't have versions)

## Introduction Call and Automate Question

- Covered what is and isn't deprecated (Chef Backend / Chef Manage are deprecated, Chef Infra Server is NOT)  
- Determined that while Chef Manage is installed, it is not really utilized except maybe to review databags.
- Stated that Automate can be used for a replacement of Chef Manage without installing Chef Infra Server components (didn't demo and honestly I would only suggest if really needing Chef Manage with some caveats. I'm still working with Product and Engineering to make it more secure and trackable.)
- Discussed the value of adding Chef Infra Server as a component of the Chef Automate (4) Habitat stack. Single system being utilized, easier updates to the system, easier management.
- Walked through (Demo) how to modify the patch.toml and include infra_server to the products and run chef-automate config patch patch.toml.
- talked about backups (back to easier management).
- Briefly discussed the value of including Inspec tests into the cookbooks \compliance\profile path and adding inclue_profile to the default.rb recipe. Let me know if you want to demo it, but you can also look at https://github.com/snohio/chef-client as an example.

I learned that Unifirst :

- Has about 1000 nodes bootstrapped
- Updating cookbooks is done manually through Knife
- Using for Oracle Linux and Windows (50/50)
- Not really using Automate for much
- Have been using Chef for about 6 years.
- Have suggested to the Unifirst compliance team of the value of Compliance Reporting but they haven't been interested.

