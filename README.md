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

Next create a folder on you C drive and call it PHP , go to file or folder  look to the left where desktop and downloaded is scroll down to the C drive click it then once in the C drive right click and click  new  folder and name it PHP.



<img width="2566" height="1458" alt="image" src="https://github.com/user-attachments/assets/b754b238-a4f2-490f-ab52-21ff5ce46bca" />

Now minimize the folder you have open and open a next folder and go to the osticket unzip files and unzip PHP into the folder you just made. first right click  the PHP zip folder and click extract all now before clicking extract look to the right and click browse now scroll down and look for the C drive and then click PHP then select and now you can go ahead and click extract all.


<img width="2804" height="1774" alt="image" src="https://github.com/user-attachments/assets/8e0e35ba-2bab-4a66-a907-e3c6a2ebe7c5" />

Then go back to the osticket unzipped files and install VC_redist.


<img width="2074" height="1330" alt="image" src="https://github.com/user-attachments/assets/4751e6da-714a-4cc5-9e56-6ada644b962c" />

Next download MYSQL5.5.62 when installing  it use (typical) as your setup click install after it is installed check the box that says launch the MYSQL instance configuration wizard , then click next and check standard configuration then click next until you get to the security option,  the password is  ( root) PLEASE NOTE  : this is just for the lab never do this  for any serious work or personal passwords. after typing root both times click next and then click execute after the file is created click finish.



<img width="2876" height="1800" alt="image" src="https://github.com/user-attachments/assets/167a66c1-8ddd-4c87-b35e-5320e1c41d9e" />

Now it time to register  PHP ,so first go to start menu and type IIS open IIS as a admin you can right click IIS and click run as administrator 
once in IIS  go to PHP manager double check it click regester a new PHP version when the box pops up click browse  (browse would be the 3 dots like this ...) once you click the 3 dots go to the C drive go to the PHP  folder and open it the click PHP.CGI which is the binary execute for PHP so double click it and click ok after that  restart the IIS ( look to the upper right under actions under manage server and you should see restart ,start and stop).



<img width="1824" height="1148" alt="image" src="https://github.com/user-attachments/assets/240c6365-ce8b-4fce-b12f-fda3bba89e32" />
<img width="2542" height="1266" alt="image" src="https://github.com/user-attachments/assets/8394df0e-051f-433e-b497-7d98ab71c261" />

Now go back to the osticket installation folder and upzip/extract osTicket-v1.15.8 ,then open a new folder ( if you don't know how to open a fresh folder just right click the folder at the bottom of the screen and click file explorer ) now go to the C drive then go to inetpub then wwwroot then minimize that folder and in the next folder double click the osticket unzip files and drag the upload folder to the wwwroot. after moving the folder rename the upload folder to (osTicket) make sure its spelt like that , to rename it just right click the upload folder and click rename 


<img width="2352" height="1622" alt="image" src="https://github.com/user-attachments/assets/9270e708-4ac5-4720-bbad-2ee2fb0aae63" />
<img width="2352" height="1622" alt="image" src="https://github.com/user-attachments/assets/e3aafe74-8ae8-4681-b8d1-31965b4a3df7" />

Now go to the start or windows button and search for IIS right click it and click run as administrator once in restart it ,at the top left go to connections under it click the small arrow beside osticket to expand it then do the same for sites then once expanded click osticket look to the right under manage folder you should see ( Browse*80*) click that to open osticket in the browser 



<img width="2288" height="1580" alt="image" src="https://github.com/user-attachments/assets/961a186e-5da5-4a32-abce-a172dc419887" />


When you open osticket installer you can observed that there are a few prerequisites that or not ticked so to enable those extensions go back to IIS go to sites then default site then osticket and double click PHP manager then under PHP Extension go to enabled or disabled an extension and enable (php_imap.dll,php_intl.dll and php_opcache.dll ) you mite have to scroll for a while and to enable them just right click and click eable now if you go back to the osticket installer you should see some of the prerequisites ticked.  



<img width="1178" height="1064" alt="image" src="https://github.com/user-attachments/assets/de28b67c-b790-4358-9c4c-244c314ca88f" />


now go to your folder or reopen a new  folder go to C drive once in C dive go to inetpub then wwwroot then osTicket then include then scroll 
down until you see ost-sampleconfig.php once you have found it right click it and rename it to (ost-config.php) please dont mess the name up not even a letter.



<img width="2812" height="1670" alt="image" src="https://github.com/user-attachments/assets/44043ae8-f86a-4d44-96cf-a7cf026f430e" />


After renaming the file right click the folder and click properties then go to security then go to advanced then disabled inheritance and click remove all inherited permissions from this object then add new permission and then click select  principal then type everyone and click check names then click ok then check the full control box then click apply and ok.  


<img width="1846" height="1376" alt="image" src="https://github.com/user-attachments/assets/e12d1c43-e423-4b53-a4b2-67962be72755" />


Now go to Heidi SQL and create a database to run osticket , first open the folder and go to the osticket installation files once in the file look for heidi SQL and double check it and click next for everything and then install  once installed  check the box that says launch Heidi SQL and click finish.



<img width="1878" height="1180" alt="image" src="https://github.com/user-attachments/assets/4d743628-2a41-42b2-b2d1-993c5262a5db" />


After launching  Heidi SQL look to the botton of the screen and click new ,when it is created look to the right where users and password is and type (root) for both, then click open then once opened look at the top left where unnamed is or the dolphin sign right click that and rename it to (osTicket) make sure its spelt exactly like that then click ok.



<img width="2856" height="1540" alt="image" src="https://github.com/user-attachments/assets/b1fa9eb7-b775-4d74-9ac1-7a78b9b99a38" />


Now go back to browser and setup osticket enter the details for helpdesk URL, admin user and database settings , PLEASE NOTE: for helpdesk and admin user you can make it up just remember your username and password. for the database part the MYSQL database is  (osTicket)  and for the MYSQL username and password its (root) then click install now.



<img width="2864" height="772" alt="image" src="https://github.com/user-attachments/assets/86544518-d69c-47ed-a340-080210d3bc70" />
<img width="2862" height="1014" alt="image" src="https://github.com/user-attachments/assets/001874b9-807b-454c-95df-5521fe499569" />

if everything goes well the lab is now completed feel free to observe both links 
[
](http://localhost/osTicket/scp/login.php)
[
](http://localhost/osTicket/)

one link it use osticket as an admin or agent and the next one is to use osticket as an user feel free to create tickets and solve them as an agent.


[
](http://localhost/osTicket/scp/login.php)

