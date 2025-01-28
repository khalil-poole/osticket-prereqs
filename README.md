<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com/watch?v=WRr7XhbUlJg&ab_channel=BrandonBroderick)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- MySQL

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Azure Virtual Machine
- Internet Information Services (IIS)
- PHP Manager
- Rewrite Module
- VC Redist
- MySQL
- Heidi SQL
- osTicket v1.15.8
- Link to downloads: https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD

<h2>Installation Steps</h2>

<h3>Step 1: Create a Virtual Machine</h3> 
Ensuring that we create a brand new Resource Group as well. Set the image and size as shown in the screenshots for the VM (Virtual Machine). Create a unique username and password, and check the box for the licensing agreement. Followed by clicking "Review + Create" for validation and creation of the VM.

![image](https://github.com/user-attachments/assets/50bf3736-3bcb-409e-90b8-7a2f7cecedb9)

![image](https://github.com/user-attachments/assets/18219c66-e57e-4523-a4e7-7d2f9f706919)

![image](https://github.com/user-attachments/assets/c2ffb510-1b05-4334-9102-45cee4ade58d)

![image](https://github.com/user-attachments/assets/7a62cb41-81e3-4c86-9779-2659aa3fd157)


<h3>Step 2: Open up Remote Desktop</h3>

Login to the VM with its public IP Address and the created credentials (for Mac users, please install Microsoft Remote Desktop). While inside the VM, download the required dependeices for osTicket to work by going here: [https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD](https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD)

After downloading, you want to click on the folder icon, and drag the downloaded folder unto the desktop.

![image](https://github.com/user-attachments/assets/8446f2c6-95e6-4c2b-9e3c-26e86b09a8f9)

We'll then extract the folder by right clicking the folder and click "Extract All". From there, we'll unzip the contents to the Desktop by clicking "Extract" in the new window.

![image](https://github.com/user-attachments/assets/fe990b16-e86a-4589-b1ea-307889198792)

![image](https://github.com/user-attachments/assets/b199e913-cd70-414f-972c-fd8b18ad7303)

After the unzip process, we won't need the zipped folder anymore, so we can safely put it into the Recycle Bin like so.

![image](https://github.com/user-attachments/assets/e8be3e29-8478-4f8e-afdc-eb3dc64b1e15)

<h3>Step 3:Enable Internet Interface Services (IIS) with Windows</h3>  

Start by going to the searchbar and typing up "Control Panel" and then open up Control Panel.

![image](https://github.com/user-attachments/assets/bd02b979-c336-4770-a2d8-221e5bd7fd76)

Then we go to Programs -> Programs and Features -> and finally on the left pane, we'll click on "Turn Windows features on or off"

![image](https://github.com/user-attachments/assets/76534928-46b0-4c8f-bd4c-fde81393697a)

Everything that's inside the red rectangles is what will be used and must be turned on for this installation to work. Afterwards, click OK. Once the process is over, click "Close"

![image](https://github.com/user-attachments/assets/7953ab7f-f563-441b-8e21-a45d6b9a22df)

<h3>Step 4: Installing packages and dependinces for osTicket</h3> 

From the “osTicket-Installation-Files” folder, install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)

From the “osTicket-Installation-Files” folder install the Rewrite Module (rewrite_amd64_en-US.msi)

Create the directory C:\PHP as shown below

![image](https://github.com/user-attachments/assets/77e6cb0a-ccf1-4041-8975-a104aafacbb4)

From the “osTicket-Installation-Files” folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder.

![image](https://github.com/user-attachments/assets/7ddc7137-b4f9-46ce-824b-b1e5971d1877)


From the “osTicket-Installation-Files” folder, install VC_redist.x86.exe.

From the “osTicket-Installation-Files” folder, install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
Typical Setup ->
Launch Configuration Wizard (after install) ->
Standard Configuration ->

Leave this particular screen the same

![image](https://github.com/user-attachments/assets/1382dab1-e159-4b5d-9d0d-f45903e3f652)


Username: root


Password: root


Username and Password goes here:

![image](https://github.com/user-attachments/assets/181ae8b2-876c-4c4b-9b57-1ab5605ddef9)

Click Next, and then click "Execute" to begin the MySQL Server installation.

Let's go back to the desktop screen and in the searchbartype in "IIS" and then right click and "Run as Administrator".

![image](https://github.com/user-attachments/assets/005258b6-bd52-4e15-9f32-778757af47f1)

The IIS window should open, we're going to register the PHP from within IIS. We'll go into the PHP Manager and then click where it says "Register new PHP version".

![image](https://github.com/user-attachments/assets/9c1b6c57-96b2-48d5-af0d-bcd87c67c6f1)

![image](https://github.com/user-attachments/assets/529eea9b-8b20-426b-9410-25f57735fbed)

A new window will open, and we're going to our PHP folder that we created, and look for "php-cgi" and open that file.

![image](https://github.com/user-attachments/assets/c90965cb-22a2-4af1-b1b9-a496497e6265)

Let's go back into the IIS home screen and then stop and then restart the server.

![image](https://github.com/user-attachments/assets/f3d704ea-4da9-4235-882f-24fc093ba961)

Install osTicket v1.15.8
From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”
Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”.

Reload IIS (Open IIS, Stop and Start the server). If you still had IIS running, stop the server, then open IIS again as an administrator, followed by starting the server.

Go to sites -> Default -> osTicket
On the right, click “Browse *:80”

![image](https://github.com/user-attachments/assets/e3987fd2-7cba-4b93-abed-b38697d3e381)

Note that some extensions are not enabled
Go back to IIS, sites -> Default -> osTicket
Double-click PHP Manager
Click “Enable or disable an extension”
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll
Refresh the osTicket site in your browser, observe the changes

![image](https://github.com/user-attachments/assets/edf5fd23-5606-4a14-8213-56cbc007f9eb)


Rename: ost-config.php
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

![image](https://github.com/user-attachments/assets/0231d7a2-4c40-4477-b4e6-36116373f1f7)


Assign Permissions: ost-config.php

Right click on ost-config.php -> Properties 

Security -> Advanced

Disable inheritance -> Remove All

New Permissions -> Everyone -> All

![image](https://github.com/user-attachments/assets/e0a95ea0-8b09-4f13-a2f1-e70116216022)

![image](https://github.com/user-attachments/assets/57daf35d-1b32-4aaa-9340-04c1e3aedef0)

![image](https://github.com/user-attachments/assets/b01bcd96-b74c-4b50-9331-849b0f22fc9d)


Ensure all boxes are checked

![image](https://github.com/user-attachments/assets/58f6040a-fd56-405e-b515-b4902d5c0d86)


Then click  OK -> Apply -> OK -> OK

From the “osTicket-Installation-Files” folder, install HeidiSQL.

Open Heidi SQL

Create a new session, root/root

![image](https://github.com/user-attachments/assets/e4257146-a2e7-4b82-98c8-2f197b0cef9e)

Connect to the session

Right click and then create a database called “osTicket”

![image](https://github.com/user-attachments/assets/2b38876b-5c5e-4c69-8bd2-5b1f7966f376)

Continue Setting up osTicket in the browser

If you get lost, go back to IIS and follow these instructions:

Go to sites -> Default -> osTicket

On the right, click “Browse *:80”

The web browser will then open up the osTicket setup page.

(click Continue)
Name Helpdesk
Default email (receives email from customers, use an email that you're not using for business)

For the Admin User, make sure that the email is seperate from the Helpdesk's email.

Create a username and password for the Admin User and save the information for later.

MySQL Database: osTicket

MySQL Username: root

MySQL Password: root

Click “Install Now!”

Congratulations, hopefully it is installed with no errors!

Browse to your help desk login page: http://localhost/osTicket/scp/login.php

End Users osTicket URL:

http://localhost/osTicket/ 

Last Step: Clean Up
Delete: C:\inetpub\wwwroot\osTicket\setup

Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php


![image](https://github.com/user-attachments/assets/29bf760c-2e3d-4613-b643-3d33ed9649c1)


This concludes the tutorial,  I highly suggest to keep the VM until the osTicket project is completely finished, as we'll need it for the next tutorial. However, if you need to take a break or come back at a later time, this is how you can stop the VM. 


![image](https://github.com/user-attachments/assets/92abfa3a-0dc5-4284-8fde-ab364f9f546d)



With that said, check out part 2 when you're ready -> [osTicket: Post-Installation Configuration](https://github.com/khalil-poole/osTicket-post-installation)



