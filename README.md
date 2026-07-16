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

<p>
<img width="1002" height="525" alt="image" src="https://github.com/user-attachments/assets/cc9127fa-d545-488c-b460-5b422a356c34" />
</p>
<h4>
Download the zip folder and unzip it onto your desktop. The folder should be called “osTicket-Installation-Files” - We will use the files in this folder to install osTicket and some of the dependencies
</h4>
<br />

<p>
<img width="972" height="616" alt="image" src="https://github.com/user-attachments/assets/b6fc8c32-2bfc-41e5-ad46-947d93585344" />
</p>
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

<br />

<p>
<img width="1896" height="549" alt="image" src="https://github.com/user-attachments/assets/1f9f909a-01eb-47c5-97ec-05b8a4960430" />
</p>
<h4>Next, install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi) from the “osTicket-Installation-Files” folder</h4>

- Open the “osTicket-Installation-Files” folder.
- Look inside for a file called "PHPManagerForIIS_V1.5.0.msi".
- Double-click the file to launch the installation wizard.
- Click Next, agree to the license agreement, then click Next again.
- When prompted for permission, click Yes.
- The PHP Manager will install automatically. Once it's finished, close the wizard.

<br />

<p>
<img width="1248" height="494" alt="image" src="https://github.com/user-attachments/assets/82cce92a-cc48-4d69-9200-2b4ec1f77b22" />
</p>
<h4>Next, install the Rewrite Module (rewrite_amd64_en-US.msi) from the “osTicket-Installation-Files” folder</h4>

- Open the “osTicket-Installation-Files” folder.
- Look inside for a file called "rewrite_amd64_en-US.msi".
- Double-click the file to launch the installation wizard.
- Accept the terms in the license agreement, click Install.
- The Rewrite Module will install automatically. Once it's finished, close the wizard.

<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<h4>Next, create a new directory on your C: drive named C:\PHP.</h4>

- Open File Explorer
- Navigate to the C: drive (Windows (C:))
- Create a new folder named PHP.

<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<h4>Next, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) from the “osTicket-Installation-Files” folder into the “C:\PHP” folder.</h4>

- Open the “osTicket-Installation-Files” folder.
- Find the file named "php-7.3.8-nts-Win32-VC15-x86.zip".
- Right-click the file and select "Extract All" from the menu that pops up.
- A window will open titled "Select a Destination and Extract Files."
- Click Browse, then find and select the PHP folder you created earlier — this tells your computer where to put the extracted files.
- Click Select, then click Extract.

<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<h4>Next, install "VC_redist.x86.exe" from the “osTicket-Installation-Files” folder</h4>

- Open the “osTicket-Installation-Files” folder.
- Look inside for a file called "VC_redist.x86.exe".
- Double-click the file to launch the installation wizard.
- Accept the terms in the license agreement, click Install.
- When prompted for permission, click Yes.
- "VC_redist.x86.exe" will install automatically. Once it's finished, close the wizard.

<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<h4>Next, install MySQL 5.5.62 (mysql-5.5.62-win32.msi) from the “osTicket-Installation-Files” folder</h4>

- Open the “osTicket-Installation-Files” folder.
- Look inside for a file called "mysql-5.5.62-win32.msi".
- Double-click the file to launch the installation wizard.
- Click Next, agree to the license agreement, then click Next again.
- When you get to the select setup page, select the Typical setup, then click Install.
- When prompted for permission, click Yes.
- MySQL will install automatically. Once it's finished, make sure the box for "Launch the MySQL Instance Configuration Wizard" is checked, then click Finish.

<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<h4>Next, Configure MySQL</h4>

- When the MySQL Instance Configuration Wizard opens, click Next.
- Select Standard Configuration, then click Next.
- Leave the next page as-is, then click Next.
- On the next page, check Modify Security Settings, create a password (make sure it's one you won't forget), then click Next.
- Click Execute, then click Finish.

<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<h4>Place Holder</h4>

- Placeholder

<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<h4>Place Holder</h4>

- Placeholder

<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<h4>Place Holder</h4>

- Placeholder

<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<h4>Place Holder</h4>

- Placeholder

<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<h4>Place Holder</h4>

- Placeholder

<br />
