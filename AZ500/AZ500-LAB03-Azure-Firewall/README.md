# AZ-500 LAB03: Azure Firewall

## 🎯 Objective
This lab focuses on deploying and configuring Azure Firewall to centrally control and log network traffic across Azure virtual networks, in alignment with the Implement network security module of the AZ‑500 certification.

## 📚 Context
This lab is based on the official LAB_03_AzureFirewall from Microsoft Learning.
It demonstrates how Azure Firewall provides scalable, stateful traffic filtering, application rules, network rules to secure Azure environments.

## 🧪 Planned Steps
1. Deploy a virtual network with multiple subnets (including AzureFirewallSubnet)
2. Deploy an Azure Firewall instance
3. Create a route table and define UDRs to force traffic through the firewall
4. Configure firewall network rules and application rules
6. Connect to test virtual machines
7. Validate traffic filtering by testing allowed and denied connections

## 🧠 Personal Notes
Walkthrough steps, behaviors, and personal observations will be documented in the notes/ folder.

## 📸 Screenshots
Screenshots will be added to the screenshots/ folder to illustrate:
1. Firewall deployment
2. Route table and UDR setup
3. Rule configuration (application & network)
4. Connectivity test results from the test VM

## 🧩 Deployment Scripts

All deployment scripts used in this lab are stored in the scripts/ folder.
They automate the provisioning of the lab architecture, including the virtual network, subnets, test VM, etc.

## 📎 References
- ([Microsoft Learn: Azure Firewall documentation](https://learn.microsoft.com/en-us/azure/firewall/overview))
- AZ‑500 official learning path: Implement network security

