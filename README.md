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
<p>
Download the zip folder and unzip it onto your desktop. The folder should be called “osTicket-Installation-Files” - We will use the files in this folder to install osTicket and some of the dependencies
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<h4>The next step is enabling IIS(Internet Information Services) & CGI(Common Gateway Interface) on Windows</h4>

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
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
