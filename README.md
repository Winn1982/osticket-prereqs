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
- Install osTicket

<h2>Installation Steps</h2>

![image](https://github.com/user-attachments/assets/dce7d148-55c0-4055-b112-2caecaea1ab5)

I created a Windows 10 Pro Virtual Machine named "os-Ticketvm". I will be using this virtual machine to complete the os Ticket lab. 
</p>
<br />

![image](https://github.com/user-attachments/assets/7a449eb7-75aa-4609-8975-838f48696486)

I downloaded osTicket to the desktop on the Windows 10 virtual machine. 
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

![image](https://github.com/user-attachments/assets/5ff93a8b-16a7-418a-9784-6527f9b62528)

I checked the C:PHP folder created to ensure the files were extracted properly. 

![image](https://github.com/user-attachments/assets/ec320927-549e-4e33-a8f7-d423ac1d6e50)

Next, we will install the VC_redistributable file from the os Ticket installation folder. 

![image](https://github.com/user-attachments/assets/65ec1e55-628e-4c16-af5b-9c7515f3e5bb)

I will install the MySQL 5.5 file from the os Ticket installation file. 

![image](https://github.com/user-attachments/assets/8660bf3e-d800-435d-907f-d38a928687a7)

I am now going to register PHP from IIS. This will make the web server aware of the computer's PHP presence. To do this we will stop and restart the server. 

![image](https://github.com/user-attachments/assets/b2f2394f-f13f-4abd-ae14-3ecf5e09454f)

I then extracted osTicket to our os Ticket installation folder. 

![image](https://github.com/user-attachments/assets/38538cec-bc89-4c82-93a1-5cc2ad2c5ba9)

I am going to copy the upload folder into inetpub and then change the name of upload to "os ticket". 

![image](https://github.com/user-attachments/assets/3a862144-413b-45ea-b989-704fe3b24db8)

I am then going to try and go to the actual os Ticket website.

![image](https://github.com/user-attachments/assets/b51e7a5f-9538-42fa-8689-eeb2a617c48d)

I successfully browsed to osTicket and opened the browser to osTicket. 

![image](https://github.com/user-attachments/assets/8b991a79-44d9-40f3-9306-1ec5f8cf51e0)

I am  now going to enable some extensions that are not enabled yet, they are php_imap.dll,  php_intl.dll, and php_opcache.dll

![image](https://github.com/user-attachments/assets/c4d53009-4485-4c5f-8430-1944eec1b22a)

To ensure the extensions were enabled we refreshed the webpage and see the green checkmarks on some red extensions. 

![image](https://github.com/user-attachments/assets/bc42466b-f24b-49d9-8d29-6981b3ab80af)
![image](https://github.com/user-attachments/assets/8dc8b6c3-b167-414a-882e-568e4a92b78f)

I renamed "ost-sampleconfig" to "ost-config" and disabled inheritance and removed all and then clicked new permissions and enabled everyone and gave them full access (this would not happen in real life, but is just for the lab's purpose). I will then stop and start the IIS server.

![image](https://github.com/user-attachments/assets/ec48d080-9188-4dd5-a909-0d9065e632eb)

I am going to install Heidi SQL.

![image](https://github.com/user-attachments/assets/b3d1dd01-d7be-4c77-a33d-f1cd69cc7093)

I am going to create a new database called "osTicket".

![image](https://github.com/user-attachments/assets/511670c6-ec37-4e6d-b2da-b8c32cc1c094)

Now that I have Heidi SQL setup, we are going to continue the installation process for osTicket. 

![image](https://github.com/user-attachments/assets/db476c65-56f3-44cf-a899-149e7ddbfd04)

I see that it was successful in installing osTicket. 

![image](https://github.com/user-attachments/assets/ed66bbc8-1965-45b9-8c90-062b50d4f40d)

This is the admin user login page. 

![image](https://github.com/user-attachments/assets/e3eed21a-c7de-422a-8012-4da6f801910a)

This is the login page where we will be "creating tickets" to work on. 
