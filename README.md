<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>


<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- PHP Manager for IIS
- IIS Rewrite Module
- PHP 7.3.8
- Microsoft Visual C++
- MySQL
- HeidiSQL

<h2>Installation Steps</h2>
<p>
I'm currently on portal.azure.com, where I've established a resource group. Upon completion, I proceed to create a Virtual Machine running Windows 10, configured with 4 virtual CPUs.
</p>
<p align="center">
<img src="https://i.imgur.com/IAQwOJX.png" height="60%" width="60%" />
</p>
<p align="center">
<img src="https://i.imgur.com/huiTMpp.png" height="60%" width="60%" />
</p>

<p>
Once that is done, I am using the public IP address and connecting it to the remote desktop. In the control menu, I clicked on the icon that says uninstall a program and selected turn windows features on and off.
<p>
I have selected Install/Enable IIS folder in windows and activated CGI and Common HTTP Features
<p>
-	World Wide Web Services -> Application Development Features ->[X]CGI [X]Common HTTP Features
<p>
  Next, I have selected the IIS Management Console folder.
  <p>
-	Internet Information Services -> Web Management Tools -> IIS Management Console [X]IIS Management Console
</p>
<p align="center">
<img src="https://i.imgur.com/72GXbfW.png" height="40%" width="40%" />
</p>
<p>
I am checking to see if IIS is installed in the web browser and searched 127.0.0.1.
</p>
<p align="center">
<img src="https://i.imgur.com/0ej018Y.png" height="60%" width="60%" />
</p>
<p>
I have downloaded and installed the PHP Manager for IIS.
</p>
<p align="center">
<img src="https://i.imgur.com/wa9XJqG.png" height="60%" width="60%" />
</p>
<p>
I have downloaded and installed the Rewrite Module
</p>
<p align="center">
<img src="https://i.imgur.com/G8kT9O7.png" height="60%" width="60%" />
</p>
<p>
I have downloaded and installed PHP 7.3.8 and unzipped the contents into C:\PHP
</p>
<p align="center">
<img src="https://i.imgur.com/emVJjwM.png" height="60%" width="60%" />
</p>
<p>
Next I have downloaded and installed VC_redist.x86.exe
</p>
<p align="center">
<img src="https://i.imgur.com/szePMjd.png" height="60%" width="60%" />
</p>
<p>
I have downloaded and installed MySQL 5.5.62 and in the following screens I have selected Typical Setup.
</p>
<p align="center">
<img src="https://i.imgur.com/oBXmDrQ.png" height="60%" width="60%" />
</p>
<p>
In the next screen I have selected Launched Configuration Wizard, the next screen Standard Configuration and made a new root password.
</p>
<p align="center">
<img src="https://i.imgur.com/hlOM7ha.png" height="60%" width="60%" />
</p>
<p>
I have opened IIS as an Admin and selected PHP Manager.
</p>
<p align="center">
<img src="https://i.imgur.com/tV3F8Rr.png" height="60%" width="60%" />
</p>
<p>
I have registered PHP within IIS and provided a path for the PHP executable file. Once I am in C:\, I am now selecting PHP and clicked on php-cgi file.  
</p>
<p align="center">
<img src="https://i.imgur.com/hgzzhRi.png" height="60%" width="60%" />
</p>
<p>
I have reload IIS and installed osTicket v1.15.8. I have extracted and copied the ‘upload’ folder to c:\inetpub\wwwroot. In the same folder, I have renamed ‘upload’ to ‘osTicket’ 
</p>
<p align="center">
<img src="https://i.imgur.com/G1bFu8j.png" height="60%" width="60%" />
</p>
<p align="center">
<img src="https://i.imgur.com/ExlF4dE.png" height="60%" width="60%" />
</p>
<p>
I have reloaded IIS again and on the left side I have clicked sites -> Default -> osTIcket. On the right side, I have clicked ‘Browse *.80’.
It has lead to the osTicket installer page and it shows that not all extension are enabled.
</p>
<p align="center">
<img src="https://i.imgur.com/ywcaFsZ.png" height="60%" width="60%" />
</p>
<p>
I have went back to IIS, clicked sites -> Default -> osTicket. I have doubled click PHP manager, clicked ‘Enable or disable an extension’
In the next screen that is labeled ‘enable or disable an extension’. I have enabled -> php_imap.dll, php_intl.dll, and php_opcache.dll.
I have reloaded the osTicket installer page and observed the new changes.
</p>
<p align="center">
<img src="https://i.imgur.com/MPFC0rL.png" height="60%" width="60%" />
</p>
<p align="center">
<img src="https://i.imgur.com/Qsz2nIC.png" height="60%" width="60%" />
</p>
<p>
In the osTicket folder, I have rename ost-sampleconfig.php to ost-config.php. 
</p>
<p align="center">
<img src="https://i.imgur.com/r3xORfL.png" height="60%" width="60%" />
</p>
<p>
Once the file has been renamed, I have right click on the file and selected properties. I have clicked security, clicked on advance and disabled inheritance and selected remove all. Next I clicked new permissions -> everyone -> all.
</p>
<p align="center">
<img src="https://i.imgur.com/4bMoDkS.png" height="40%" width="40%" />
</p>
<p>
I have continued to setup osTicket in the browser. I have now clicked ‘continue’ on the osTicket browser page. I have filled out the page and continue to install more programs to set the final requirements for osTicket.
</p>
<p align="center">
<img src="https://i.imgur.com/R1jXSso.png" height="60%" width="60%" />
</p>
<p>
I have downloaded and installed HeidiSQL 
</p>
<p align="center">
<img src="https://i.imgur.com/R6Tk5an.png" height="60%" width="60%" />
</p>
<p>
In HeidiSQL, I have right click on the left side that says ‘Unnamed’, select ‘create new’, and selected ‘database’. I have named the new database osTicket. Once the new database is set, I have went back to the browser for the osTicket page and finished the MySQL database info.
</p>
<p align="center">
<img src="https://i.imgur.com/T552pjD.png" height="60%" width="60%" />
</p>
<p>
The final steps for osTicket in the browser
•	MySQL Database: osTicket
•	MySQL Username: root
•	MySQL Password: Password1
•	Click ‘Install Now!’
Once everything is installed, in the next screen it will give a congratulations page.
</p>
<p align="center">
<img src="https://i.imgur.com/siezGtX.png" height="60%" width="60%" />
</p>
<p>
The last step is to clean up, I have deleted the setup folder, set the permissions back to ‘Read’ in ost-config.php file, and browsed to the help desk login page: http://localhost/osTicket/scp/login.php. The login page has successfully been loaded.
</p>
<p align="center">
<img src="https://i.imgur.com/swLbMQA.png" height="40%" width="40%" />
</p>
