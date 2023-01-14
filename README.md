
<p align="center">

<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10 Pro </b>

<h2>List of Prerequisites</h2>

- Web Platform Installer
- PHP Manager for IIS
- osTicket
- My SQL
- HeidiSQL

<h2>Installation Steps</h2>

https://user-images.githubusercontent.com/120864279/212370084-3b95072e-109e-430a-8b53-567cf7a56d40.mp4



I'm going into the control panel to enable Internet Informations Systems with CGI, therefore; I'll be able to deploy the osTicket on the web server. I go to the control panel -> programs -> turn windows features off -> IIS -> World Wide Web Services -> Application Development Features -> CGI 

<p>

 <img width="1440" alt="Install PHP manager pt 0 5" src="https://user-images.githubusercontent.com/120864279/210012275-f718b78e-23e5-4722-a01f-caadf9d3cb4f.png">

Downloading and installing PHP Manager 1.5.0. for IIS 10

</p> 


https://user-images.githubusercontent.com/120864279/212438466-1ab3a554-a0ff-4871-8d9b-ed090785c5e0.mp4

Downloading and Installing the Rewrite Module.
<p>


![Screen Shot 2023-01-13 at 5 54 12 PM (2)](https://user-images.githubusercontent.com/120864279/212481994-0de68ef5-5082-4a69-9491-f79bf7d883c3.png)

 Creating a folder to store my PHP files. I made this folder in C:\PHP

<p>

 https://user-images.githubusercontent.com/120864279/212490382-2abde39b-94c2-4381-81d2-23a9af75ae25.mp4
 
 I downloaded PHP 7.3.8 zip file and extracted all the files in the folder to C:\PHP
 
 
<p>
  
 <img width="1440" alt="Screen Shot 2023-01-04 at 2 16 28 PM" src="https://user-images.githubusercontent.com/120864279/210641987-a57ba4ad-ac72-4444-83e3-f32b8726d848.png">

Downloading the Microsoft Visual C++ redistributable package.
 
<p>
 
https://user-images.githubusercontent.com/120864279/212492659-352e3ded-f1f0-4e39-8d70-ff1db3d3d808.mp4
 
Downloading and Installing the MySQL 5.5.62. After I download the file I open it and start the setup. I do typical setup -> Launch Configuration Wizard -> Standard Configuration -> then enter Password1 as the password.
   
<p>




<p>
  
<img width="1440" alt="Copy upload file into Inetpub pt 3" src="https://user-images.githubusercontent.com/120864279/209999150-23d8b40b-d91b-4f6b-9521-0099157bc508.png">
  
  
Downloading osTicket-v1.15.8, followed by extracting and copying the upload folder to the c:\inetpub\wwwroot folder. 


<img width="1440" alt="Rename upload folder to osTicket pt 4" src="https://user-images.githubusercontent.com/120864279/210003287-8e51e69f-c2ee-4de0-aa90-a51924e41885.png">
  
  
Change the name of the "upload" folder to "osTicket" when the file is finished copying. 




<p>

<img width="1440" alt="Screen Shot 2022-12-29 at 4 10 12 PM" src="https://user-images.githubusercontent.com/120864279/210015802-1771ea64-86a6-41b9-969a-f29a6e489a1e.png">


  I open Internet Informations Systems (IIS) as adn administrator. and click stop then start on the right side of the panel. Once machine starts I click the dropdown arrow next the the name under connections, sites, Default Web Site, and the osTicket. After clicking osTicket I click the "Browse*:80 (http)" button on the right side of the page and the browser opens.
  

<p>

<img width="1440" alt="osTicket screen after browse pt 7" src="https://user-images.githubusercontent.com/120864279/210003667-eff3daf4-16a6-4a2a-9655-6764b6f760db.png">
  
  Screen after clicking "Browse*:80" on the Internet Informations Systems page. 

<p>
  
<img width="1440" alt="PHP Manager ph 17" src="https://user-images.githubusercontent.com/120864279/210015329-58704545-0644-4464-95b8-a4277e10c505.png">

 Open IIS and click on PHP Manager under the IIS group in the menu 

<p>
  
  
 <p>
  
<img width="1440" alt="Enable extentions PHP manager pt 8" src="https://user-images.githubusercontent.com/120864279/210016510-fa000b16-ffb4-45da-a68e-6fa02878c55a.png">

  
  Enabling extentions that are needed to improve localization. Enable the php_intl.dl and php_opache.dll extensions.
<p>

  ![Screen Shot 2023-01-06 at 1 06 38 PM (2)](https://user-images.githubusercontent.com/120864279/211082386-65901eee-efa9-4bb0-8c8f-351409085130.png)

Enabling the php_opache.dll extension

<p>

![Screen Shot 2023-01-06 at 1 07 15 PM (2)](https://user-images.githubusercontent.com/120864279/211082514-2cedadfe-9eef-4446-b006-526dc31519ed.png)

Enabling the php_intl.dll extension 

<p>
  
<img width="1440" alt="After refresh os pt 9" src="https://user-images.githubusercontent.com/120864279/210158218-60f7c1e3-d60d-40a2-9265-aa71718283c0.png">
Screen after enabling extensions. Notice the Intl extension now has a check mark.

<p>

<img width="1440" alt="Rename ost pt 10" src="https://user-images.githubusercontent.com/120864279/210005917-da53e064-9560-4083-be0d-36dde561e6b0.png">
 Rename the C:\inetpub\wwwroots\osTicket\include\ost-sampleconfig.php 
  to C:\inetpub\wwwroots\osTicket\include\ost-config.php 
<p>


<img width="1440" alt="Disable inheritance pt 11" src="https://user-images.githubusercontent.com/120864279/210005943-88302711-3a12-4df8-8765-87dc3922d1af.png">
Right-click the ost-config folder then click properties - security - users - edit - users -  full control - apply - okay
<p>


<p>

<img width="1440" alt="osTicket Basic installation pt 13" src="https://user-images.githubusercontent.com/120864279/210006076-ac0839b7-5790-4889-9df3-18fe8b19bceb.png">
After assigning permissions, I hit continue on the osTicket installer and it takes me to this screen. Here I fill out everything under the System settings and Admin User section. 
<p>

<img width="1440" alt="Install Heidi pt 14" src="https://user-images.githubusercontent.com/120864279/210006102-24ca8d18-4436-4077-8137-15a946f016ba.png">
After filling out the info install Heidi to create the database to use for osTicket.

<p>
  

![Start new](https://user-images.githubusercontent.com/120864279/211086059-e7b8a9f3-0d7b-4356-a0ad-4c4505cd3c87.png)

 Open Heidi and click new.

<p>

![SQL PW](https://user-images.githubusercontent.com/120864279/211085463-da1d07c2-bbc8-417b-94e3-dddd9ecc97b2.png)

The username and password that was entered when downloading MySql 5.5 is used here. The username should already be input.

 <p>
   
  ![Screen Shot 2023-01-06 at 1 40 56 PM (2)](https://user-images.githubusercontent.com/120864279/211087582-05b14bab-b50e-471b-a9fd-78c25a6231da.png)
   
   
 When I get to this screen I have to create a database for osTicket. I right-click the field under unnamed and go to create new, followed by database
   
 <p>

   
 ![Screen Shot 2023-01-06 at 1 54 35 PM (2)](https://user-images.githubusercontent.com/120864279/211089576-de7fecb4-c0d5-4b19-96b3-28d7e49fae6f.png)

Name the database osTicket. 

 <p>
   
 ![Screen Shot 2023-01-06 at 2 01 48 PM (2)](https://user-images.githubusercontent.com/120864279/211090849-1299010b-3421-4f45-97a6-7945b5f46152.png)

Return back to the osTicket installer fill out the info under the database settings. Since you named the database osTicket make sure you enter osTicket under MySQL Database. Enter the MySQL Username and MySQL Password to then click install.
   
<p>

  ![Screen Shot 2023-01-06 at 2 25 24 PM (2)](https://user-images.githubusercontent.com/120864279/211093859-e42abe57-2f33-4b03-b7df-9bf57541eeb4.png)
     
     
 If everything has installed correctly you will see this screen. Congratulations you have successfully installed osTicket.
