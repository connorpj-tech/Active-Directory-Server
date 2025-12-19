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
- <b> Select local install media and chose Microsoft Server 2022 ISO file </b>
- <b> Allocate at least 2048MiB and 2 CPUs.  Enable 40GiB for storage </b>
- <b> Name: Windows_Server_2022, click finish to start machine </b>
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

- <b> Select Install Windows Server</b>
- <b> Select the Windows Server 2025 Standard Evaluation (Desktop Experience) </b>
- <b> Select Disk 0 to install Windows onto </b>
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

**3. Network Setup**

- <b> Right click on Windows Icon and select device manager
- <b> Click on Network and under actions select add legacy hardware
- <b> Select from list and click on network adapters
- <b> Manufactor: Microsoft, Model: Microsoft KM-Test.  Install
- <b> Under View Network Connections, rename new interface "Internal", right click on new adapter and select properties
- <b> Select properties for Internet Control Protocol 4
- <b> Use the following IP address: 172.16.0.1, Subnet Mask: 255.255.255.0
- <b> Use the following DNS server address: 127.0.0.1 and click ok </b>
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
