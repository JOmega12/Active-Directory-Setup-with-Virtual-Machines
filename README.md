
<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>


<h1>Active Directory Setup</h1>
This tutorial outlines the setup for Active Directory(AD)
<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)
- Remote Desktop Connection
- Azure Virtual Machine
  -  DC-1 and Client-1 Setup

<h2> Objectives</h2>

- Create Domain Controller(dc-1) Virtual Machine and Client(client-1) Virtual Machine on Azure
  - Dc-1 Image will be the data center as shown in the picture
  - Client-1 Image will be the Windows 10 version 
- Establish connectivity between the two Virtual Machines
- Double check connectivity from Client to Domain Controller by pinging the Controller

<h2>Creating Domain Controller and Client Virtual Machines</h2>

This is DC-1
![create-dc-1-ad](https://github.com/user-attachments/assets/27a116cb-6c3c-48b4-acb8-8b1b6a80d860)

This is Client-1
![create-client-1-ad](https://github.com/user-attachments/assets/8807ff0e-0521-4fc8-9d1a-e06a7b3b2aa0)

You also need to create the virtual network where both the virtual machines will be working with:
![create-ad-network](https://github.com/user-attachments/assets/30af0da4-f62e-4db4-9cc5-c9f645c48e71)



<h3>Establishing Connection between the two Virtual Machines</h3>

- Make DC-1 Ip address static because you want the domain controller to be the DNS server so that the IP address doesnt change. DC-1's static address will now be 10.0.0.4 no matter how many times the virtual machine has restarted
![setDC1NetworkToStatic](https://github.com/user-attachments/assets/579740d8-9c11-4be9-b9e1-b6bdf7dc7209)

- Next access your DC-1 firewall
- ![HowToAccessWindowsFirewall](https://github.com/user-attachments/assets/a18c2957-bf9f-4edd-94a8-5fb0f06b0ccc)
- Disable Firewall of DC-1
- ![TurnOffWindowsFirewall](https://github.com/user-attachments/assets/2e415790-e057-4b12-9dbd-b3d8fd580fe5)


<h3>Checking Connectivity by pinging </h3>

Connect the DNS server of Client1 to DC1
![ConnectDNSClient1ToDC1](https://github.com/user-attachments/assets/4916b844-c58f-4da6-ad37-d02f367f3c18)

Within Client 1 and open powershell

Ping Domain Controller 1 with `ping (private IP address of DC-1)`
![PingDC1](https://github.com/user-attachments/assets/d7ec4e80-3a9d-4765-8b70-e057dbdabd8e)


Observe and make sure the ping is successfull
![CheckingIfDNSConnectToDC1](https://github.com/user-attachments/assets/4b2f003d-d4cb-4f50-b36a-2352ad9b37b0)

<br />
<h2>Conclusion</h2>

<p>Once you've setup in this project, this Active Directory serves as a basis for future projects and implementation!</p>
- If you want to see how to use the Active Directory, click on the next project: <a href="https://github.com/JOmega12/Active-Directory-Deployment-and-Configuration">Next Project</a>

<br />
