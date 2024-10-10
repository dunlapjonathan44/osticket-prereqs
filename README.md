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

- PHP Manager for IIS-PHP Manager for IIS configures PHP to run smoothly on an IIS server, making it easier to manage PHP settings and extensions, ensuring fast and reliable performance for web applications.
- URL Rewrite Module-The URL Rewrite Module in IIS allows clean URLs and redirects, making URLs more user-friendly and better for SEO. It also helps control how requests are routed in the application for security and efficiency.
  
- Microsoft Visual C++ Redistributable (VC_redist.x86)-The VC_redist.x86 provides necessary Visual C++ libraries for running apps like osTicket. It’s critical for ensuring smooth application performance on Windows systems by preventing errors from missing dependencies.
- MySQL Database-MySQL is a powerful database system used to store and manage data. It's known for being reliable and scalable, making it ideal for handling large volumes of data and running complex queries.
- HeidiSQL-HeidiSQL is a user-friendly interface for managing MySQL databases. It simplifies tasks like running queries, exporting data, and managing users, making database administration more efficient.


<h2>Installation Steps</h2>


<p>

</p>
<p>
In the screenshot, I created a virtual machine in Azure, naming it "os-ticket-vm," using the East US region, with Windows 10 Pro (22H2) and 2 vCPUs. Then I chose a username and password and clicked Review and Create. After it passed validation I clicked create and went to the next step.
</p>
<br />

<p>
<img src="https://i.imgur.com/HRwXn0l.png)" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

  After setting up the Windows 10 VM in Azure, log in using your credentials. It’s recommended to create a Notepad file and save a copy of all credentials, as there will be several. Inside the VM, open Microsoft Edge and download the osTicket-Installation-Files.zip. Extract the files, and you should see the following.
  
 <img src="https://i.imgur.com/L2KjS5v.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
 
  Next, we need to enable Internet Information Services (IIS). Start by searching for "Control Panel" in the search bar at the bottom of the screen. Click on Uninstall a Program, then select Turn Windows features on or off. In the window that appears, check the box for Internet Information Services (IIS). Additionally, under World Wide Web Services -> Application Development Features, make sure to enable CGI.

  <img src="https://i.imgur.com/7fg6q8S.png IIS" height="80%" width="80%" alt="Disk Sanitization Steps"/>

  
   <img src="https://i.imgur.com/QCCascY.png Enable CGI" height="80%" width="80%" alt="Disk Sanitization Steps"/>
   
   After completing the previous steps, proceed with installing the PHP Manager for IIS. Open the installation file and accept all the default settings by clicking OK. Repeat the process for the rewrite module by running the rewrite_amd64 file, again accepting the default options.
   
  <img src="https://i.imgur.com/L2KjS5v.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  
  
   <img src="https://i.imgur.com/xT8w8JQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

  Next, install the Microsoft Visual C++ Redistributable, accepting all default settings. Then proceed to install MySQL, choosing the **Standard Configuration** option. For simplicity in this lab, set both the username and password to "root". In a real-world scenario, you would use a stronger, more secure password.

 
 <img src="https://i.imgur.com/qq3YMw9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 

Now, open Internet Information Services (IIS) by typing "IIS" in the search bar, then selecting Run as administrator. In IIS, click on PHP Manager, then choose Register new PHP version. Browse to C:\PHP\php-cgi.exe and select it to complete the registration.

 <img src="https://i.imgur.com/Tym4If9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 

 To reload IIS and apply the new PHP version, click Restart on the right-hand side of the IIS window. This ensures the updated PHP configuration is properly loaded.

 <img src="https://i.imgur.com/O89AQk3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 

 Extract the **osTicket** zip file, then move the extracted **upload** folder to **C:\inetpub\wwwroot**. Once moved, rename the folder to **osTicket** (make sure the name is exact).

 <img src="https://i.imgur.com/vKt3xLp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
 <img src="https://i.imgur.com/X6WXZ2p.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 

 Reload IIS once more. In the left-hand pane, navigate to Sites and click the arrow to expand until you find osTicket. Then, in the right-hand pane, click Browse. You should now see the following.

 


</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</p>
<br />
