<h1>SIEM Microsoft Azure/Sentinel World Map RDP Failure Tracker</h1>


<h2>Description</h2>
Project consists of creating a Virtual Machine Lab environment to monitor and track RDP login attempts from around the world.  With the use of Microsoft Azure I was able to create a Windows 10 Pro Virtual Machine with an open RDP port.  After setting up the architechture of the Azure environment and creating Log Analytic Workspaces I used a simple PowerShell script to log data from Event Viewer with the failed RDP login attempts. The PowerShell script also used a Geolocation API to create logs of latitude, longitude, and country data from IP addresses associated with the failed attempts. With Microsoft Sentinel I used that data to plot and track exactly when and where these attacks took place on a World Map. 
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>Microsoft Azure</b>
- <b>Microsoft Sentinel</b>
- <b>Microsoft Sentinel</b>
- <b>Remote Desktop Connection</b>
- <b>Log Analytic Workplaces</b>

<h2>Environments Used </h2>

- <b>Windows 10 Pro</b>

<h2>Project walk-through:</h2>

<p align="center">
Create Virtual Machine of Windows 10 Pro in Microsoft Azure<br/>
<img src="https://imgur.com/H7CfgFF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Rename Ethernet Adapters and Set Internal NIC to desired IP,Mask,Gateway,DNS:  <br/>
<img src="https://imgur.com/odaGn1E.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Configure Local Server for Active Directory Domain Services: <br/>
<img src="https://imgur.com/rXPlLxA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Configure Local Server for Remote Acces and install NAT:  <br/>
<img src="https://imgur.com/WN2kGxm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Configure Local Server for DHCP:  <br/>
<img src="https://imgur.com/DEo4T6K.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Create Scope for DHCP between 172.16.0.100-200:  <br/>
<img src="https://imgur.com/3SgUQeW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Run PowerShell Script while Unrestricted to add Users from .txt file:  <br/>
<img src="https://imgur.com/BL2XUHp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe created Users and DHCP Address Lease:  <br/>
<img src="https://imgur.com/xkw7NwI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Confirm connection in CLIENT1 under created User: jbezos and check for network connectivity:  <br/>
<img src="https://imgur.com/WO1FCIL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
