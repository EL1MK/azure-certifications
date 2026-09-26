## Exercise 1: Create the virtual networking infrastructure

1. Create a virtual network: *myVirtualNetwork*
<figure>
  <img src="../screenshots/lab02_01_01_create_vnet.png" alt="description" width="50%">
</figure>

2. Create application security groups: *myAsgWebServers* & *myAsgMgmtServers*
<figure>
  <img src="../screenshots/lab02_01_02_create_asg.png" alt="description" width="50%">
  </figcaption>
</figure>

3. Create a network security group (NSG) *myNSG* and associate the NSG to the subnet
<figure>
  <img src="../screenshots/lab02_01_03_create_nsg.png" alt="description" width="50%">
  </figcaption>
</figure>

<figure>
  <img src="../screenshots/lab02_01_04_associate_nsg.png" alt="description" width="50%">
  </figcaption>
</figure>

4. Create inbound NSG security rules to allow HTTP/HTTPS traffic to web servers and RDP to the management servers

<figure>
  <img src="../screenshots/lab02_01_05_nsg_rules.png" alt="description" width="50%">
  </figcaption>
</figure>



## Exercise 2: Deploy virtual machines and test network filters
1. Create a virtual machine to use as a web server: *myVmWeb*
<figure>
  <img src="../screenshots/lab02_02_01_create_vmweb.png" alt="description" width="50%">
  </figcaption>
</figure>

2. Create a virtual machine to use as a management server: *myVmMgmt*
<figure>
  <img src="../screenshots/lab02_02_03_create_vmmgmt.png" alt="description" width="50%">
  </figcaption>
</figure>

3. Associate each virtual machine's network interface to its application security group
<figure>
  <img src="../screenshots/lab02_02_02_asg_vmweb.png" alt="description" width="50%">
  </figcaption>
</figure>

<figure>
  <img src="../screenshots/lab02_02_04_asg_vmmgmt.png" alt="description" width="50%">
  </figcaption>
</figure>

4. Test the network traffic filtering

Install Windows web server role on *myVmWeb*: ```Install-WindowsFeature -name Web-Server -IncludeManagementTools```

<figure>
  <img src="../screenshots/lab02_02_06_test_vmweb.png" alt="description" width="50%">
  </figcaption>
</figure>

<figure>
  <img src="../screenshots/lab02_02_07_test_vmweb2.png" alt="description" width="50%">
  </figcaption>
</figure>

*myVmWeb* is accessible from browser using HTTP but is not accessible using other protocols (e.g., RDP).

<figure>
  <img src="../screenshots/lab02_02_05_test_vmmgmt.png" alt="description" width="50%">
  </figcaption>
</figure>

<figure>
  <img src="../screenshots/lab02_02_05_test_vmmgmt.png" alt="description" width="50%">
  </figcaption>
</figure>

*myVmMgmt* is accessible from browser using RDP but is not accessible using other protocols (e.g., HTTP).

5. Clean-up resources

```Remove-AzResourceGroup -Name "AZ500LAB07" -Force -AsJob```

