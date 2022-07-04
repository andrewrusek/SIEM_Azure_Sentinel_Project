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
Create Virtual Machine of Windows 10 Pro in Microsoft Azure: <br/>
<img src="https://imgur.com/H7CfgFF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Create a Log Analytic Workspace with Azure:   <br/>
<img src="https://imgur.com/AOFHWr9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Set LAW data collection to "All Events": <br/>
<img src="https://imgur.com/hOcJuje.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Connect LAW to Virtual Machine:   <br/>
<img src="https://imgur.com/Bx2s6jO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Add Inbound port rules so RDP Port 3389 and Port 0 are open:  <br/>
<img src="https://imgur.com/uqxHDet.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Run PowerShell script to create Log file:  <br/>
<img src="https://imgur.com/X2dgQP6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Log File output:  <br/>
<img src="https://imgur.com/X2dgQP6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe created Users and DHCP Address Lease:  <br/>
<img src="https://imgur.com/xkw7NwI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Confirm connection in CLIENT1 under created User: jbezos and check for network connectivity:  <br/>
<img src="https://imgur.com/WO1FCIL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
