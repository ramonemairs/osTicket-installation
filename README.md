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


To start the lab go to azure.microsoft.com (https://azure.microsoft.com/en-gb/get-started/azure-portal) create an accout then go to the search bar and type virtual machines or (VM) and click create new virtual machine , name the virtual machine osTicket-vm and set the region to east US 2 or east US .


<img width="748" height="1258" alt="image" src="https://github.com/user-attachments/assets/508fd20b-d6d7-42a0-a894-90cbb7e83851" />



 The operating system for the virtual machine is a windows 10 and for the size* it must have 2vcpus and 8GB of RAM anything lower the virtual machine is going to be very slow.


 <img width="752" height="1256" alt="image" src="https://github.com/user-attachments/assets/be487303-63a7-4605-a5a1-36a72982d5b2" />

 

 Create a user name and password for the virtual machine ,NOTE: before leaving the basic tab check the box under licensing. Then click next and when you get to networking allow it to create its own virtual network then click review and create then create , When it is finally created it should look like the image above.


 <img width="1172" height="720" alt="Screenshot 2026-07-06 at 1 51 50 PM" src="https://github.com/user-attachments/assets/8f182f7c-e39f-4e33-9c02-dfc6f8875ed9" /> 

 

The next step is to login to virtual machine so first go to the search bar and type VM scroll to the side and look for the public IP address, Now download and open up remote desktop copy the public ip address from the virtual machine go back into remote desktop click the plus button and add new PC then copy the ip address, then type in the username and password you used to create the virtual machine in azure then hit enter to login.


<img width="2284" height="1244" alt="image" src="https://github.com/user-attachments/assets/45ac7d73-736b-477a-bec3-1901aa317c1c" />



After connecting to the virtual machine in remote desktop go to Microsoft edge and download osTicket installation files ( [
](https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD)](https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD) then go into files or folder find the osTicket files and unzip the files, you do that by right clicking the mouse and press extract all.


<img width="2302" height="1214" alt="image" src="https://github.com/user-attachments/assets/ffc0d9f4-e85e-4e1b-a6ca-e1805d8a9aca" />



after downloading and unzipping the file its time to enable IIS internet Information Services , so first click the start menu and type control panel open it and go to programs ( click uninstall programs ) then click ( turn windows features on or off ) then scroll to internet Information Services (IIS) ,  check the box then expand it go to ( world wide web services) expand that and go to application development features expand that aswell and then search for CGI and check that box then close it. 


 <img width="2272" height="1210" alt="image" src="https://github.com/user-attachments/assets/59332012-6579-45c8-b0ea-4fcfdee5fae8" />
 


 Now it time to install  PHP manager first go to the folders then go to the osTicket installation folder that is unzipped , go to PHP manager and install it.

 
<img width="2288" height="1314" alt="image" src="https://github.com/user-attachments/assets/f3e2eb26-78ba-439b-80f8-1229f1f63ef9" />

after installing PHP install rewrite module.


<img width="2342" height="1234" alt="image" src="https://github.com/user-attachments/assets/9e52502e-985f-482a-8e4f-3141c35c2718" />

Next create a folder on you C drive and call it PHP , go to file or folder  look to the left where desktop and downloaded is scroll down to the C drive click it then once in the C drive right click scroll down to new click the folder and name it PHP.



<img width="2566" height="1458" alt="image" src="https://github.com/user-attachments/assets/b754b238-a4f2-490f-ab52-21ff5ce46bca" />

Now minimize the folder you have open and open a next folder and go to the osticket unzip files and unzip PHP into the folder you just made. first right click  the PHP zip folder and click extract all now before clicking extract look to the right and click browse now scroll down and look for the C drive and then click PHP then select and now you can go ahead and click extract all.


<img width="2804" height="1774" alt="image" src="https://github.com/user-attachments/assets/8e0e35ba-2bab-4a66-a907-e3c6a2ebe7c5" />

Then go back to the osticket unzipped files and install VC_redist.


<img width="2074" height="1330" alt="image" src="https://github.com/user-attachments/assets/4751e6da-714a-4cc5-9e56-6ada644b962c" />

Next download MYSQL5.5.62 when installing  it use (typical) as your setup click install after it is installed check the box that says launch the MYSQL instance configuration wizard , then click next and check standard configuration then click next until you get to the security option,  the password is  ( root) PLEASE NOTE  : this is just for the lab never do this  for any serious work or personal passwords. after typing root both times click next and then click execute after the file is created click finish.



<img width="2876" height="1800" alt="image" src="https://github.com/user-attachments/assets/167a66c1-8ddd-4c87-b35e-5320e1c41d9e" />

Now it time to register  PHP ,so first go to start menu and type IIS open IIS as a admin you can right click IIS and click run as administrator 
once in IIS  go to PHP manager double check it click regester a new PHP version when the box pops up click browse  (browse would be the 3 dots like this ...) once you click the 3 dots go to the C drive go to the PHP  folder and open it the click PHP.CGI which is the binary execute for PHP so double click it and click ok after restart the IIS ( look to the upper right under actions under manage server and you should see restart ,start and stop)



