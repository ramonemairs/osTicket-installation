# osTicket-installation
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket -  Installation</h1>
This tutorial outlines step by step how to install the open-source help desk ticketing system osTicket.



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Setup a virtual machine in Azure
- Install the Remote desktop
- Install the osTicket requirements
- Install osTicket itself
- Do the after-installation configuration of osTicket
- Explore osTicket as a Help Desk professional 

<h2>Installation Steps</h2>


<img width="596" height="1006" alt="image" src="https://github.com/user-attachments/assets/0ca28ff1-8d7e-4584-90d5-435791a53077" />

To start the lab go to azure.microsoft.com (https://azure.microsoft.com/en-gb/get-started/azure-portal) create an accout then go to the search bar and type virtual machines or (VM) and click create new virtual machine , name the the virtual machine osTicket-vm and set the region to east US 2 or east US .


<img width="748" height="1258" alt="image" src="https://github.com/user-attachments/assets/508fd20b-d6d7-42a0-a894-90cbb7e83851" />

 The operating system for the virtual machine is a windows 10 and for the size* it must have 2vcpus and 8GB of RAM anything lower the virtual machine is going to be very slow.


 <img width="752" height="1256" alt="image" src="https://github.com/user-attachments/assets/be487303-63a7-4605-a5a1-36a72982d5b2" />

 Create a user name and password for the virtual machine ,NOTE: before leaving the basic tab check the box under licensing. Then click next and when you get to networking allow it to create its own virtual network then click review and create then create , When it is finally created it should look like the image above.


 <img width="1172" height="720" alt="Screenshot 2026-07-06 at 1 51 50 PM" src="https://github.com/user-attachments/assets/8f182f7c-e39f-4e33-9c02-dfc6f8875ed9" /> 

The next step is to login to virtual machine so first go to the search bar and type VM scroll to the side and look for the public IP address.Now download and open up remote desktop copy the public ip address from the virtual machine go back into remote desktop click the plus button and add new PC then copy the ip .

 

 
