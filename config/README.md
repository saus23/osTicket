<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>
<p> &emsp; </p>


<h1>osTicket - Administration Panels</h1>
This tutorial outlines the staff and admin panels of osTicket.<br />
<p> &emsp; </p>


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
<p> &emsp; </p>

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)
<p> &emsp; </p>


<h2>Administration Panels</h2>

<p>
<img src="https://i.imgur.com/3PLR866.png" height="80%" width="80%" alt="SLAs"/>
</p>
<p>
Login URLs:<p></p>

  - Admin/Agent: http://localhost/osTicket/scp/login.php<p></p>
  - End-user: http://localhost/osTicket<p></p>
<p> &emsp; </p>
- Configure Roles: Admin Panel -> Agents -> Roles<p></p>

>Edit and create permission groups.<p>
<p>[Add new role -> "superuser" -> permissions -> assign everything -> Add Role]
<p> &emsp; </p>
- Configure Dept: Admin Panel -> Agents -> Departments<p></p>

>Ticket visibility (help desk vs sysAdmins vs networking).<p>
<p>[Add new department -> "sysAdmins" -> Access -> add agents -> Create Dept]
<p> &emsp; </p>
- Configure Teams: Admin Panel -> Agents -> Teams<p></p>

>Assign agents from various Departments.<p>
<p>[Add new Team -> "Online Banking" -> Members -> add agents -> Create Team]
<p> &emsp; </p>
- Allow Unregistered: Admin Panel -> Settings -> User Settings -> [uncheck registration required]<p></p>
</p>
<br />
<p> &emsp; </p>
<p> &emsp; </p>

<p>
<img src="https://i.imgur.com/uARAmPf.png" height="80%" width="80%" alt="help-topics"/>
</p>
<p>
- Configure Agents: Admin Panel -> Agents -> Add Agent<p></p>

>Ticket workers.<p>
<p>[Create 2 agents (jane/john) -> Access (superuser/support) -> Teams (Online Banking/none)]
<p> &emsp; </p>
- Configure Users: Agent Panel -> Users -> Add User<p></p>

>Normal users or customers.<p>
<p>[Create "Karen"]
<p> &emsp; </p>
- Configure SLAs: Admin Panel -> Manage -> SLA<p></p>

>Severity levels and deadlines.<p>
<p>[Create 3 SLA plans -> (Sev-a/grace=1/24-7), (Sev-B/grace=4/24-7), (Sev-C/grace=8/business hours)]
<p> &emsp; </p>
- Configure Topics: Admin Panel -> Manage -> Help Topics<p></p>

>Predefined ticket categories and Departments.<p>
<p>[Add 2 new topics -> "Billing" & "Network Outage" -> Parent: Report a problem -> Add topic]
<p> &emsp; </p>
</p>
<br />
<p> &emsp; </p>
<p> &emsp; </p>

<p>
<img src="https://i.imgur.com/d0Wch9b.png" height="80%" width="80%" alt="ticket"/>
</p>
<p>
- Login as Karen and create a new ticket.<p></p>

>Select "Billing" for a ticket about network problems
<p> &emsp; </p>
- Login as John and correct the ticket.<p></p>

>Set Sev-A / Help Topic = Networking / Assign to "Online Banking"
<p> &emsp; </p>
- Login as Jane. Assign to self and close the ticket.<p></p>
- Tickets can also be created by agents for phone call tickets from the Admin Panel.
</p>
<br />
