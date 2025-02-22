<p align="center">
<img src="https://github.com/user-attachments/assets/b112fb16-135e-4b66-81dc-6276761de85a" height="40%" width="60%" alt="Microsoft Azure Logo"/>
</p>




<h1>Azure: Creating Virtual Machines</h1>


<p>
This project is the first amongst a collection focused on implementing a Virtual Network in Azure.
Microsoft Azure is a cloud platform that will let you rent space to store or process your data.  
In this project, I will establish a connection between two virtual machines using Windows and Linux in Microsoft Azure's Cloud environment. 
This setup will enable me to perform a basic network traffic inspection using Wireshark in the next part of the collection.
</p>

<h2>Key Objectives</h2>
<h3>Virtual Machine Setup</h3>

-  Configure and deploy Windows VM
-  Configure and deploy Linux VM

<p>
  <h3>Remote Connectivity</h3>
  
  -  Establish Remote Desktop Connection (RDP) between the Virtual Machines (VMs)
</p>


<h3>Environments and Technologies Used</h3>

- Microsoft Azure (Virtual Machines, Networking)
- Windows App (Remote Desktop Protocol)

<p>
  <h3>Operating Systems Used</h3>
  </p>




| **Operating System**        | **Role**               |
|----------------------------|------------------------|
| <img alt= "windows logo" src="https://i.imgur.com/KcrV0u6.png" width="20"> Windows (Windows 10 Pro) | Windows Virtual Machine |
| <img alt= "Ubuntu logo" src="https://github.com/user-attachments/assets/87cccf20-cfc6-4950-b1ec-b480d913e7eb" width="20"> Linux (ubuntu 22.04) | Linux Virtual Machine              |
<p></p>

<p>
<h1>Setup and Configuration of Virtual Machines</h1></p>


<h3><u>Step 1: Create Resource Group</u></h3>

- Go to [Portal.azure.com](https://portal.azure.com)
- Create a Resource Group
- Name it `"RG-Network-Activities"` & Set the region to (Europe) UK South

<img alt="resource group name" src="https://i.imgur.com/dNXnPOP.png" width="776">
<img alt= "resource group name" src="https://i.imgur.com/Fw6lP7s.png" width="776">
</p>

<h3><img alt= "windows logo" src="https://i.imgur.com/KcrV0u6.png" width="20">  Step 2: Create Windows Virtual Machine</h3>

- Go to [Portal.azure.com](https://portal.azure.com)
- Create a Virtual Machine
- Name it "windows-vm" & Set the region to (Europe) UK South
- Select a vm size with at least 2 vcpus
- Set a username and password
- Be sure to memorise your credentials or store in a secure place

![Creating Windows Virtual Machine](https://github.com/user-attachments/assets/192a051e-fc10-4648-aa3b-51ccd9c2bbb2)
<br><br> 
![Credentials](https://github.com/user-attachments/assets/9d35ac70-acf2-4331-9176-64c4a64ed08d)
<br><br> 
![Networking Step 1](https://github.com/user-attachments/assets/db017071-b60a-4d7e-af54-29de04be897e)
<br><br> 
<h3><img alt= "linux Ubuntulogo" src="https://github.com/user-attachments/assets/6e6e72e4-01cf-4891-a3e8-eea6b5971f10" width="20">  Step 3: Create Linux Virtual Machine</h3>


- Go to [Portal.azure.com](https://portal.azure.com)
- Create a Virtual Machine
- Name it "linux-vm" & Set the region to (Europe) UK South
- Select a vm size with at least 2 vcpus
- Set a username and password
- Be sure to memorise your credentials or store in a secure place
- Deploy the Linux vm to the same Virtual Network as the Windows vm
  
![Linux VM Create 001](https://github.com/user-attachments/assets/2ccd052e-fcbc-409e-abaf-af0869ee72c4)
<br><br> 
![Linux Credentials](https://github.com/user-attachments/assets/ec0c115f-b9c9-4714-87cb-c40f3dbf7bbd)
<br><br> 
![Networking Step 1](https://github.com/user-attachments/assets/db017071-b60a-4d7e-af54-29de04be897e)


<p>
<h1>Remote Desktop Connections</h1></p>

<h3><u>Step 4: Confirm Virtual Network/Subnet Configuration</u></h3>
Confirm that the virtual machines have been deployed to the same resource group and that they are on the same Virtual network/subnet.
This is to ensure that we can establish the remote desktop connection and perform a basic network traffic inspection in the next part.


![VM Deployed](https://github.com/user-attachments/assets/766e801c-d0b0-48ff-9932-bc2bf80414b4)
<br><br> 
<img width="586" alt="Networking" src="https://github.com/user-attachments/assets/913fdb24-bb5e-4d2f-ad4f-38c8d424502f" />
<br><br>
![image](https://github.com/user-attachments/assets/1efa6437-22d0-404e-a6c0-9e2ebff7f88a)



<h3><img alt= "RDP logo" src="https://github.com/user-attachments/assets/4aaa5d6e-ce8b-481f-a8da-57edc9a2917e" width="20"> Step 5: Establish Remote Desktop Connection</h3>

- Go to [Portal.azure.com](https://portal.azure.com)
- Search for "Virtual Machines" in the Azure search bar
- Select the "windows-vm" you created earlier and copy it's Public IP address

- Launch your Remote Desktop Connection Application
    - Mac Users download <a href="https://apps.apple.com/us/app/windows-app/id1295203466?mt=12" target="_blank" rel="noopener noreferrer">Windows App</a> Formerly known as "Microsoft Remote Desktop"
    - Windows Users open and use Remote Desktop
- Select "Add PC"
- Choose "Add Credentials" from the drop down and enter the credentials you created earlier, noting to accept the security prompt and proceed.
- You can now establish a remote connection to your virtual machine, by right-clicking the newly added device
  
<img width="1156" alt="Add PC" src="https://github.com/user-attachments/assets/151f6ec9-b615-4ed0-a5d1-6223206b2808" />

<img width="1158" alt="Connect PC" src="https://github.com/user-attachments/assets/5774f3e0-c118-44fe-89b9-57fb4ed16075" />




<h1>Project Summary</h1></p>

🎉Congratulations! You have created your first virtual machine within Azure!🎉

In this project, a virtual network was successfully deployed in Microsoft Azure, connecting a Windows (Windows 10 Pro) Virtual Machine and a Linux (ubuntu 22.04) Virtual Machine together using the Remote Desktop Connection (RDP). 








