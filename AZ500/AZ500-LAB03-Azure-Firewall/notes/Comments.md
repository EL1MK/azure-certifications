# Exercise 1: Deploy and test an Azure Firewall

## Task 1: Use a template to deploy the lab environment.
 To that extent, the official template provided ([here](https://github.com/MicrosoftLearning/AZ500-AzureSecurityTechnologies/blob/master/Allfiles/Labs/08/template.json)) will be used.
 The template sets up the architecture described below which associated to the resource group "AZ500LAB03":

<figure>
  <img src="../screenshots/lab03_01_01_archi.png" alt="description" width="50%">
</figure>

The following resources have been deployed using the scripts, others will be deployed later in the lab:

<figure>
  <img src="../screenshots/lab03_01_02_deploy_archi.png" alt="description" width="50%">
</figure>

## Task 2: Deploy the Azure firewall

The Azure firewall has been created and deployed as follows:

<figure>
  <img src="../screenshots/lab03_02_01_deploy_fw.png" alt="description" width="50%">
</figure>

<figure>
  <img src="../screenshots/lab03_02_02_fw_ok.png" alt="description" width="50%">
</figure>

## Task 3: Create a default route

The goal is to create a default route for the Workload-SN subnet. This route will configure outbound traffic through the firewall.

The first step is to create and deploy the route table:

<figure>
  <img src="../screenshots/lab03_03_01_create_route_table.png" alt="description" width="50%">
</figure>

<figure>
  <img src="../screenshots/lab03_03_02_route_table_ok.png" alt="description" width="50%">
</figure>

Then the route table is associated to the Workload-SN subnet:

<figure>
  <img src="../screenshots/lab03_03_03_route_table_sub.png" alt="description" width="50%">
</figure>

Finally, a rule to force all outbound traffic from the subnet to go through the firewall is defined:

<figure>
  <img src="../screenshots/lab03_03_04_route_sub.png" alt="description" width="50%">
</figure>

<figure>
  <img src="../screenshots/lab03_03_05_route_sub_ok.png" alt="description" width="50%">
</figure>

## Task 4: Configure an application rule

The goal is to create an application rule in the firewall that allows outbound access to www.bing.com

The application rule is created, specifying the source IP range and protocols used to reach a specific domain name, then applied:

<figure>
  <img src="../screenshots/lab03_04_01_app_rule_create.png" alt="description" width="50%">
</figure>

<figure>
  <img src="../screenshots/lab03_04_02_app_rule_apply.png" alt="description" width="50%">
</figure>

## Task 5: Configure a network rule

The goal is to create a network rule in the firewall that allows outbound access to two IP addresses on port 53 (DNS).

The network rule is created, specifying the source IP range, protocol, destination IP addresses and port, then applied:

<figure>
  <img src="../screenshots/lab03_05_01_ntw_rule_create.png" alt="description" width="50%">
</figure>

<figure>
  <img src="../screenshots/lab03_05_02_ntw_rule_apply.png" alt="description" width="50%">
</figure>

## Task 6: Configure the virtual machine DNS servers

The goal is to configure the primary and secondary DNS addresses for the virtual machine. This is not a firewall requirement, but it will allow to test the application rule:

<figure>
  <img src="../screenshots/lab03_06_01_dns_config.png" alt="description" width="50%">
</figure>

## Task 7: Test the firewall

The goal is to test the firewall to confirm that it works as expected.

The first step is to connect to the jump server:

<figure>
  <img src="../screenshots/lab03_07_01_srv_jump_connect.png" alt="description" width="50%">
</figure>

Then connect to the working server using the command ```mstsc /v:Srv-Work in a shell```:

<figure>
  <img src="../screenshots/lab03_07_02_srv_work_connect.png" alt="description" width="50%">
</figure>

Internet Explorer Enhanced Security Configuration must be disabled to perform our tests:

<figure>
  <img src="../screenshots/lab03_07_03_srv_work_allow_edge.png" alt="description" width="50%">
</figure>

The firewall rules are tested through the browser and the desired behavior is observed as www.bing.com can be reached, whereas www.microsoft.com cannot:

<figure>
  <img src="../screenshots/lab03_07_04_bing_ok.png" alt="description" width="50%">
</figure>

<figure>
  <img src="../screenshots/lab03_07_05_microsoft_ko.png" alt="description" width="50%">
</figure>

 ## Clean-up resources
 Resources can be easily cleaned running the following command in Azure:
 ```Remove-AzResourceGroup -Name "AZ500LAB08" -Force -AsJob```

