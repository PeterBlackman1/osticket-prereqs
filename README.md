
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

https://user-images.githubusercontent.com/120864279/210416032-df9ac818-54f2-4c18-928f-b7a05b2332be.mp4



I'm going into the control panel to enable Internet Informations Systems so I'll be able to deploy the osTicket on the web server.

<p>

  

https://user-images.githubusercontent.com/120864279/210423971-4d648d8b-27c9-4dc5-9f83-b84f5c291941.mov

  
  
Downloading the Web Platform Installer and open to install key components needed to run osTicket.

<p>

<img width="1440" alt="Install PHP manager pt 0 5" src="https://user-images.githubusercontent.com/120864279/210012275-f718b78e-23e5-4722-a01f-caadf9d3cb4f.png">

Downloading and installing PHP Manager 
</p>

<img width="1440" alt="My SQL" src="https://user-images.githubusercontent.com/120864279/209996803-e5cf47c6-2212-47f1-a6b7-65e395ccca21.png">


Adding MySQL and all simple versions of x86 PHP up until 7.3. Then I'll click install and if there's any failures I go back and fix them by downloading the proper files. After I'm done I'll add the Microsoft Visual C++ redistributable package.


<p>


  
<img width="1440" alt="Copy upload file into Inetpub pt 3" src="https://user-images.githubusercontent.com/120864279/209999150-23d8b40b-d91b-4f6b-9521-0099157bc508.png">
  
  
Downloading osTicket, followed by extracting and copying the upload folder to the root folder. 


<img width="1440" alt="Rename upload folder to osTicket pt 4" src="https://user-images.githubusercontent.com/120864279/210003287-8e51e69f-c2ee-4de0-aa90-a51924e41885.png">
  
  
Change the name of the upload folder to osTicket when the file is finished copying. 




<p>

<img width="1440" alt="Screen Shot 2022-12-29 at 4 10 12 PM" src="https://user-images.githubusercontent.com/120864279/210015802-1771ea64-86a6-41b9-969a-f29a6e489a1e.png">


  I open Internet Informations Systems and click stop then start on the right side of the panel. Once machine starts I click the dropdown arrow next the the name under connections, sites, Default Web Site, and the osTicket. After clicking osTicket I click the "Browse*:80 (http)" button on the right side of the page and the browser opens.
  

<p>

<img width="1440" alt="osTicket screen after browse pt 7" src="https://user-images.githubusercontent.com/120864279/210003667-eff3daf4-16a6-4a2a-9655-6764b6f760db.png">
  
  Screen after clicking "Browse*:80" on the Internet Informations Systems page. 

<p>
  
<img width="1440" alt="PHP Manager ph 17" src="https://user-images.githubusercontent.com/120864279/210015329-58704545-0644-4464-95b8-a4277e10c505.png">

 Open IIS and click on PHP Manager under the IIS group in the menu 
<p>
  
<img width="1440" alt="Enable extentions PHP manager pt 8" src="https://user-images.githubusercontent.com/120864279/210016510-fa000b16-ffb4-45da-a68e-6fa02878c55a.png">

  
  Enabling extentions that are needed to improve localization. Enable the php_imap.dll, php_intl.dll, php_opache.dll extensions.
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
  
 https://user-images.githubusercontent.com/120864279/210255560-e50bc4c4-f6e3-4b31-a024-9008c35245de.mp4
