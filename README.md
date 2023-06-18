<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Configuring Network File Permissions with Active Directory</h1>
In this tutorial we'll dive into the on-premises Active Directory within Azure Virtual Machines.<br />



<br /><h2>Environments & Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (22H2)


<br /><h2>Learning About Active Directory</h2>

<br /><p>
<img src="https://i.imgur.com/xoAWKZ0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/7v2iKcm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create two virtual machines (DC-1 & Client-1). The image setting for DC-1 is <b>Windows Server 2022</b>. Login to DC-1 - from the Server Manager window, select <b><i>Add Roles & Features</i></b> - select <b><i>Active Directory Domain Services</i></b>. A pop-up will appear click on <b><i>Promote this server to a domain controller</i></b>. This will complete the Active Directory install and turn the server into a domain controller. When prompted, make sure to add a new forest and create a root domain name. Now that Active Directory is installed, we need to restart. Restarting may disconnect the virtal machine - if this happens, just login again to DC-1 to reconnect. Active Directory has created default user and security groups.
</p>
<br />
<p>
<img src="https://i.imgur.com/flafRfK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/KnIj9XV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/ruxVM8E.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Client-1 sent a ping command to mainframe but no such host file exists within the DNS lookup (Domain Name System). We'll need to create a host file. Switching back to DC-1, open the Server Manager window go to <b><i>Tools</i></b> --> <b><i>DNS Manager</i></b> --> select DC-1 --> Domain list of A records (host name to doamin mapping). Right-click then select <b><i>New Host</i></b> --> type in <b><i>mainframe</i></b> --> set IP to DC-1 --> <b>Add Host</b>. Client-1 can now ping to mainframe.
</p>
<br />
<p>
<img src="https://i.imgur.com/AbICeA9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/IMt84Mr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 To allow file shares, select the folder read access – right-click -go to properties – sharing – hit share

Type in domain user hit add – share

Now the file is shared. 

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />









----no use
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
