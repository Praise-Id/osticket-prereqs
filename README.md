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

- Windows 10 Enterprise LTSC 2021

<h2>Prerequisite Files</h2>

- [osTicket installation files](https://drive.usercontent.google.com/download?id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD&export=download)

<h2>Installation Steps</h2>

<h4>
Download the zip folder and unzip it onto your desktop. The folder should be called “osTicket-Installation-Files” - We will use the files in this folder to install osTicket and some of the dependencies
</h4>
<p>
<img width="1002" height="525" alt="image" src="https://github.com/user-attachments/assets/cc9127fa-d545-488c-b460-5b422a356c34" />
</p>

<br />

<h4>Next, enable IIS(Internet Information Services) & CGI(Common Gateway Interface) on Windows</h4>

- Open Control Panel. You can find this by clicking the Start menu, typing "Control Panel," and then clicking it.
- Click "Uninstall a program." You'll find this under the "Programs" section of Control Panel.
- Click "Turn Windows features on or off." It's usually on the left side of the page, near the top.
- A window will pop up with a big list of checkboxes.
- Find "Internet Information Services" in the list and click its checkbox. This turns on the main feature we need.
- A little arrow or plus sign will appear next to it — this means there are more options hidden inside. Click to expand it.
- Inside that, find "World Wide Web Services" and check its box too. This will open up even more sub-options.
- Inside that list, find "Application Development Features" and check its box. Yep, more sub-options will appear — that's normal.
- Somewhere in that final list, you'll see "CGI." Check that box. This is the specific piece we actually need.
- Click "OK" at the bottom of the window. Windows will now install everything you checked. This might take a minute or two — just let it finish.
<p>
<img width="972" height="616" alt="image" src="https://github.com/user-attachments/assets/b6fc8c32-2bfc-41e5-ad46-947d93585344" />
</p>


<br />

<h4>Next, install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi) from the “osTicket-Installation-Files” folder</h4>

- Open the “osTicket-Installation-Files” folder.
- Look inside for a file called "PHPManagerForIIS_V1.5.0.msi".
- Double-click the file to launch the installation wizard.
- Click Next, agree to the license agreement, then click Next again.
- When prompted for permission, click Yes.
- The PHP Manager will install automatically. Once it's finished, close the wizard.
<p>
<img width="1896" height="549" alt="image" src="https://github.com/user-attachments/assets/1f9f909a-01eb-47c5-97ec-05b8a4960430" />
</p>


<br />

<h4>Next, install the Rewrite Module (rewrite_amd64_en-US.msi) from the “osTicket-Installation-Files” folder</h4>

- Open the “osTicket-Installation-Files” folder.
- Look inside for a file called "rewrite_amd64_en-US.msi".
- Double-click the file to launch the installation wizard.
- Accept the terms in the license agreement, click Install.
- The Rewrite Module will install automatically. Once it's finished, close the wizard.
<p>
<img width="1248" height="494" alt="image" src="https://github.com/user-attachments/assets/82cce92a-cc48-4d69-9200-2b4ec1f77b22" />
</p>


<br />

<h4>Next, create a new directory on your C: drive named C:\PHP.</h4>

- Open File Explorer
- Navigate to the C: drive (Windows (C:))
- Create a new folder named PHP.
<p>
<img width="1013" height="660" alt="image" src="https://github.com/user-attachments/assets/dedbb501-1e76-4be6-804a-8091ece218bd" />
</p>


<br />

<h4>Next, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) from the “osTicket-Installation-Files” folder into the “C:\PHP” folder.</h4>

- Open the “osTicket-Installation-Files” folder.
- Find the file named "php-7.3.8-nts-Win32-VC15-x86.zip".
- Right-click the file and select "Extract All" from the menu that pops up.
- A window will open titled "Select a Destination and Extract Files."
- Click Browse, then find and select the PHP folder you created earlier — this tells your computer where to put the extracted files.
- Click Select, then click Extract.

<p>
<img width="722" height="586" alt="image" src="https://github.com/user-attachments/assets/d1abd8b0-e691-48f9-a902-9064a5b22380" />
</p>

<br />

<h4>Next, install "VC_redist.x86.exe" from the “osTicket-Installation-Files” folder</h4>

- Open the “osTicket-Installation-Files” folder.
- Look inside for a file called "VC_redist.x86.exe".
- Double-click the file to launch the installation wizard.
- Accept the terms in the license agreement, click Install.
- When prompted for permission, click Yes.
- "VC_redist.x86.exe" will install automatically. Once it's finished, close the wizard.
<p>
<img width="1236" height="399" alt="image" src="https://github.com/user-attachments/assets/5d3b800b-088d-40f2-9cd0-29dea4d817e0" />
</p>


<br />

<h4>Next, install MySQL 5.5.62 (mysql-5.5.62-win32.msi) from the “osTicket-Installation-Files” folder</h4>

