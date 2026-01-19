<h1>Active Directory (In progress)</h1>

 ### [YouTube Demonstration](https://youtu.be/7eJexJVCqJo)

<h2>Description</h2>
This SOP will demenstrate how to provision a Windows virtual machine in the cloud and configure an Active Directory server
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
      <td><img width="400" src="https://github.com/connorpj-tech/Active-Directory-Server/blob/main/Create%20New%20Machine.png" /></td>
      <td><img width="400" src="https://github.com/connorpj-tech/Active-Directory-Server/blob/main/Hardware%20Configuration.png" /></td>
      <td><img width="400" src="https://github.com/connorpj-tech/Active-Directory-Server/blob/main/Storage%20Configuration.png" /></td>
    </tr>
       <td align="center"><b>Launching KVM</b></td>
       <td align="center"><b>Hardware Configuration</b></td>
       <td align="center"><b>Hard Disk Configuration</b></td>
       </tr>
  </table>
</div>

**2. Installing and configuring Windows Server**

- <b> Go to the new resource and click connect.  Use the public IP to access the virtual machine using RDP client</b>
- <b> Click on add roles and features to add Active Directory </b>
- <b> Go through the wizard and select Active Directory Domain Services </b>
- <b> Click install </b>
- <b> Create an Administrator password </b>
- <b> Login as Administrator and start Windows </b>
<p align="center">
 <table>
    <tr>
      <td><img width="400" alt="Installing Windows" src="https://github.com/connorpj-tech/Active-Directory-Server/blob/main/Install%20Windows.png" /></td>
      <td><img width="400" alt="Select Image" src="https://github.com/connorpj-tech/Active-Directory-Server/blob/main/Select%20Image.png"</td>
      <td><img width="400" alt="Disk Partition" src="https://github.com/connorpj-tech/Active-Directory-Server/blob/main/Disk%20Partition.png"</td> 
      <td><img width="400" src="https://github.com/connorpj-tech/Active-Directory-Server/blob/main/Set%20Password.png" /></td>
      <td><img width="400" src="https://github.com/connorpj-tech/Active-Directory-Server/blob/main/Login%20As%20Administrator.png"</td>
    </tr>
       <td align="center"><b> Installing Windows</b></td>
       <td align="center"><b> Select Image</b>
       <td align="center"><b> Disk Partition</b>
       <td align="center"><b> Set Password</b>
       <td align="center"><b> Login As Administrator</b> 
       </tr>
 </table>

**3. Promote to a Domain Controller**

- <b> Right click on Windows Icon and select system.  Change the PC name to DC (Domain Controller) </b>
- <b> Restart machine, click on flag to promote this machine to a domain controller </b>
- <b> Add new forest and name domain root mydomain.com </b>
- <b> Create password </b>
- <b> Keep everything default and click install </b>
<p align="center">
 <table>
     <tr>
      <td><img width="400" alt="Device Manager" src= </td>
  </tr>
 </table>
 
 **4. Configuring Windows Server**

- <b> Select Add Roles and Features
- <b> Select Role Based

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
