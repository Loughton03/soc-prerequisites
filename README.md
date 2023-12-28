<p align="center">
<img src="https://i.imgur.com/8I0YcgP.png" alt="Azure logo"/>
</p>

<h1>Azure Resource Creation</h1>
In this portion of the lab, we will create our virtual enviornments on Microsoft Azure.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- SQL Server


<h2>Operating Systems Used</h2>

- Windows 10</b> (21H2)
- Ubuntu Linux</b> (21H2)


<h2>Installation Steps</h2>

<h3>-Windows VM Setup</h3>

<p>
1. Create a Windows 10 Pro Virtual Machine and name the Resource Group "RG-Cyber-Lab". Name your VM and select a region.
</p>
<br />

<p>
<img src="https://i.imgur.com/RiKnW2C.png" height="80%" width="80%" alt="Windows Resource Group Setup"/>
</p>
<p>
2. Continue to the networking section and name the Virtual Network "Lab-VNet".
</p>
<br />

<p>
<img src="https://i.imgur.com/gsS9tjd.png" height="80%" width="80%" alt="Virtual Machine Setup"/>
</p>
<p>
3. Next we'll check the VM settings and create our Windows vm!
</p>
<br />

<h3>-Linux VM Setup</h3>


<p>
<img src="https://i.imgur.com/icXQLrC.png" height="80%" width="80%" alt="Public IP Address"/>
</p>
<br />

<p>
1. We will begin the next section of our lab by creating a Ubuntu Linux Virtual Machine and name the Resource Group "RG-Cyber-Lab". Name your VM and select a region.
</p>
<br />

<p>
2. Continue to the networking section and name the Virtual Network "Lab-VNet".
</p>
<br />

<p>
<img src="https://i.imgur.com/1ygdJtk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
3. Next we'll check the VM settings and create our Linux vm!
</p>
<br />


<p>
<img src="https://i.imgur.com/sNimdvJ.png" height="80%" width="80%" alt="Internet Installation Services installation"/>
</p>
<p>
Now that we have this installed, let's download the installation files needed for osTicket and HeidiSQL.
</p>
<br />

<p>
<img src="https://i.imgur.com/n9NDKgB.png" height="80%" width="80%" alt="Internet Installation Services installation"/>
</p>
<p>
Now head to the installation folders.

•	From the Installation Files, download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi) 
•	From the Installation Files, download and install the Rewrite Module (rewrite_amd64_en-US.msi).

Create a directory C:\PHP.
</p>
<br />

<p>
<img src="https://i.imgur.com/BsYhvqG.png" height="80%" width="80%" alt="Create a PHP Folder in the C directory"/>
</p>
<p>
Download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) from the Installation Files and unzip the contents into C:\PHP 

•	From the Installation Files, download and install VC_redist.x86.exe. 
•	From the Installation Files, download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi). 

Next, download osTicket, and extract the content to the folder c:\inetpub\wwwroot. Rename the folder "Upload" to "osTicket."
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open IIS Manager as an Admin, Register the PHP using the PHP folder.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In IIS Manager, open PHP Manager. We need to enable three extensions named php_imap.dll, php_intl.dll, php_opcache.dll Now reload IIS manager and make your way to "Sites > Default > osTickets. Click " Browse *:80" on the right to open the osTicket web interface.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
It should look like this.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Perfect. Now let's return to c:\inetpub\wwwroot\osticket\include. Look for the file named "ost-sampleconfig.php" We will rename it to "ost-config.php." Once completed, right-click the file, and open properties, under the security tab, "Disable Inheritance." Then Remove all new permissions, and give everyone permissions.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
HeidiSQL From the Installation Files, download and install HeidiSQL.

 •	Open Heidi SQL 
•	Create a new session, root/Password1 
•	Connect to the session 
•	Create a database called "osTicket" 

Let's return to osTicket in the web interface. Name the Helpdesk and remember your login credentials. 

##Continue Setting up osticket in the browser 

•	MySQL Database: osTicket 
•	MySQL Username: root 
•	MySQL Password: Password1 
•	Click "Install Now!"
</p>
<p>
<img src="https://i.imgur.com/cPxyIZe.png" height="80%" width="80%" alt="osTicket Installer"/>
</p>

<p>
<img src="https://i.imgur.com/TGmrZnu.png" alt="osTicket Installer Complete"/>
</p>
<br />

<p>
osTicket should be up and running with no issues. We will now move on the Post Installation Config.
</p>
<br />

