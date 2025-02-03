<p align="center">
<img src="https://github.com/user-attachments/assets/b112fb16-135e-4b66-81dc-6276761de85a" width="500 alt="Microsoft Azure Logo"/>
</p>




<h1>Deploying A Virtual Network in Azure for Traffic Analysis</h1>

<p> 
This project Is the first amongst a collection focused on implementing Azure and Active Directory.
The goal here is to create a basic lab that mirrors a real working network environment, providing me with hands-on-learning and practical experience with Microsoft Azue, Powershell and Wireshark.
</p>


<h2>Overview </h2>

<p>In this project, I will set up and establish a connection between two virtual machines using Windows and Linux in Microsoft Azure's Cloud environment. 
This will allow me to perform a basic network traffic inspection using Wireshark.</p>

<h2>Key Objectives</h2>
<h3>Virtual Machine Setup</h3>

-  Configure and deploy Windows VM
-  Configure and deploy Linux VM

<p>
  <h3>Remote Connectivity</h3>
  
  -  Establish Remote Desktop Connection (RDP) between the Virtual Machines (VMs)
</p>

<p>
  <h3>Network Traffic Analysis</h3>
  
  -  Perform a basic network traffic inspection between both Virtual Machines using Wireshark
</p>

<h3>Environments and Technologies Used</h3>

- Microsoft Azure (Virtual Machines, Networking)
- Windows App (Remote Desktop Protocol)
- Wireshark (Traffic Analysis)
- PowerShell (Command-line Operations)

<p>
  <h3>Operating Systems Used</h3>
  </p>




| **Operating System**        | **Role**               |
|----------------------------|------------------------|
| <img alt= "windows logo" src="https://i.imgur.com/KcrV0u6.png" width="20"> Windows (Windows 10 Pro) | Windows VM) |
| <img alt= "Ubuntu logo" src="https://github.com/user-attachments/assets/87cccf20-cfc6-4950-b1ec-b480d913e7eb" width="20"> Linux (ubuntu 22.04) | Linux VM              |
<p></p>

<p>
<h1>Setup and Configuration of Virtual Machines</h1></p>


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
- Select a vm size with at least 2 vcpus
- Set a username and password
- Be sure to memorise your credentials or store in a secure place

