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

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>


- Enable ISS
- Download Needed Resources
- Enable Extensions
- PHP Manager
- Heidi SQL

<h2>Installation Steps</h2> 

<h3><b>Enabling</b> ISS</h3>
<p>
<img src="osTicket-Enable ISS 1.PNG" height="80%" width="80%" alt="Enabling ISS"/>
</p>
<p>
Picture 1 - Enabling Application Development Features and common HTTP Features.
</p>  
  <img src="osTicket-Enable ISS 2.PNG" height="80%" width="80%" alt="Enabling ISS"/>
  <p>
Picture 2 - Enabling CGI. Enabling CGI is important because it allows for PHP to be exexuted on the web server.
</p>

  <img src="osTicket-ISS Confirm Enable.PNG" height="80%" width="80%" alt="Confirming ISS"/>
</p>
<p>
Picture 3 - Using the port 127.0.0.1, you can test to see if ISS was enabled succesfully. 
</p>

<h3><b>Installing and Registering PHP</b></h3>

<p>
<img src= "osTicket-Installing PHP.PNG" height="80%" width="80%" alt="Installing PHP"/>
</p>
<p>
  Picture - 1 After downloading PHP Manager, create a folder named "PHP" in your C: Drive. Then unzip the contents from the PHP manager download file to the file you created in your C: Drive.
</p> 

</p>
<p>
  <img src="osTicket-PHP Setup.PNG" height="80%" width="80%" alt="PHP-Register"/>
</p>
<p>
  Picture 2 - Open "ISS" as and administrator and regiester PHP. After registering, reload ISS.
</p>
<h3>Installing osTicket</h3>
<p>
  <img src="osTicket-Installing osTicket.PNG" height="80%" width="80%" alt="Installing-osTicket"/>
</p>
<p>
 Picture 4 - After installing osTicket, extract and copy the "upload" folder into the path "c:\inetpub\wwwroot", then rename the "upload" file to "osTicket". Rename it exactly as this will be important.
</p>
<p>
  <img src="osTicket-Enable extentions.PNG" height="80%" width="80%" alt="Navigate *.80"/>
</p>
<p>
  Picture 5 - Open ISS and navigate the path "sites->Default->osTicket" and click "PHP Manager". Then navigate to "Enable or disable an extention" under the PHP extentions tab. This can bee seen on <b>Picture 3.</b> You can also select "Browse *.80" to open up the local host for osTicket at this time. After enabling the extentions in the next step you can visually see the changes. 
</p>
<p>
  <img src="TS-enabl-extentions.PNG" height="80%" width="80%" alt="Enabling PHP Extentions"/>
</p>
<p>
  Picture 6 - Once you have reached this page, you need to enable the following: php_imap.dll, php_intl.dll, php_opcache.dll. They are also shown in the picture above.
</p>
<p>
  <img src="osTicket-file-name-change.PNG" height="80%" width="80%" alt="ost-name-change"/>
</p>
<p>
 Picture 7 - Navigate to C:\inetpub\wwwroot\osTicket\include, once you are there, find a file named "ost-sample-config", rename that file to "ost-config". This is importnant because this is the file osTicket uses to operate off of.
</p>
<br />
<p>
<img src="osTicket-ost-config-permission 1.PNG" height="80%" width="80%" alt="permissions 1"/>
<img src="osTicket-ost-config-permission 2.PNG" height="80%" width="80%" alt="permissons 2"/>
</p>
<p>
  Picture 8&9 - Navigate to C:\inetpub\wwwroot\osTicket\include\ost-congfig. Once you are there right-click the file and navigate to properties then security. Once your are there you are going to remove all permissions assigned. Then add a role for everyone, and give the role full access.
<p>
<b>Now that your permissions are good go back to where you found *.80. Then click the continue button.</b>
</p>  
  <p>
  <img src= "osTicket-Creating Database for osticket.PNG" height="80%" width="80%" alt="HeidiSQL Database Creation"/>
</p> 
<h3><b>Installing and setting up HeidiSQL</b></h3>
<p>
  Picture - 1 After installing HeidiSQL, register a new database and name it "osTicket". This will be used when installing osTicket.
</p>
<p>
  <img src= "osTicket-Database view from osTicket.PNG" height="80%" width="80%" alt="HeidiSQL Database Creation"/>
</p>
<p>
  Picture 2 - After you created a data base in HeidiSQL, fill out the information shown in the picture. Then press install.
</p>
<p>
  <img src= "TS-Installed.PNG" height="80%" width="80%" alt="osTicket Installed"/>
</p>



<br />
