<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com/watch?v=fWX1Lj-rOa0)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Installation Files 
https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6
<h2>Installation Steps</h2>

- Create Virtual Machine in Azure
- Install/Enable IIS in Windows With CGI
- Download and install PHP Manager for IIS
- Download and install the Rewrite Module
- Create the directory C:\PHP
- Download PHP 7.3.8
- Download and install VC_redist.x86.exe.
- Download and install MySQL 5.5.62

<h2>Installation Steps</h2>
<p>
<img src="https://i.imgur.com/gw1eh6W.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
First step is creating our Windows 10 virtual Machine(VM) on Azure. This can be done on Azure by opening Virtual Machines->Create->Windows 10 with 2-4 Virtual CPUs /create username and password->Review->Create. 
</p>
<br />

<p>
<img src="https://i.imgur.com/lKFGfUb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open Remote Desktop Connection then connect to your virtual machine by typing the VM's ip address into Remote Desktop Connection. Use the credentials you created for the virtual machine to login.
</p>
<br />

<p>
<img src="https://i.imgur.com/NY8HmDl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In the VM, right-click the windows menu->Run->Control->
</p>
<br />

<p>
<img src="https://i.imgur.com/voWlYYp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Programs->
</p>
<br />

<p>
<img src="https://i.imgur.com/7ZnhzzF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Turn Windows features on or off-> Internet Information Services->World Wide Web->Application Development features->CGI
</p>
<br />

<p>
<img src="https://i.imgur.com/7Iqm9Uy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Activating CGI allows us to host a webpage on our own network. Test this by typing 127.0.0.1 into google.com in your VM. The webpage that loads up should look like the screenshot above.
</p>
<br />

<p>
<img src="https://i.imgur.com/L1SM68G.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, download/install PHP Manager & Rewrite Module  Here is the [link](https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6)
</p>
<br />

<p>
<img src="https://i.imgur.com/fdZPh2o.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/4aaIh6P.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create a folder on the C drive and name it PHP. Then dowload and extract PHP 7.3.8 and unzip the contents into the PHP folder we just created [here](https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6).
</p>
<br />

<p>
<img src="https://i.imgur.com/Cojbwm8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
                            
  Download and install VC redist.x86.exe
<img src="https://i.imgur.com/cWDdaTP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 Download and install My SQL 5.5.62 Typical->
 Setup Launch Configuration Wizard (after install) -> Standard Configuration -> Password1
  
<img src="https://i.imgur.com/3DPgXGH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>.
<img src="https://i.imgur.com/UKU95B5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/twqaevN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open IIS as admin. Open PHP Manager->Register new PHP ENTER: C:->PHP->php-cgi.exe. Now restart the server. 
</p>
<br />

<p>
<img src="https://i.imgur.com/gDHbkt7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download/install osTicket using this [link](https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6). Open osticket->upload. Extract the upload file into C:->Inetpub->wwwroot. Now rename the "upload" folder to "osTicket". Now, return to ISS and restart the server. 
</p>
<br />

<p>
<img src="https://i.imgur.com/VPQS3V4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In IIS->sites->default Web Services->osTicket->*80 to open osTicket in your internet browser.
</p>
<br />

<p>
<img src="https://i.imgur.com/1edLrbk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/rSdryq4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now we need to enable some extensions so that our osTicket can operate. In ISS open sites->osTicket->PHP Manager->Enable or disable extensions, enable extensions: ph.pop.cash.dll, phpImap.dll, phpintl.dll. Refresh the osTicket tab in your internet explorer. 
</p>
<br />

<p>
<img src="https://i.imgur.com/KpoAt9i.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next rename the file "Ostsampleconfig" to "Ostconfig". This file can be found in Browse->wwwroot->include->Ostsampleconfig.
</p>
<br />

<p>
<img src="https://i.imgur.com/ceHaTx7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now, right-click "ostconfig"->open properties->security->advanced->disable inheritance->remove all permissions. Then select "EVERYONE" and apply.
</p>
<br />

<p>
<img src="https://i.imgur.com/qInGkfb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download/install heidi from this [link](https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6). Next right-click->create new->database->and name it osTicket.
</p>
<br />

<p>
<img src="https://i.imgur.com/t8X3F9s.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open osTicket in your internet browser and fill out the installation details and install.
</p>
<br />

<p>
<img src="https://i.imgur.com/hDFRuXm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next delete the folder named "setup" this folder is in osTicket->Setup. 
</p>
<br />

<p>
<img src="https://i.imgur.com/zb2lSeh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, right-click "ostconfig"->properties->security->advanced->disable inheritance->modify->read only. Then select "EVERYONE" and apply. 
</p>
<br />

<p>
<img src="https://i.imgur.com/lfVp5fP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next open this link http://localhost/osTicket/scp/login.php and log in to osTicket with the credentials you created when filling out the osTicket installation page.
</p>
<br />
Congrulations!!! You have now installed osTicket on your VM.
