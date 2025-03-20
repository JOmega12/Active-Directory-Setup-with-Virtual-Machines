
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



<h3>Establishing Connection between the two Virtual Machines</h3>

Make DC-1 Ip address static because you want the domain controller to be the DNS server so that the IP address doesnt change. DC-1's static address will now be 10.0.0.4 no matter how many times the virtual machine has restarted


Disable Firewall of DC-1
<h3>Checking Connectivity by pinging </h3>

Connect the DNS server of Client1 to DC1

Within Client 1 and open powershell

Ping Domain Controller 1 with `ping (private IP address of DC-1)`
Observe and make sure the ping is successfull

<br />
<h2>Conclusion</h2>

<p>Once you've setup in this project, this Active Directory serves as a basis for future projects and implementation!</p>
- If you want to see how to use the Active Directory, click on the next project: <a href="https://github.com/JOmega12/Active-Directory-Deployment-and-Configuration">Next Project</a>

<br />
