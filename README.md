 <h1> Vulnerability Management</h1>


 <h2> Description</h2>
Setup Nessus Essentials to scan local VMs hosted on VMWare Workstation in order to run credentialed scans to discover vulnerabilities, remediate some of the vulnerabilities, and then perform a rescan to verify remediation
<br/>

<h2> Environments Used</h2>
<b1> Windows 10 Pro</b1> 22h2

<h2> Step by Step Walkthrough </h2>

<p align="center">
Created a VM in VMWare w/ Bridged Network: <br/>
<img src="https://i.imgur.com/660aGYX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Setup Nessus Essential:  <br/>
<img src="https://i.imgur.com/aol6tMK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Pinged IP of VM from your machine which will result in Request timed out: <br/>
<img src="https://i.imgur.com/5Id6mK8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Ran wf.msc to access the firewall from VM:  <br/>
<img src="https://i.imgur.com/NsmstbL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Disabled Firewalls:  <br/>
<img src="https://i.imgur.com/fn8phtS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Pinged VM again with firewall off:  <br/>
<img src="https://i.imgur.com/nHOXfw1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Ran the first scan on Nessus Essential.<br/> Reviewed the scan mostly info:
<img src="https://i.imgur.com/6MLTQtX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
On the VM enabled Remote Registry:  <br/>
<img src="https://i.imgur.com/gdrQAZP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Enabled File and Print Sharing:  <br/>
<img src="https://i.imgur.com/RPLS3aO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Disabled UAC:  <br/>
<img src="https://i.imgur.com/aKp3cdF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Created DWORD (32-bit) in :  <br/> Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System
<img src="https://i.imgur.com/CUI0pWG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Add credentials in Nessus Essentials:  <br/>
<img src="https://i.imgur.com/jO8IKf1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Ran another scan with noticing more crits and high vulnerabilities:  <br/>
<img src="https://i.imgur.com/sQuTKSi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/YoBA8GN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Reviewed remediations:  <br/>
<img src="https://i.imgur.com/ayyXlIY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Installed Mozilla Firefox 3.6.12 on VM:  <br/>
<img src="https://i.imgur.com/acL4IXU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
After installation of Mozilla Firefox 3.6.12 ran another scan:  <br/>
<img src="https://i.imgur.com/BG96UBa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/f0z9sJ3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Ran Windows Update, Uninstalled Mozilla Firefox:  <br/>
<img src="https://i.imgur.com/JEpx0HT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/5d7qWWs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Ran another scan after Remediating the issues:  <br/>
<img src="https://i.imgur.com/V0ADJxK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