- Open the “osTicket-Installation-Files” folder.
- Look inside for a file named "mysql-5.5.62-win32.msi".
- Double-click the file to launch the installation wizard.
- Click Next, agree to the license agreement, then click Next again.
- When you get to the select setup page, select the Typical setup, then click Install.
- When prompted for permission, click Yes.
- MySQL will install automatically. Once it's finished, make sure the box for "Launch the MySQL Instance Configuration Wizard" is checked, then click Finish.
<p>
<img width="1679" height="795" alt="image" src="https://github.com/user-attachments/assets/dc78345f-0ee3-4dab-9ff0-aa3ccbe0ca2e" />
</p>


<br />

<h4>Next, Configure MySQL</h4>

- When the MySQL Instance Configuration Wizard opens, click Next.
- Select Standard Configuration, then click Next.
- Leave the next page as-is, then click Next.
- On the next page, check Modify Security Settings, create a password (make sure it's one you won't forget), then click Next.
- Click Execute, then click Finish.
<p>
<img width="1641" height="796" alt="image" src="https://github.com/user-attachments/assets/998ca6fa-61d8-46e1-aa2f-d02f39e63189" />
</p>


<br />

<h4>Next, open IIS as an Admin</h4>

- Click the Start menu and type "IIS" or "Internet Information Services".
- When Internet Information Services (IIS) Manager appears in the search results, right-click it.
- Select "Run as administrator" from the menu.
- If prompted for permission, click Yes to allow it to open.
<p>
<img width="981" height="619" alt="image" src="https://github.com/user-attachments/assets/856e57b3-79a0-4991-bec0-017a7baa6fad" />
</p>


<br />

<h4>Register PHP from within IIS</h4>

- In the middle panel, under the IIS section, double-click PHP Manager.
- In the PHP Manager pane, click "Register new PHP version".
- A dialogue box will open asking you to browse for the PHP executable.
- Click Browse, navigate to your PHP folder (C:\PHP), and select the file "php-cgi.exe".
- Click OK to confirm.

<br />

<h4>Next, Reload ISS</h4>

- In the Connections panel on the left, right-click your server name.
- In the Actions panel on the right, click "Stop" to stop the server.
- Wait a moment, then click "Start" in the same Actions panel to start the server back up.
<p>
<img width="932" height="364" alt="image" src="https://github.com/user-attachments/assets/3cddc6a0-0214-4680-959c-646d20fc938f" />
</p>


<br />

<h4>Next, Install osTicket from the “osTicket-Installation-Files” folder</h4>

- Open the “osTicket-Installation-Files” folder.
- Find the zipped folder named "osTicket-Installation-Files".
- Unzip (extract) this folder.
- Inside the unzipped folder, locate the "upload" folder and copy it.
- Navigate to your C: drive, open "inetpub", then open "wwwroot".
- Paste the "upload" folder into "wwwroot".
- Rename the pasted "upload" folder to "osTicket".
<p>
<img width="1261" height="691" alt="image" src="https://github.com/user-attachments/assets/65cf3fe5-ac52-4426-8360-6f9e080cc9a1" />
</p>


<br />

<h4>Next, Reload ISS</h4>

- Open IIS Manager (as Administrator).
- In the Connections panel on the left, right-click your server name.
- In the Actions panel on the right, click "Stop" to stop the server.
- Wait a moment, then click "Start" in the same Actions panel to start the server back up.
<p>
<img width="932" height="364" alt="image" src="https://github.com/user-attachments/assets/3cddc6a0-0214-4680-959c-646d20fc938f" />
</p>


<br />

<h4>Next, load the osTicket site</h4>

- Open IIS Manager (as Administrator).
- In the Connections panel on the left, expand the drop-down for your server name.
- Expand "Sites", then expand "Default Web Site"
- Select osTicket, then click "Browse*:80" in the Actions panel on the right.
<p>
<img width="1424" height="742" alt="image" src="https://github.com/user-attachments/assets/ecbcd7b3-c2d5-41da-8fbf-59ae6abbd217" />
<img width="990" height="652" alt="image" src="https://github.com/user-attachments/assets/8835360e-de98-4c72-97f1-57530a29f8b1" />
</p>


<br />

<h4>Note: we have not yet enabled some of the recommended extensions.</h4>

<p>
<img width="567" height="434" alt="image" src="https://github.com/user-attachments/assets/4f6d7f2d-1da2-46b5-bd7b-12aa27a8dc7d" />
</p>


<br />

<h4>Next, enable recommended PHP extensions</h4>

- Go back to IIS Manager, and navigate to Sites -> Default Web Site -> osTicket.
- Double-click PHP Manager.
- Click "Enable or disable an extension."
- Enable the following: "php_imap.dll", "php_intl.dll", "php_opcache.dll"
- Refresh the osTicket site in your browser and observe the changes.

<p>
<img width="958" height="1005" alt="image" src="https://github.com/user-attachments/assets/eb268a77-f3f8-45fa-a1dd-feaf509ae989" />
</p>


<br />

<h4>Rename the Config File</h4>

