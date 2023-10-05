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

4) Go down to the "Internet Information Services" option and select the checkbox, then press the + to access more options. Make sure the "Web Management Tools", "IIS Management Console" and "World Wide Web       Services" boxes are marked.

     ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/888663a1-aaf6-4845-97fe-5465605a2381)

     ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/249f7d5b-242f-4441-bdf7-76ba03a7b4de)

5) To make sure IIS was setup correctly, go to the Microsoft Edge web browser and connect to "127.0.0.1", you should see the below screen if done successfully.

     ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/e9c30b96-f29a-4dd3-8bca-90949bd281b6)

6) Install PHP Manager for IIS, open the installer from the download link above. Click all the necessary options to proceed with installation and then close the installer once finished.

     ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/8c8fb509-d126-4a38-95a9-92298e5b9aec)

7) Install IIS URL rewrite module, the instlal can also be found in the downloads linked above. Open said installer and click all the necessary options to proceed with the installation, then close the            installer once finished.

     ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/edb6def0-d962-4dae-96b2-88fa289c907e)

8) Creat a new folder in your C: drive named "PHP".

9) Unzip the "php-7.3.8" file from the above download link into this new "PHP" folder in your C: drive.

10) Install Microsoft Visual C++ 2015-2022 Redistributable, the installer can be found in the above download link. Select the necessary options to install then close the installer.

     ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/ad5f33ca-671e-4e5e-9eb1-3a7a3ad717d7)

11) Install MySQL Server, open the installer and select the "Typical" installation option, once installed it will automatically open the configuration wizard, click next. Select the "Standard Configuration"       option and click next, then select the "Install As Windows Service" option, hit next. You will then be prompted to creat a password for the user "root", make sure you remember this for future reference.       Click next, execute, then finish.

     ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/c6955e37-d8fe-4cc5-8fe3-0763861e3a13)

     ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/4a8915d9-9e96-45b4-bba2-e07a0fa3ce4f)

     ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/7af67fec-6c55-4e63-9c12-cbd3edf929b7)

     ![image](https://github.com/jvilleda96/osticket-prereqs/assets/147073936/28daed00-8cb2-4695-a2f8-45b79142d876)

12) 



