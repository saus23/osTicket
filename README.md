<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />
<p> &emsp; </p>


<h2>Video Demonstration</h2>

- ### [YouTube: Windows implementation](https://youtu.be/4BuSPjaT7os)
<p> &emsp; </p>

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
<p> &emsp; </p>

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)
<p> &emsp; </p>

<h2>List of Prerequisites</h2>

- PHP
- mySQL
- HeidiSQL
- C++ redistributable 2015-2022
- IIS URL rewrite module 2
- PHP Manager for IIS
<p> &emsp; </p>

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/FKafBCx.png" height="80%" width="80%" alt="CGI"/>
</p>
<p>
- Create a windows 10 vm in azure.<p></p>
- Enable IIS & CGI.<p></p>
[start -> control panel -> uninstall a program -> turn windows features on/off -> highlight IIS -> expand www services / app dev feat -> highlight CGI]<p></p>
<p> &emsp; </p>
- Install php manager and the rewrite module.<p></p>
- Create a folder in C: named "PHP" and extract the php binaries to it.
</p>
<br />
<p> &emsp; </p>
<p> &emsp; </p>


<p>
<img src="https://i.imgur.com/yk5yUID.jpeg" height="80%" width="80%" alt="mySQL"/>
</p>
<p>
- Install Visual C++ Redistributable 2015-2022 & mySQL.<p></p>
[mySQL wizard -> [typical] -> launch -> [standard] -> password = "root" -> execute]<p></p>
<p> &emsp; </p>
- Open IIS as admin and set php-cgi.exe from PHP Manager.<p></p>
[start -> IIS(admin) -> PHP Manager -> register new version -> C:\PHP\php-cgi.exe]<p></p>
<p> &emsp; </p>
- Restart IIS.
</p>
<br />
<p> &emsp; </p>
<p> &emsp; </p>


<p>
<img src="https://i.imgur.com/x5Tzfsr.png" height="80%" width="80%" alt="phpManager"/>
</p>
<p>
- Unzip osTicket.zip, move the upload folder to c/inetpub/wwwroot and rename it "osTicket".<p></p>
- Rename c/inetpub/wwwroot/osTicket/include/ost-sampleconfig.php to ost-config.php<p></p>
- Assign permissions to ost-config.php<p></p>
[properties -> security -> advanced -> disable inheritance -> add -> select principal -> "Everyone" -> Full control]<p></p>
<p> &emsp; </p>
- Reload IIS and launch osTicket (sites / web site / osTicket / browse http)<p></p>
- Enable php_imap.dll, php_intl.dll, php_opcache.dll<p></p>
[IIS -> sites -> default -> osticket -> PHP Manager -> enable/disable extensions]
</p>
<br />
<p> &emsp; </p>
<p> &emsp; </p>


<p>
<img src="https://i.imgur.com/iBhfqwC.png" height="80%" width="80%" alt="heidi"/>
</p>
<p>
- Continue to the next page filling in the credentials of the first 2 sections of the page.<p>
(the admin and default emails must be different)<p></p>
- Install (defaults on everything) and launch HeidiSQL and create a new session.<p></p>
[new -> user/pass : root/root -> open -> right-click unnamed -> create new -> database -> "osTicket"]<p></p>
<p> &emsp; </p>
- the mySQL section of the page can now be filled out with:<p></p>
mySQL database: osTicket<p></p>
mySQL username: root<p></p>
mySQL password: root
</p>
<br />
