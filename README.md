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

- Deploy Microsoft Azure’s cloud computing platform and create a Virtual Machine (VM) within a designated resource group.

- Connect to the VM using Remote Desktop Protocol (RDP) with the assigned public IP address.

- Download the required installation files from the osTicket documentation and extract them into a dedicated PHP folder within the local C:\ drive.

- Install Internet Information Services (IIS) and CGI modules, ensuring that all necessary features and configurations are properly enabled.

- Open the osTicket system through IIS and proceed with the initial setup and configuration.

<h2>Installation Steps</h2>

<p>
<img width="1356" height="358" alt="image" src="https://github.com/user-attachments/assets/876fb30e-7ac5-4b7c-973d-367eb8ceb248" />
</p>
<p>
After creating a Windows-based Virtual Machine (VM) in Microsoft Azure, I assigned it to a designated resource group to organize all related data, files, virtual networks, and services. Once the VM was deployed, I accessed it by locating its public IP address in the Azure portal and connecting through Remote Desktop Protocol (RDP) using the administrator credentials I configured during setup. Within the virtual environment, I opened a web browser to download the osTicket installation files, extracted the contents, and organized them into their appropriate directories to prepare for system deployment. This process demonstrated practical experience with Azure cloud management, remote access configuration, and web-based application setup in a virtualized environment.</p>
<br />

<p><img width="260" height="180" alt="image" src="https://github.com/user-attachments/assets/0e1ee3b0-9693-4f86-a715-fc6754767c67" />
</p>
<p>I went to the "OS Ticket Documentation" Application and installed the IIS (Internet Information Services) with CGI, and these two will host the osTickets, along with PHP Manager and the "rewrite modules" for compatibility with the IIS. I created the Directory on my Windows (C:) Drive named "PHP" and from the unzipped files, extracted the "php 7.3.8" into the "PHP" folder. I then installed the "VC_redist" file, "mysql.5.5.62" with the Typical Setup configuration. I registered PHP within IIS Manager to ensure the web server could locate and process PHP files. With all components integrated and IIS reloaded, I successfully launched the osTicket system, completing the web-based help desk deployment within the Azure environment.
</p>
<br />

<p>
<img width="540" height="485" alt="image" src="https://github.com/user-attachments/assets/9899e4d5-c6d2-49d5-a343-247b868e50f8" />

</p>
<p>
After extracting the osTicket 1.15.8 installation files, I copied the “upload” folder into the C:\inetpub\wwwroot directory and renamed it “osTicket.” Once the files were in place, I reloaded the IIS server to apply the latest changes and navigated to Sites → Default Web Site → osTicket to manage the application settings. Through PHP Manager, I enabled key PHP extensions — php_imap.dll, php_intl.dll, and php_opcache.dll — to ensure full application functionality. I then renamed ost-sampleconfig.php to ost-config.php, adjusted file permissions to allow backend configuration, and updated access controls to secure the file. Finally, I launched the osTicket setup through IIS (Browse:80) to verify that the system was properly configured and operational.<br />
