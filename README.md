<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
In this lab, I install osTicket from the ground up using the necessary installation files. There are a few steps to take before the installation of the ticketing system. This lab is done using a Windows 10 Pro VM made on Azure. The necessary installation files that are referenced and used are located <a href="https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6">here!</a><br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop Connection
- Internet Information Services (IIS)
- MySQL

<h2>Operating Systems Used </h2>

- Windows 10 Pro</b> (21H2)


<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/m6Bek7Y.png" height="80%" width="80%" alt="Installation Steps"/>
</p>
<p>
Before installing any files, iInternet Information Services (IIS0 needs to be enabled. We are installing osTicket locally and it needs IIS in order to function. To turn on IIS, open the control Panel. From the Control Panel, Open Programs and turn Windows Features On or Off. Within this menu, expand Internet Information Services, expand Web Management Tools, and enable IIS Management Console. Click and expand World Wide Web Services and expand Application Development Features. In Application Development Features, enable CGI and click ok to confirm.
</p>
<br />

<p>
<img src="https://i.imgur.com/RB5YByC.png" height="80%" width="80%" alt="Installation Steps"/>
</p>
<p>
After enabling IIS, download and install PHP Manager for IIS (PHPManagerforIIS_V1.5.0msi) from the installation files folder. Download and install the Rewrite Module (rewrite_amd64_en-US.msi) after installing PHP Manager for IIS. 
</p>
<br />

<p>
<img src="https://i.imgur.com/neliVrg.png" height="80%" width="80%" alt="Installation Steps"/>
</p>
<p>
After installing the Rewrite Module, create a new folder/directory called C:\PHP on the Windows (C:) drive This new folder will be used to unzip the contents from the PHP 7.3.8-nts-Win32-VC15-x86.zip) zip folder download from the installation files. Extract all contents from the zip folder into the C:\PHP folder.
</p>
<br />

<p>
<img src="https://i.imgur.com/mYKZExi.png" height="80%" width="80%" alt="Installation Steps"/>
</p>
<p>
Next, download and install VC_redist.x86.exe from the installation files. 
</p>
<br />

<p>
<img src="https://i.imgur.com/UW2eIpW.png" height="80%" width="80%" alt="Installation Steps"/>
</p>
<p>
Next, download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi) from the installation. Select Standard Configuration and select Install As Windows Service and make sure Launch the MySQL Server automatically is checked. For credentials, the username will be root and the password is Password1. In a practical setting, the credentials will be basic to where they can be easily guessed. For the purposes of this lab, the standard credentials root and Password1 will do.
</p>
<br />

<p>
<img src="https://i.imgur.com/9ylqXGk.png" height="80%" width="80%" alt="Installation Steps"/>
<img src="https://i.imgur.com/KoK1Lug.png" height="80%" width="80%" alt="Installation Steps"/>
</p>
<p>
Before installing osTicket, configurations need to be made within IIS. Open IIS as an admin and select PHP Manager. Within PHP Manager , select Register new PHP versoni. Select Brrowse and select the PHP CGI executable file (php-cgi.exe)within the PHP folder created earlier in the lab. After registering the PHP version, reload the IIS server within the management console.
</p>
<br />

<p>
<img src="https://i.imgur.com/ivQmua0.png" height="80%" width="80%" alt="Installation Steps"/>
</p>
<p>
From the installation files, download osTicket v1.15.8. Extract and copy the "upload" folder to the following path: c:\inetpub\wwwroot folder, rename "upload" to osticket."Reload the IIS server afterwards. 
</p>
<br />

<p>
<img src="https://i.imgur.com/s856Cpz.png" height="80%" width="80%" alt="Installation Steps"/>
<img src="https://i.imgur.com/pNkLVo6.png" height="80%" width="80%" alt="Installation Steps"/>
<img src="https://i.imgur.com/Mpq7ybU.png" height="80%" width="80%" alt="Installation Steps"/>
</p>
<p>