![Creating Windows Virtual Machine](https://github.com/user-attachments/assets/192a051e-fc10-4648-aa3b-51ccd9c2bbb2)
<br><br> 
![Credentials](https://github.com/user-attachments/assets/9d35ac70-acf2-4331-9176-64c4a64ed08d)
<br><br> 
![Networking Step 1](https://github.com/user-attachments/assets/db017071-b60a-4d7e-af54-29de04be897e)
<br><br> 
<h3><img alt= "linux Ubuntulogo" src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/9e/UbuntuCoF.svg/1024px-UbuntuCoF.svg.png" width="20">  Create Linux Virtual Machine</h3>

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
Confirm that the virtual machines have been deployed to the same resource group and that they are on the same Virtual network/subnet.
This is to ensure that we can establish the remote desktop connection and perform a basic network traffic inspection.


![VM Deployed](https://github.com/user-attachments/assets/766e801c-d0b0-48ff-9932-bc2bf80414b4)
<br><br> 
<img width="586" alt="Networking" src="https://github.com/user-attachments/assets/913fdb24-bb5e-4d2f-ad4f-38c8d424502f" />
<br><br>
![image](https://github.com/user-attachments/assets/1efa6437-22d0-404e-a6c0-9e2ebff7f88a)



<h3><img alt= "RDP logo" src="https://github.com/user-attachments/assets/4aaa5d6e-ce8b-481f-a8da-57edc9a2917e" width="20"> Establish Remote Desktop Connection</h3>

- Go to [Portal.azure.com](https://portal.azure.com)
- Search for "Virtual Machines" in the Azure search bar
- Select the "windows-vm" you created earlier and copy it's Public IP address
- Launch your Remote Desktop Connection Application
- Select "Add PC"
- Choose "Add Credentials" from the drop down and enter the credentials you created earlier, noting to accept the security prompt and proceed.
- You can now establish a remote connection to your virtual machine, by right-clicking the newly added device
  
<img width="1156" alt="Add PC" src="https://github.com/user-attachments/assets/151f6ec9-b615-4ed0-a5d1-6223206b2808" />

<img width="1158" alt="Connect PC" src="https://github.com/user-attachments/assets/5774f3e0-c118-44fe-89b9-57fb4ed16075" />


<h1>Observe ICMP Traffic Using Wireshark</h1></p>

- Within your Windows virtual machine launch the Edge Browser
- Visit https://www.wireshark.org/download.html
- Download the Windows x64 Installer
- Launch the Wireshark installer
- Continue through the installation prompts
- Ensure to select the check box for install "Npcap" to allow Wireshare to capture live network data
- Launch the Wireshark Application once the installation is complete
- Select the Ethernet option which has began to display network activity
- Click the shark icon in the upper left corner of the application window to begin analysing the network traffic
- A new window will be displayed titled "Capturing from Ethernet" as shown below

<img width="1262" alt="Wireshark Launched" src="https://github.com/user-attachments/assets/2a2a75e5-0809-4342-87bb-bd40a9b23e19" />



<img width="1461" alt="image" src="https://github.com/user-attachments/assets/17d5f341-a276-4d0f-bb83-dc759b0d7cd7" />

<h3>Confirm Connection Between Domain Controller & Client Machines</h3></p>

- Using Wireshark filter for ICMP traffic
- Retrieve the private IP address of the Ubuntu Linux Virtual Machine (10.0.0.5)
- Attempt to ping Linux Virtual Machine from with the Windows 10 Virtual Machine
- Observe the ping requests and replies within Wireshark

<img width="1367" alt="Ping replies" src="https://github.com/user-attachments/assets/f49a0cdd-aeb3-4d6d-8aee-ca6ce53a7df6" />


<h3>Perpetual Pings & Network Security Groups(Firewalls)</h3>

- Initial a perpetual(non-stop-ping) from your Windows Virtual Machine to your Linux Machine using the following command:
  - "ping 10.0.0.5 -t"
- In your Windows Virtual Machine obeserve the continuos ping requests and replies between the machines in both Powershell and Wireshark
- Return to [Portal.azure.com](https://portal.azure.com)
- Open the Network Security Group your Linux Virtual Machine is using and disable incoming ICMP Traffic


![NSG Ruling](https://github.com/user-attachments/assets/030d90e2-2538-4417-9b92-a97c03d3ad38)



<h3>Adding an Inbound Security Rule</h3></p>

- Set the source as "any"
- Source port ranges as "*"
- Destination "any"
- Service "Custom"
- Destination port ranges "*"
- Protocol "ICMPv4"
- Action "Deny"
- Priority "290" to evaluate this rule first

<img width="1365" alt="Effective Firewall" src="https://github.com/user-attachments/assets/4fb5ca31-7a0b-4213-baab-385d260aec67" />
<br><br> 

- In your Windows Virtual Machine obeserve the Failing ping requests and timeout notices
- Re-enable the ICMP traffic for the Network Security Group your Virtual Machine is using and notice the replies begin to resume
- Stop the ping activities using "CTRL +C"

<h3>Making an SSH Connection & Observing Traffic</h3></p>

- Within your Windows Virtual Machines Powershell
- Enter the "SSH" followed by the private ip address of your Linux machine
- You'll be prompted for your password, enter the credentials you created earlier
- Once your connection is established you can trial running some commands like "whoami" in Powershell with the SSH filter applied in Wireshark to observe the traffic

<img width="1388" alt="SSH Filter" src="https://github.com/user-attachments/assets/4ee0fdc8-930b-48d7-9ac9-adc2b807ad1a" />




<h1>Project Summary</h1></p>

In this project, a virtual network was successfully deployed in Microsoft Azure, connecting a Windows (Windows 10 Pro) VM and a Linux (ubuntu 22.04 VM together using the Remote Desktop Connection (RDP). Wireshark was then used to capture, filter and analyze ICMP and SSH network traffic between the two virtual machines. Additionally, firewall rules in the Network Security Group (NSG) were modified to block and re-enable ICMP traffic, demonstrating network security controls and traffic filtering in a cloud environment. 








