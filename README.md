<h1>Nessus - Vulnerablity Management Lab</h1>


<h2>Description</h2>
This lab utilizes Nessus to conduct a vulnerability scan on a VMware virtual machine running Windows 10. This lab also involves remediating a medium severity vulnerability which is found in the virtual machine, as well as rescanning to verify the vulnerability was successfully remediated.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Nessus</b> 
- <b>VMware Workstation 17 Player</b>
- <b>Registry Editor</b>
- <b>Local Security Policy</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> 

<h2>Program walk-through:</h2>

<p align="center">
Launch VM and run "ipconfig" in command prompt to get IP address and enable remote registry in services.msc: <br/>
<img src="https://i.imgur.com/asr60lL.png" height="80%" width="80%" alt="ipconfig"/>
<img src="https://i.imgur.com/TiPvCaM.png" height="80%" width="80%" alt="ipconfig"/>
<br />
<br />
Disable user account control, add key (REG_DWPORD "LocalAccountTokenFilterPolicy") to registry to further disable user account control for remote use, and restart VM: **Not recommended for normal use, only for lab purposes only**  <br/>
<img src="https://i.imgur.com/N6NYFaU.png" height="80%" width="80%" alt="Disable User Account Control"/> <img src="https://i.imgur.com/TiPvCaM.png"/>
<br />
<br />
Create a new basic network scan, run the scan, and analyze initial results: <br/>
<img src="https://i.imgur.com/OAfEJeN.png" height="80%" width="80%" alt="Vulnerability scan"/>
<img src="https://i.imgur.com/OAQaixp.png" height="80%" width="80%" alt="Vulnerability scan"/>
<img src="https://i.imgur.com/uBZmQJW.png" height="80%" width="80%" alt="Vulnerability scan"/>
<br />
<br />
Analyze the scan results. Prioritize the highest severity vulnerablities, and start the remediation process:  <br/>
<img src="https://i.imgur.com/tgpbGDR.png" height="80%" width="80%" alt="Analyze scan results"/>
<br />
<br />
Make any necessary remediations. For this specific one, go to secpol.msc, and change the policy "Microsoft network server: Digitally sign communications (always) to "Enabled":  <br/>
<img src="https://i.imgur.com/ZQVhIZR.png" height="80%" width="80%" alt="Remediations"/>
<br />
<br />
Rescan and verify the remediations were successful:  <br/>
<img src="https://i.imgur.com/jTJUL7b.png" height="80%" width="80%" alt="Rescan and verify"/>
</p>

<h2>Final Takeaways</h2>
This project was mainly to get some experience with Nessus and vulnerability management. This was a very basic demonstration of a vulnerability scan and the remediation process that follows. I think this was a very useful lab, as vulnerability management seems to be a very big part of a security analyst's job. This project was very fun and beginner friendly. It was also very insightful overall!

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
