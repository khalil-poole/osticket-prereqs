<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

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

1. Create a Virtual Machine, ensuring that we create a brand new Resource Group as well. Set the image and size as shown in the screenshots for the VM (Virtual Machine). Create a unique username and password, and check the box for the licensing agreement. Followed by clicking "Review + Create" for validation and creation of the VM.

![image](https://github.com/user-attachments/assets/50bf3736-3bcb-409e-90b8-7a2f7cecedb9)

![image](https://github.com/user-attachments/assets/18219c66-e57e-4523-a4e7-7d2f9f706919)

![image](https://github.com/user-attachments/assets/c2ffb510-1b05-4334-9102-45cee4ade58d)

![image](https://github.com/user-attachments/assets/7a62cb41-81e3-4c86-9779-2659aa3fd157)


2. Open up Remote Desktop and login to the VM with its public IP Address and the created credentials. While inside the VM, download the required dependeices for osTicket to work by going here -> https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD

