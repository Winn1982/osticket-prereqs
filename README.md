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

- Windows 10</b> (22H2)

<h2>List of Prerequisites</h2>

- Create Windows 10 Pro Virtual Machine
- Download osTicket Installation Files
- Enable IIS with CGI
- Install VC Redistributable 
- Install MySQL

<h2>Installation Steps</h2>

![image](https://github.com/user-attachments/assets/dce7d148-55c0-4055-b112-2caecaea1ab5)

I created a Windows 10 Pro Virtual Machine named "os-Ticketvm". I will be using this virtual machine to complete the os Ticket lab. 
</p>
<br />

![image](https://github.com/user-attachments/assets/7a449eb7-75aa-4609-8975-838f48696486)

I downloaded os Ticket to the desktop on the Windows 10 virtual machine. 
</p>
<br />

![image](https://github.com/user-attachments/assets/3204b05d-0014-4f72-a96f-44c64776f2ca)
![image](https://github.com/user-attachments/assets/acf3976f-b4ea-4087-b87b-84a98e3662e7)
![image](https://github.com/user-attachments/assets/981c9f3c-1afe-444d-8fda-c71f70f4a4b8)

I went into Control Panel, uninstall a program and clicked turned Windows Features On/Off, I clicked the box next to Internet Information Services (IIS), I then went into World Wide Web Services and Application Development Features and turned on CGI and then the web server began installation.  
</p>
<br />

![image](https://github.com/user-attachments/assets/0a8a15b5-c90b-4a5c-80d0-dbebc7bc1f8c)

I confirmed the web server was installed by going to IP address 127.0.0.1 and the default web page that IIS issues. 

![image](https://github.com/user-attachments/assets/56fb2673-5111-480b-ac89-f89a1642fe0b)

I then returned to the os Ticket installation file and downloaded PHP Manager for IIS.

![image](https://github.com/user-attachments/assets/d644f58d-1814-4eff-9f1b-78e156517558)

After installing PHP Manager I am going to install rewrite_amd64

![image](https://github.com/user-attachments/assets/4461eb5b-e681-4c04-86d0-83dbc0f4c1ea)

I then created a new folder on the C: Drive called "PHP".

![image](https://github.com/user-attachments/assets/f9ebb0b2-a66e-44b0-b5c1-572fe96b9683)

I will then extract the PHP 7.3.8 NTS folder to the PHP folder that was just created. 


