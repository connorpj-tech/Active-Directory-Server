<h1>Active Directory (In progress)</h1>

 ### [YouTube Demonstration](https://youtu.be/7eJexJVCqJo)

<h2>Description</h2>
This SOP will demenstrate how to deploy a Windows virtual machine in the cloud and configure an Active Directory server for managing users in a company setting
<br />


<h2>Languages and Utilities Used</h2
                                 
- <b>Microsoft Azure</b>
- <b>Remmina (RDP client)</b>
- <b>Windows Server 2025</b>

<h2>Key Steps:</h2>

**1. Setting up a Virtual Machine on Azure**

- <b> In Azure start by creating a new Virtual Machine </b>
- <b> For image, select Windows Server 2025 Datacenter -x64 Gen2 </b>
- <b> Allocate at least 8MiB and 2 CPUs </b>
- <b> Create a username and password for machine </b>
- <b> Select port 3389 for RDP </b>
- <b> For disk, select image default </b>
- <b> Click Review + Create and launch the virtual machine
<div align="left">
  <table>
    <tr>
      <td><img width="400" src="https://github.com/connorpj-tech/Active-Directory-Server/blob/main/Create%20VM.png" /></td>
      <td><img width="400" src="https://github.com/connorpj-tech/Active-Directory-Server/blob/main/Create%20VM(1).png" /></td>
      <td><img width="400" src="https://github.com/connorpj-tech/Active-Directory-Server/blob/main/Disk.png" /></td>
    </tr>
       <td align="center"><b>Virtual Machine Image</b></td>
       <td align="center"><b>Computing size/account</b></td>
       <td align="center"><b>Disk Configuration</b></td>
       </tr>
  </table>
</div>

**2. Connecting to Virtual Machine**

- <b> Under Virtual Machines in the Azure portal and click on WindowsServer2025.  Click on connect </b>
- <b> In Remmina copy the IP address and admin credentials </b>
- <b> Click on Save + Connect to remote desktop into the VM </b>
<div align="left">
 <table>
    <tr>
      <td><img width="400" alt="Connect" src="https://github.com/connorpj-tech/Active-Directory-Server/blob/main/Connect.png" /></td>
      <td><img width="400" alt="Remote Desktop Configuration" src="https://github.com/connorpj-tech/Active-Directory-Server/blob/main/RDP.png"</td>
    </tr>
       <td align="center"><b> Connect</b></td>
       <td align="center"><b> Remote Desktop Configuration</b>
       </tr>
 </table>

**3. Install Active Directory Domain Services**

- <b> Right click on Windows Icon and click System </b>
- <b> Rename machine DC </b>
- <b> Under Manage, click on Add Roles and Features </b>
- <b> In the wizard check Active Directory and Domain Services </b>
- <b> Keep all defaults and install </b>
<div alight="left">
 <table>
     <tr>
       <td><img width="400" alt="Rename Machine" src="https://github.com/connorpj-tech/Active-Directory-Server/blob/main/Rename%20Machine.png" /></td>
       <td><img width="400" alt="Roles And Services" src="https://github.com/connorpj-tech/Active-Directory-Server/blob/main/Roles%20and%20Features.png" /></td>
       <td><img width="400" alt="Active Directory and Domain Services" src="https://github.com/connorpj-tech/Active-Directory-Server/blob/main/Active%20Directory%20Domain%20Services.png" /></td>
     </tr>
        <td align="center"><b> Rename Machine</b></td>
        <td align="center"><b> Roles And Services</b></td>
        <td align="center"><b> Active Directory and Domain Services</b></td>
        </tr>
 </table>

**4. Promote to a Domain Controller**

- <b> Once AD is installed, click on flag to promote this machine to a domain controller </b>
- <b> Add new forest and name domain root mydomain.com </b>
- <b> Create password </b>
- <b> Keep everything default and click install </b>
<div align="left">
 <table>
     <tr>
      <td><img width="400" alt="Configure Domain Controller" src="https://github.com/connorpj-tech/Active-Directory-Server/blob/main/Promote%20to%20DC.png" /></td>
     </tr>
        <td align="left"><b> Configure Domain Controller</b>
      
  </tr>
 </table>


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
