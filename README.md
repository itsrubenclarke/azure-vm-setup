<p align="center">
<img src="https://github.com/user-attachments/assets/f492f831-b275-4c14-a73f-68318e82c00c" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Project: Deploying an Active Directory Lab in Azure</h1>

<p> 
This project Is the first amongst a collection focused on implementing Azure and Active Directory.
The goal here is to create a basic lab that mirrors a real working environment, providing me with hands-on-learning and practical experience with Active Directory services in a Cloud-based environment.
</p>


<h2>Overview </h2>

<p>In this project, I will set up and establish a connection between two virtual machines, each assigned a specific role. One virtual machine will function as the Domain Controller, while the other will be configured as the Client. This will allow me to perform a basic network traffic inspection.</p>

<h2>Key Objectives</h2>
<h3>Virtual Machine Setup</h3>

-  Configure and deploy the Domain Controller 
-  Configure and deploy a Client 

<p>
  <h3>Remote Connectivity</h3>
  
  -  Establish Remote Desktop Connection (RDP) between the Virtual Machines (VMs)
</p>

<p>
  <h3>Network Traffic Analysis</h3>
  
  -  Perform a basic network traffic inspection between the Domain Controller and Client Virtual Machines
</p>

<h3>Environments and Technologies Used</h3>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<p>
  <h3>Operating Systems Used</h3>
  </p>
  

| **Operating System**        | **Role**               |
|----------------------------|------------------------|
| <img alt= "windows logo" src="https://i.imgur.com/KcrV0u6.png" width="20"> Windows Server 2022 | Domain Controller (DC) |
| <img alt= "Windows logo" src="https://i.imgur.com/KcrV0u6.png" width="20"> Windows 10 (21H2) | Client VM              |
<p></p>

<p>
<h1>Setup and Configuration Guide</h1></p>


<h3><u>Create Resource Group</u></h3>

- Go to [Portal.azure.com](https://portal.azure.com)
- Create a Resource Group
- Name it "RG-Network-Activities" & Set the region to (Europe) UK South

<img alt="resource group name" src="https://i.imgur.com/dNXnPOP.png" width="776">
<img alt= "resource group name" src="https://i.imgur.com/Fw6lP7s.png" width="776">
</p>

<h3><img alt= "windows logo" src="https://i.imgur.com/KcrV0u6.png" width="20">  Create Windows Virtual Machine</h3>

- Go to [Portal.azure.com](https://portal.azure.com)
- Create a Virtual Machine
- Name it "windows-vm" & Set the region to (Europe) UK South

<img src="https://i.imgur.com/zr3HREy.png" width="776">


- Select a vm size with at least 2 vcpus
- Set a username and password
- Be sure to memorise your credentials or store in a secure place

<img src="https://i.imgur.com/iLEVzal.pngg" width="776">

<h3><img alt= "linux Ubuntulogo" src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/9e/UbuntuCoF.svg/1024px-UbuntuCoF.svg.png" width="20">  Create Linux Virtual Machine</h3>

- Go to [Portal.azure.com](https://portal.azure.com)
- Create a Virtual Machine
Name it "linux-vm" & Set the region to (Europe) UK South
![Linux VM Create 001](https://github.com/user-attachments/assets/2ccd052e-fcbc-409e-abaf-af0869ee72c4)
