<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br /

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Install Azure's cloud computing system and create a VM under a "resource group"
- Log into RDP (Remote Desktop Protocol) with the copied public IP Address of the VM
- Install files from the "OS Ticket Documentation" Application and extract to a PHP folder inside the Windows (C:) Drive.
- Install Internet Information Services (IIS) and CGI, install the correct properties
- Launch the osTicket System through IIS

<h2>Installation Steps</h2>

<p>
<img width="1356" height="358" alt="image" src="https://github.com/user-attachments/assets/876fb30e-7ac5-4b7c-973d-367eb8ceb248" />
</p>
<p>
After creating a Virtual Machine, it was set to a resource group folder that holds all data, files, virtual networks, and other services we will create. After creating the Virtual Machine, I went to the main page to search for the newly created VM, copied the public IP Address, opened up the RDP (Remote Desktop Protocol), and pasted the public IP Address of the Virtual Machine, and used the credentials I created to log into the Virtual Machine in the RDP. Installed Wireshark for activity tracking on the NIC (Network Interface Card). Opened web windows inside the Virtual Machine and installed the osTicket Installation Files, extracted all files, and put them in their respective folders. 
</p>
<br />

<p><img width="260" height="180" alt="image" src="https://github.com/user-attachments/assets/0e1ee3b0-9693-4f86-a715-fc6754767c67" />
</p>
<p>I went to the "OS Ticket Documentation" Application and installed the IIS (Internet Information Services) with CGI, and these two will serve up our osTickets, along with PHP Manager for the IIS, and this is needed to run the osTickets, install the "rewrite modules", and after that's installed I created the Directory on my (C:) Drive named "PHP" and from the unzipped files, I extracted the "php 7.3.8" into the "PHP" folder. I then installed the "VC_redist" file, "mysql.5.5.62" with the "Typical Setup". Now, open the IIS Application and register PHP in the IIS Application. It makes the web server aware of the existence of PHP on the computer, and it tells the web server where it is. Once that's done, reload the web server. And now we can finally install the osTicket system. 
</p>
<br />

<p>
<img width="540" height="485" alt="image" src="https://github.com/user-attachments/assets/9899e4d5-c6d2-49d5-a343-247b868e50f8" />

</p>
<p>
Go to the "osTicket 1.15.8" folder and extract all documents inside. It creates two separate folders, so we will copy the "upload" folder into the "inetpub" folder (which is located in the Windows (C:) Drive) and into the folder "wwwroot". I then renamed the "upload" to "osTicket". I reloaded the IIS server, so everything is up to date. Then, I went to "sites," "Default Web Site," "osticket," and double-clicked "PHP Manager," "enable or disable extension," and I enabled the php_imap.dll, php_inti.dll, and php_opcache.dll, and refreshed the browser since those services were disabled. Now, rename "ost-sampleconfig.php" to "ost-config.php" and configure it so that the osticket can make changes in this file on the backend. Disable its permissions from its properties and add new permissions. Click "Browse.80" from the IIS Application to access the ticket launcher. </p>
<br />
