<h1>Active Directory (In progress)</h1>

 ### [YouTube Demonstration](https://youtu.be/7eJexJVCqJo)

<h2>Description</h2>
Project consists of a setting up a functional Active Directory server in a virtualized environment.  This lab will demonstrate how to set up a domain controller, configuring network adapters, and connecting a client to the server.  Will also be using a Powershell script that will automatically create numerous user accounts and setting up group policies for users
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>KVM</b>

<h2>Environments Used </h2>

- <b>Windows 2022 Server</b>
- <b>Windows 10 Pro</b>

<h2>Lab Walk-through:</h2>

**1. Setting up Virtulization With KVM**

- <b> Select New to create a new virtual machine </b>
- <b> Select local install media </b>
- <b> Choose Microsoft Server 2022 ISO file</b>
- <b> Allocate at least 2048MiB and 2 CPUs </b>
- <b> Enable 40GiB of storage </b>
- <b> Name: Windows_Server_2022 </b>
- <b> Click on finish to start machine </b>
<div align="left">
  <table>
    <tr>
      <td><img width="400" src="https://github.com/connorpj-tech/Active-Directory-Server/blob/main/Create%20New%20Machine.png" /></td>
      <td><img width="400" src="https://i.imgur.com/esCpSbH.png" /></td>
      <td><img width="400" src="https://i.imgur.com/SfPFR8u.png" /></td>
    </tr>
       <td align="center"><b>Launching KVM</b></td>
       <td align="center"><b>Hardware Configuration</b></td>
       <td align="center"><b>Hard Disk Configuration</b></td>
       </tr>
  </table>
</div>

**2. Setting up Network Configuration**

- <b> Click on Settings on the main screen </b>
- <b> Toggle on Expert and click on Network
- <b> Click on Adapter 2 and checkmark Enable Network Adapater
- <b> Attached to: Internal Network
- <b> Click okay
<p align="center">
 <table>
    <tr>
      <td><img width="400" alt="Configuring Network" src="https://i.imgur.com/gv7PzLy.png" /></td>
    </tr>
       <td align_"center"><b> Configuring Network</b></td>
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
