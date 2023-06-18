# LLMNR-Poisoning

<h1>LLMNR Poisoning</h1>


<h2>Description</h2>
Project consists of a simple PowerShell script that walks the user through "zeroing out" (wiping) any drives that are connected to the system. The utility allows you to select the target disk and choose the number of passes that are performed. The PowerShell script will configure a diskpart script file based on the user's selections and then launch Diskpart to perform the disk sanitization.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Responder</b> 
- <b>Hashcat</b>

<h2>Environments Used </h2>

- <b>Kali Linux</b>
- <b>Windows 10</b> (21H2)

<h2>Program walk-through:</h2>

<p align="center">
Starting Responder: <br/>
<img src="https://github.com/JarredWhite1/LLMNR-Poisioning/blob/main/responder1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Reaching out to our Atttacking IP from Windows target machine:  <br/>
<img src="https://github.com/JarredWhite1/LLMNR-Poisioning/blob/main/responder2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
"Failed to resolve" error on target Windows machine: <br/>
<img src="https://i.imgur.com/nCIbXbg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Attack machine captures NTLMv2 hashes!:  <br/>
<img src="https://i.imgur.com/cdFHBiU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Making a file with the hashes in it:  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Cracking the hashes with hashcat on our host Windows machine:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Cracked the password!  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 LLMNR Poisoning Defense  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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