- Navigate to your C: drive, open "inetpub", open "wwwroot", open "osTicket".
- Open the folder named  "include".
- Find the file named "ost-sampleconfig.php", and rename the file to "ost-config.php".

<p>
<img width="750" height="561" alt="image" src="https://github.com/user-attachments/assets/17f7e93b-6d1e-4780-b2ef-2ada4717bce1" />
</p>


<br />

<h4>Assign Permissions to the Config File</h4>

- While still in the C:\inetpub\wwwroot\osTicket\include folder, right-click the file "ost-config.php".
- Select "Properties" from the menu. In the Properties window, click the "Security" tab.
- Click "Advanced", in the Advanced Security Settings window, click "Disable inheritance".
- A popup will ask how you'd like to proceed. Click "Remove all inherited permissions from this object".
- In the new window, click the blue link that says "Select a principal".
- In the "Enter the object name to select" field, type Everyone, click "Check Names", then click OK.
- Under "Basic permissions," check the box for "Full control", click OK to close this window.
- Click Apply, click OK to close the Advanced Security Settings window.
- Click OK one more time to close the Properties window.
  
<p>
<img width="1653" height="771" alt="image" src="https://github.com/user-attachments/assets/c35fe324-0a9c-4375-98a9-61f1bc6c5fd8" />
</p>


<br />

<h4>Next, continue setup in the browser</h4>

- Switch back to your web browser showing the osTicket setup page.
- Click the "Continue" button.
- In the "Helpdesk Name" field, type a name for your Helpdesk.
- In the "Default Email Address" field, type an email address that will receive support tickets from customers.
- Fill in any other required fields on this page (such as Admin username, password, and email — follow the on-screen labels).
- Do not fill in the database settings yet.
  
<p>
<img width="1553" height="598" alt="image" src="https://github.com/user-attachments/assets/53f5559e-f281-4b0d-bcc0-a4d8cab56a5a" />
</p>


<br />

<h4>Next, Install HeidiSQL (HeidiSQL_12.3.0.6589_Setup)</h4>

- Open the “osTicket-Installation-Files” folder.
- Look inside for a file named "HeidiSQL_12.3.0.6589_Setup".
- Double-click the file to launch the installer, click Install.
- If prompted for permission, click Yes.
- Once installation completes, click Finish (this may automatically open HeidiSQL, or you can find it later via the Start menu).
- In the HeidiSQL "Session manager" window, click "New".
- A new session will appear in the list on the left, with its name field editable — you can leave the default name or rename it.
- On the right side, make sure "Network type" is set to "MySQL (TCP/IP)".
- In the "User" field, leave it as the default.
- In the "Password" field, type the password you created when configuring MySQL.
- Leave "Hostname / IP" as 127.0.0.1 and Port as 3306 (defaults), click "Open".
- Once connected, you'll see a panel on the left listing your databases.
- Right-click anywhere in that left panel and select "Create new," then "Database".
- In the popup, type osTicket as the database name.
- Leave other settings as default, then click OK.
  
<p>
<img width="950" height="449" alt="image" src="https://github.com/user-attachments/assets/0c00283a-cb7e-432c-897d-865646ddab25" />
</p>


<br />

<h4>Next,  complete osTicket setup in the browser</h4>

- Switch back to your web browser showing the osTicket setup page.
- Scroll to the database configuration section.
- Fill in the fields as follows: MySQL Hostname: localhost (if not already filled in), MySQL Database: osTicket, MySQL Username: your SQL username, MySQL Password: your SQL password.
- Scroll down and click the "Install Now!" button.
- Wait while the installer creates the necessary database tables — this may take a minute or two.
  
<p>
<img width="306" height="235" alt="image" src="https://github.com/user-attachments/assets/35f2499f-2e14-4314-a0fe-420e65b6d70c" />
</p>


<br />

<h4>Next,  log into osTicket</h4>

- Congratulations — hopefully it installed with no errors!
- Once setup is complete, you'll typically see a confirmation page with next steps.
- Open a new browser tab and go to your helpdesk login page: http://localhost/osTicket/scp/login.php
- Log in using the admin credentials you created during setup.
- End users can access the support portal at: http://localhost/osTicket/
  
<p>
<img width="527" height="418" alt="image" src="https://github.com/user-attachments/assets/6179a4a0-6313-443f-bc69-314ff57d622f" />
</p>


<br />

<h4>Next, clean up (optional)</h4>

- Open File Explorer.
- Navigate to This PC -> Local Disk (C:) -> inetpub -> wwwroot -> osTicket.
- Find the folder named "setup", and delete it.
- In the same folder, navigate to the "include" folder.
- Right-click the file "ost-config.php" and select "Properties", click the "Security" tab.
- Click "Edit...", select "Everyone" from the list of user names.
- In the "Allow" column below, uncheck all boxes except "Read" and "Read & execute".
- Click OK to save, click OK again to close the Properties window.

<br />


<h6>Prerequisite files & steps gotten from<a href="https://coursecareers.com/course/it"> Course Careers IT Course</h6>
