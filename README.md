<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used</h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Create an Azure Virtual Machine Windows 10
- Log into the VM with Remote Desktop
- Install / Enable IIS in Windows WITH CGI
- Install PHP Manager for IIS
- Install the Rewrite Module
- Create the directory C:\PHP
- Unzip PHP 7.3.8 into the “C:\PHP” folder
- Install VC_redist.x86.exe
- Install MySQL 5.5.62
- Open IIS as an Admin
- Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe)
- Reload IIS (Open IIS, Stop and Start the server)
- Install osTicket v1.15.8
- Reload IIS (Open IIS, Stop and Start the server)
- Go to sites -> Default -> osTicket
- Note that some extensions are not enabled
- Rename: ost-config.php
- Assign Permissions: ost-config.php
- Continue Setting up osTicket in the browser (click Continue)
- Install HeidiSQL
- Continue Setting up osTicket in the browser


<h2>Installation Steps</h2>

<h3>Create an Azure Virtual Machine Windows 10</h3>

![01](https://github.com/user-attachments/assets/e23b62af-c194-415a-98f9-0f0308df979a)

<h3>Log into the VM with Remote Desktop</h3>

![02](https://github.com/user-attachments/assets/f6983dad-5f6e-44ab-a75b-b1a932364573)

<h3>Install / Enable IIS in Windows WITH CGI</h3>

![03](https://github.com/user-attachments/assets/db2802d6-fc6b-4ce4-8f92-dec890e9acc0)

<h3>Install PHP Manager for IIS</h3>

![04](https://github.com/user-attachments/assets/b8917928-03ab-4fed-94fa-ff0f3a8854c2)

<h3>Install the Rewrite Module</h3>

![05](https://github.com/user-attachments/assets/4dd23521-8efc-4da6-8229-3ebf7b821423)

<h3>Create the directory C:\PHP</h3>

![06](https://github.com/user-attachments/assets/c82b1109-3128-441d-b6a9-aa49694e1457)

<h3>Unzip PHP 7.3.8 into the “C:\PHP” folder</h3>

![07](https://github.com/user-attachments/assets/5cf44599-2bd1-44ae-a6e0-828671000d95)

<h3>Install VC_redist.x86.exe</h3>

![08](https://github.com/user-attachments/assets/9349ba87-32a5-46bf-9c4e-7a0f44e4c141)

<h3>Install MySQL 5.5.62</h3>

![09](https://github.com/user-attachments/assets/2094510f-676a-48cd-bb61-16fd8ab563dc)

<p>Typical Setup</p>
<p>Launch Configuration Wizard (after install) -></p>
<p>Standard Configuration</p>
<p>Username: root</p>
<p>Password: root</p>

<h3>Open IIS as an Admin</h3>

![10](https://github.com/user-attachments/assets/56a09829-44bc-4832-b885-6db44799212b)

<h3>Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe)</h3>

![11](https://github.com/user-attachments/assets/a4ae83b5-0f2a-4cbd-853d-f38f21267695)

<h3>Reload IIS (Open IIS, Stop and Start the server)</h3>

![12](https://github.com/user-attachments/assets/8eac56c7-b3bb-441b-bd2e-f884ef583e7d)

<h3>Install osTicket v1.15.8</h3>

<p>From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”</p>

![13](https://github.com/user-attachments/assets/26f93c15-4ba6-4b8d-8bab-a010950c5be9)

![14](https://github.com/user-attachments/assets/8704e810-0c1d-4ed5-806b-ad103f141b25)

<p>Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”</p>

![15](https://github.com/user-attachments/assets/b3aaaaa4-d777-4f28-8979-92ab35e0aefb)

<h3>Reload IIS (Open IIS, Stop and Start the server)</h3>

<h3>Go to sites -> Default -> osTicket</h3>

<p>On the right, click “Browse *:80”</p>

![16](https://github.com/user-attachments/assets/b871ba7a-3140-4154-a410-048725686bcb)

<h3>Note that some extensions are not enabled</h3>
<p>Go back to IIS, sites -> Default -> osTicket</p>
<p>Double-click PHP Manager</p>

![17](https://github.com/user-attachments/assets/906995fe-2688-4a12-a3f4-3c59416e9b82)

<p>Click “Enable or disable an extension”</p>
<p>Enable: php_imap.dll</p>
<p>Enable: php_intl.dll</p>
<p>Enable: php_opcache.dl</p>

![18](https://github.com/user-attachments/assets/a52655b0-5993-4136-8c54-0fa9d939358d)

<p>Refresh the osTicket site in your browser, observe the changes</p>

<h3>Rename: ost-config.php</h3>

<p>From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php</p>

![19](https://github.com/user-attachments/assets/b46d5051-7ddd-4eef-adb6-813261596127)

<p>To: C:\inetpub\wwwroot\osTicket\include\ost-config.php</p>

![20](https://github.com/user-attachments/assets/224fb5af-5bcb-44e1-8546-0978c186fd84)

<h3>Assign Permissions: ost-config.php</h3>
<p>Disable inheritance -> Remove All</p>
<p>New Permissions -> Everyone -> All</p>

![21](https://github.com/user-attachments/assets/1b54999a-c57f-4097-8917-d5644eff15ec)

![22](https://github.com/user-attachments/assets/9d332cee-6a4a-4d2f-ab08-5463dfd03381)

![23](https://github.com/user-attachments/assets/51d0eb4b-a670-486e-8542-9b03d1acf79b)

![24](https://github.com/user-attachments/assets/ba4b3725-e219-437a-bfa0-396da91e6298)

![25](https://github.com/user-attachments/assets/dcfd602e-23a8-4568-8d3e-56a02010bd55)

<h3>Continue Setting up osTicket in the browser (click Continue)</h3>

<p>Name Helpdesk</p>
<p>Default email (receives email from customers)</p>

![26](https://github.com/user-attachments/assets/774cae18-e2d6-4c53-aee8-91d6254eb580)

<h3>Install HeidiSQL</h3>

![27](https://github.com/user-attachments/assets/8f4261a3-f7ec-43c8-b319-c7dfeb29d712)

<p>Open Heidi SQL</p>
<p>Create a new session, root/root</p>
<p>Connect to the session</p>
<p>Create a database called “osTicket”</p>

![28](https://github.com/user-attachments/assets/f2f345be-5223-4375-afc8-0871d9638072)

![29](https://github.com/user-attachments/assets/ff1ac668-dfa9-47e4-bacd-4b5e785463de)

<h3>Continue Setting up osTicket in the browser</h3>
<p>MySQL Database: osTicket</p>
<p>MySQL Username: root</p>
<p>MySQL Password: root</p>
<p>Click “Install Now!”</p>

![30](https://github.com/user-attachments/assets/238f78e0-2dd1-4a26-b751-591ba7f8e436)

