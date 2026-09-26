# Exercise 1: Deploy and test an Azure Firewall

## Task 1: Use a template to deploy the lab environment.
 To that extent, the official templayte provided ([here](https://github.com/MicrosoftLearning/AZ500-AzureSecurityTechnologies/blob/master/Allfiles/Labs/08/template.json)) will be used.
 The template set up the architecture described below which associated to the ressource group "AZ500LAB03":

 // image

 ## Task 2: Deploy the Azure firewall

 //images

 ## Task 3: Create a default route
 The goal is to create a default route for the Workload-SN subnet. This route will configure outbound traffic through the firewall.

 //images

 ## Task 4: Configure an application rule
 The goal is to create an application rule that allows outbond access to www.bing.com

 //images

 ## Task 5: Configure a network rule
 The goal is to create a network rule that allows outbound access to two IP addresses on port 53 (DNS).

 //images

 ## Task 6: Configure the virtual machine DNS servers
 The goal is to configure the primary and secondary DNS addresses for the virtual machine. This is not a firewall requirement.

 ## Task 7: Test the firewall
 The goal is to test the firewall to confirm that it works as expected.

 ## Clean-up resources
 Resources can be easily cleaned running the following command in Azure:
 ```Remove-AzResourceGroup -Name "AZ500LAB08" -Force -AsJob```
