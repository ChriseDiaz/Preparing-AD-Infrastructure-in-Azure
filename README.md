<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1
- Step 2
- Step 3
- Step 4

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
1.Create a Resource Group:

Go to the Azure portal and create a new resource group for organizing your resources.

2.Create a Virtual Network and Subnet:

Create a virtual network (VNet) to ensure network connectivity.
Define a subnet within the VNet for your Domain Controller VM.

3.Create the Domain Controller VM (Windows Server 2022):

Launch a Windows Server 2022 VM, naming it "DC-1."
Set up a username (labuser) and password (Cyberlab123!) during VM creation.

4.Set NIC Private IP to Static:

After the VM is created, go to the Network Interface (NIC) settings of the VM and set the Private IP address to be static.

5.Log into the VM and disable Windows Firewall (for testing connectivity):

Log into the VM using Remote Desktop Protocol (RDP).
Disable the Windows Firewall temporarily to test connectivity (do this with caution for testing purposes).



</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
1.Create the Client VM (Windows 10) named “Client-1”:

Launch a Windows 10 VM named "Client-1."
Set up the username (labuser) and password (Cyberlab123!) during VM creation.

2.Attach Client-1 to the same region and Virtual Network as DC-1:

Ensure the VM is in the same Azure region and connected to the same Virtual Network (VNet) as the Domain Controller (DC-1).

3.Set DNS settings to DC-1’s Private IP:

After VM creation, go to Client-1’s network settings and set the DNS server to the private IP address of DC-1.

4.Restart Client-1 from the Azure Portal:

Use the Azure portal to restart the Client-1 VM.

5.Log in to Client-1 and test connectivity:

Log in to Client-1.
Attempt to ping DC-1’s private IP address and ensure the ping succeeds.

6.Check DNS settings on Client-1:

Open PowerShell on Client-1 and run ipconfig /all.
Verify that the DNS settings show DC-1’s private IP address.
</p>
<br />
