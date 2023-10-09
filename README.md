<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
In this tutorial I will guide you through the installation of osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (22H2)

<h2>List of Prerequisites</h2>

  - Microsoft Azure Subscription
  - Internet Information Services (IIS)
  - PHP Manager
  - Rewrite Module
  - VC Redist
  - MySQL
  - Heidi SQL
  - osTicket v1.15.8
  - Link to downloads: https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6

<h2>Installation Steps</h2>

1) Setup a virtual machine with Microsoft Azure (portal.azure.com). When setting up make sure you select Windows 10 Pro as your operating system and that you choose a machine with at least 2vcpus and 16gb of     memory. Once setup note the Public IP address in your essentials panel, you'll need this in the next step.

   ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/1a335469-0fcf-43a2-b9f7-9a469036a96e)

2) Use the "Remote Desktop Connection" application to connect to your newly created virtual machine. It will ask you for an IP address, use the previously saved address to connect, you will then be prompted      to login using the username and password you created for the virtual machine.

   ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/aef22eaf-6294-4965-b4dd-725116742408)

3) Once logged in to your virtual machine we have to enable internet information services (IIS) along with CGI & common HTTP features. To do this open up your control panel and click on "Programs", then click    "Turn Windows features on or off".

    ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/5d07dc97-9985-4a98-b8a5-47f3c1adc613) 

    ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/eb09f916-ee3e-4e94-b76e-e51d75050c66)

4) Go down to the "Internet Information Services" option and select the checkbox, then press the + to access more options. Make sure the highlighted boxes are checked, then hit ok.

     ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/888663a1-aaf6-4845-97fe-5465605a2381)

     ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/4bc20d7b-7979-4ade-9153-7093be755e7c)
     
5) To make sure IIS was setup correctly, go to the Microsoft Edge web browser and connect to "127.0.0.1", you should see the below screen if done successfully.

     ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/e9c30b96-f29a-4dd3-8bca-90949bd281b6)

6) Install PHP Manager for IIS, open the installer from the download link above. Click all the necessary options to proceed with installation and then close the installer once finished.

     ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/8c8fb509-d126-4a38-95a9-92298e5b9aec)

7) Install IIS URL rewrite module, the installer can also be found in the downloads linked above. Open said installer and click all the necessary options to proceed with the installation, then close the            installer once finished.

     ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/edb6def0-d962-4dae-96b2-88fa289c907e)

8) Creat a new folder in your C: drive named "PHP".

9) Unzip the "php-7.3.8" file from the above download link into this new "PHP" folder in your C: drive.

10) Install Microsoft Visual C++ 2015-2022 Redistributable, the installer can be found in the above download link. Select the necessary options to install then close the installer.

     ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/ad5f33ca-671e-4e5e-9eb1-3a7a3ad717d7)

11) Install MySQL Server, open the installer and select the "Typical" installation option, once installed it will automatically open the configuration wizard, click next. 

     ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/c6955e37-d8fe-4cc5-8fe3-0763861e3a13)

     Select the "Standard Configuration" option and click next.

     ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/4a8915d9-9e96-45b4-bba2-e07a0fa3ce4f)

     Select the "Install As Windows Service" option, hit next.  

     ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/7af67fec-6c55-4e63-9c12-cbd3edf929b7)

     You will then be prompted to creat a password for the user "root", make sure you remember this for future reference. Click next, execute, then finish.

     ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/28daed00-8cb2-4695-a2f8-45b79142d876)

12) Open internet information services manager as an administrator, then click the "PHP Manager" option.

     ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/c134f557-eb3c-4a54-a05a-e40ee165a95c)

     Select the "Register new PHP version" option.

     ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/9f091e9f-cd64-42c3-969c-be49fc042761)

     Select the "php-cgi.exe" file located in the PHP folder on your C: drive.

     ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/90937c98-043f-470b-9f2b-59d3ddddfe14)

     Refresh the server.

13) Extract the "upload" folder in your osticket zip file to the "wwwroot" subfolder in your "inetpub" folder in your C: drive.

     ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/f47b6f95-6926-469e-83d3-d9462993c852)

     Rename the "upload" folder to "osTicket".

14) Go back to IIS manager and locate the PHP manager for osTicket.

     ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/4eb90940-eb38-4a00-a7a6-eb500dc531a8)

     Scroll down to "Enable or disable an extension".

     ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/460b3821-d51d-481c-9159-21167e686907)

     Enable the following:php_imap.dll, php_intl.dll and php_opcache.dll.

     ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/6f5c0117-78ad-4e40-9053-00d56e0456f4)

     Refresh your osTicket folder and click the Browse*.80 link.

     ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/95bfabd9-9816-4d27-9750-3adcebd5e5df)

     If done correctly, you should have a similar screen to the one below:

    ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/d333a307-d646-4c24-b13a-2b6bca4b638f)


15) Go back to the osTicket folder in your C: drive and open the include subfolder to locate the "ost-sampleconfig.php" file, rename this to "ost-config.php".

    ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/06cd5d9b-1a86-4fb4-97e1-bece2500c665)

    Go to the "Security" tab and press advanced to change permissions.

    ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/01227ef9-2c31-419a-8e8a-90a01d92f64f)

    Select "Disable inheritance" and the second option to clear all permissions.

    ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/2c1ca399-ae74-4b5b-aa68-291aac7212d0)

    Add a new permission for everyone with full control

    ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/159678a8-8a10-4c37-981e-ac81734d7c5d)

    Hit apply, then ok.

16) Time to install HeidiSQL, open the installer and select the necessary options to continue.

    ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/c006df8a-720e-4026-9271-b986f73d3d3c)

    Now select "Launch HeidiSQL" and hit finish.

    ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/6432bed1-6897-4459-947d-de13d541b87b)

    create a new session in the bottom left.

    ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/9dc568c0-9a28-4033-ba2b-d7636898fb7b)

    Enter our previously created "root" login info and hit open.

    ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/829ad05f-7c5f-462a-b21e-33d0bfa7b5e8)

    Right click "Unamed" and select create new database, name it "osTicket".

    ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/9fd9947d-3998-4ec1-bd36-106697eb82e4)

17) Go back to Microsoft Edge and continue setting up osTicket, fill out the information however you wish, just make sure you save usernames and passwords. For database setting you will have to use the           database we created in HeidiSQL and the "root" username and password.

    ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/cc821421-b4b4-455b-bc39-bd3406744139)

    If successful, you will get this screen.

    ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/230962c0-5d41-4034-b4b9-cc6dbd71c731)

18) Go to http://localhost/osTicket/scp/login.php to test the login, if successful you should see this screen.

    ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/e99ef037-2a75-405f-aa2b-cfc09833f928)


osTicket is now successfully installed into your virtual machine!

