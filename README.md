This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket on an iPad Pro!




<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- [Downloaded files contains osTicket Installation Files ](http://tinyurl.com/filesdwn)
- Azure Virtual Machine 
- iPad Pro
- Keyboard (Optional)
- Persistence

<h2>Installation of PHP,IIS URL Rewrite Module 2, Microsoft Visual C++ Redistributable </h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="create a MS Azure VM"/>
</p>
Install from the downloaded files the file named " PHPManagerForIISV1.5.0 "


<p>
<img src="https://imgur.com/7OTYMBG" height="80%" width="80%" alt="create a MS Azure VM"/>
</p>

Install from the downloaded files the file " rewrite_amd64_en-US " Also known as IIS URL Rewrite Module 2 according to the setup screen.
<p>
<img src="https://imgur.com/lYv8aUO" height="80%" width="80%" alt="create a MS Azure VM"/>
</p>

Create a folder/directory in C:\ drive and called it "PHP" final result -> C:/PHP to store the PHP files in the next steps.

Install from the downloaded files the file named " VC_redist.x86 "

<p>
<img src="https://imgur.com/MPLkcUo" height="80%" width="80%" alt="create a MS Azure VM"/>
</p>

<h2>Installation of MySQL database</h2>

Installation of file named " mysql-5.5.62-win32 " make sure to remember the password YOU enter. It will be used to access/modify/connect to the database.
* Note the default user is called "root" followed by the password you enter.


<p>
<img src="https://imgur.com/4mOEmxH" height="80%" width="80%" alt="create a MS Azure VM"/>
</p>


<h2>Installation of osTicket-v1.15.8</h2>

Open Internet Information Services (IIS) Manager.
Double click on the PHP Manager icon to ENABLE and REGISTER a new PHP version for the website.


<p>
<img src="https://imgur.com/E4Ryo2I" height="80%" width="80%" alt="create a MS Azure VM"/>
</p>


Right click on "osTicket-v1.15.8" file and select "Extract All" to unzip the files.
Copy the folder called upload into the following path "C:\inetpub\wwwroot".
<p>
<img src="https://imgur.com/Za985Py" height="80%" width="80%" alt="create a MS Azure VM"/>
</p>
Rename the folder " upload " you just copied to " osTicket ".

<p>
<img src="https://imgur.com/nsi18J7" height="80%" width="80%" alt="create a MS Azure VM"/>
</p>




Restart the Internet Information Services (IIS) by Stopping and Starting it.

Go to Sites -> Default -> osTicket
On the right side, find and click "Browse *:80".
This will launch the setup page for osTicket 
<p>
<img src="https://imgur.com/mcE5hi2" height="80%" width="80%" alt="create a MS Azure VM"/>
</p>

In Internet Information Services (IIS) click on the " PHP Manager " to ENABLE 3 extensions that are disabled.
- php_imap (imap email plugin)
- php_intl.dll (international languages)
- php_opcache.dll (improve performance via caching)
<p>
<img src="https://imgur.com/NnOrvbO" height="80%" width="80%" alt="create a MS Azure VM"/>
</p>



<h2> Configuration File for osTicket</h2>

Rename the file " ost-sampleconfig.php " in " C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php " to " ost-config.php " 

Assign Permissions: " ost-config.php"
Disable inheritance -> Remove All
New Permissions -> Everyone -> All


From Downloaded files install & launch HeidiSQL an open source data management tool.
Connect to the database via username is root & password is the one you entered during installation of MySQL.

Create a database called " osTicket"


<p>
<img src="https://imgur.com/bPytW5Y" height="80%" width="80%" alt="create a MS Azure VM"/>
</p>


Setup of the osTicket in the browser
<p>
<img src="https://imgur.com/bPytW5Y" height="80%" width="80%" alt="create a MS Azure VM"/>
</p>

For security reasons delete the folder setup in C:\inetpub\wwwroot\osTicket\setup

Set permissions to "Read" only: C:\inetpub\wwwroot\osTicket\include\ost-config.php


</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
