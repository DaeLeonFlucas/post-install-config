<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br /><br />

This is a continuation of the [osTicket - Prerequisites and Installation Lab](https://github.com/DaeLeonFlucas/osticket-prereqs)<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- osTicket
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

1. Familiarity with the osTicket UI
2. Configure Roles, Departments, Teams, and Users
3. Configure Service Level Agreement (SLA) Plans and Help Topics


<h2>osTicket UI</h2>
<p>
When navigating the osTicket User Interface (UI), note there are two panels: the Agent Panel and Admin Panel. You will know which panel you are on if the opposite panel is displayed on the top right of the UI. You will switch back and forth between the two panels during the post-configuration installation lab. 
  
In the photo below, you can see we are on the Agent Panel since the UI is displaying the Admin Panel as an option in the top right:
</p>
<p>
<img src="https://imgur.com/bV72KPM.png" height="70%" width="70%" alt="osTicket"/>
</p>


<h2>Configure Roles</h2>
<p>
To setup the proper osTicket configurations, you must log in with the 'user_admin' account that was created in the [osTicket - Prerequisites and Installation Lab](https://github.com/DaeLeonFlucas/osticket-prereqs)
</p>
<p>
Login using the account created.
</p>
<p>
<img src="https://imgur.com/0YfQFj8.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
Roles are the permissions granted to Agents per Department that they have access to. Navigate to the Admin Panel, select Agents -> Roles, and click 'Add New Role'.
</p>
<p>
<img src="https://imgur.com/YekL3QB.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
We will create a new Role named 'Supreme Admin'. Once you have entered the name, select the 'Permissions' tab and ensure that all the permissions under the 'Tickets', 'Tasks', and 'Knowledgebase' tabs are checked to allow all permissions for this Role. Once all boxes have been checked, click 'Add Role'.
</p>
<p>
<img src="https://imgur.com/GBZ8gQy.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
<img src="https://imgur.com/BftSAif.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
<img src="https://imgur.com/liBmY8w.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
<img src="https://imgur.com/MpxDdQI.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
Once all boxes have been checked, click 'Add Role'.
</p>



<h2>Configure Deparments</h2>
<p>
Departments are used to route and resolve tickets based on their importance or instructions.
To configure Departments, head to the Admin Panel then select Agents -> Departments, and click on 'Add New Department'.
</p>
<p>
<img src="https://imgur.com/FIknaQW.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
We will create a new department named 'System Administrators'. Once you have typed the name, click 'Create Dept'.
</p>
<p>
<img src="https://imgur.com/ftyyfpP.png" height="70%" width="70%" alt="osTicket"/>
</p>




<h2>Configure Teams</h2>
<p>
Teams allow you to pull Agents from different Departments and organize them to handle a specific issue or user via a Help Topic or Ticket Filter.
To configure Teams, head back to the Admin panel then go to Agents -> Teams, and click on 'Add New Team'. Create a new team called 'Level II Support', and add your current user account to the Team.
</p>
<p>
<img src="https://imgur.com/bWC5aor.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
<img src="https://imgur.com/xGbRUFS.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
Once done, click on 'Create Team'.
</p>





<h2>Configure Agents</h2>
<p>
Agents are given the access to the help desk in osTicket to respond, resolve, and update the status of tickets. To configure Agents or the ones who will be resolving the tickets, go to the Admin panel go to Agents -> Add New, and click on 'Add New Agent'.
</p>
<p>
<img src="https://imgur.com/cKtoFdN.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
Here we will create two new agents. The first Agent will be named 'jane doe' with the email 'jane.doe<span>@</span>osticket.com' and username 'jane.doe'. 
<p>
<img src="https://imgur.com/e7okRmE.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
Once you have set the proper information click on 'Set Password'. Uncheck the boxes 'Send the agent a password reset email' and 'Require password change at next login'. This will allow us to set the password to 'Password1' and enable us to use the password for our next login instead of requiring us to change it at the next login. 
</p>
<p>
<img src="https://imgur.com/WvkjIeB.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
Click on the 'Access' tab and select the 'System Administrators' department with the role of 'Supreme Admin'. For 'Extended Access', add the 'Support' department and 'Supreme Admin' role as well. In the 'Teams' tab, select the 'Level II Support' team and click 'Add'.
</p>
<p>
<img src="https://imgur.com/aLLJRoN.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
Finally, click on 'Save Changes' to create a new Agent. 
</p>
<p>
<img src="https://imgur.com/XkHoEHJ.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
We will create a second Agent with the name 'john smith'. The creation process is similar to the previous Agent creation process with just a few changes. Ensure the user's name, email, username, and password are properly set. 

In the 'Access' tab, set the 'Primary Department' to 'Support' and the role to 'Supreme Admin'.

Next, in 'Teams' add the 'Level I Support' team, then click Save changes.
</p>
<p>
<img src="https://imgur.com/ahYOo13.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
<img src="https://imgur.com/tr1GKHu.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
<img src="https://imgur.com/sRUx8p6.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
Please note, when configuring a true work/production environment osTicket instance, ensure that you apply the concept of 'Least Privilege' to only provide the least amount of access a user needs to complete their duties. However, for the sake of this lab, we will allow john smith to have a 'Supreme Admin' role.
</p>




<h2>Configure Users</h2>
<p>
Users are creators and owners of tickets and by using osTicket they can track the status of their tickets. To configure Users who will submit tickets into the osTicket system, navigate to the Agent panel then click on Users -> Add New. Here we will create two new Users.
</p>
<p>
<img src="https://imgur.com/d75tPfh.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
Our two new users will be 'karen karen' with the email 'karen<span>@</span>osticket.com' and 'ken ken' with the email 'ken<span>@</span>osticket.com'. Once you have entered the proper information for each user, click on 'Add User'.
</p>
<p>
<img src="https://imgur.com/OV9Lf0p.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
<img src="https://imgur.com/uppLFPo.png" height="70%" width="70%" alt="osTicket"/>
</p>




<h2>Allow Anyone to Create Tickets</h2>
<p>
Access the Admin Panel, go to the Settings tab, and click on Users, make sure Registration Required is unchecked. This will allow the user to create tickets without logging in.
</p>
<p>
<img src="https://imgur.com/oJnMe9z.png" height="70%" width="70%" alt="osTicket"/>
</p>

<h2>Configure SLA Plans</h2>
<p>
The purpose of the SLA Plan is to provide a length of time in which the help desk Administrator expects tickets to be closed. To create new SLA plans, navigate to the Admin Panel then go to Manage -> SLA, and click on 'Add New SLA Plan'.
</p>
<p>
<img src="https://imgur.com/4vdq2E4.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
We will create three separate SLA plans with different specifications for low-, medium-, and high-severity tickets. Create each SLA Plan with the following specifications:

1.) SEV-A with 1 hour Grace Period, 24/7 schedule

2.) SEV-B with 4 hour Grace Period, 24/7 schedule

3.) SEV-C with 8 hour Grace Period, Business Hours schedule

Below is an example of the creation of SLA Plan 'SEV-A'. 
</p>
<p>
<img src="https://imgur.com/drQqlQw.png" height="70%" width="70%" alt="osTicket"/>
</p>



<h2>Configure Help Topics</h2>
<p>
Help Topics will determine what Department the ticket is routed to which will determine which Agents have access to the ticket. The Help Topic also can determine other configurations of the ticket, such as the ticket’s SLA (or Service Level Agreement) and priority of a ticket, i.e. Emergency to Low.

osTicket creates four Help Topics. Feedback, General Inquiry, Report a Problem, and Report a Problem/Access Issue by default.

To configure new Help Topics navigate to the Admin Panel then to Manage -> Help Topics and select 'Add New Help Topic'.
</p>
<p>
<img src="https://imgur.com/gjgq1od.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
Create four different Help Topics based on the potential severity a ticket could have. Here are some examples:
  
- Business Critical Outage
- Personal Computer Issues
- Equipment Reset
- Password Reset

Click on 'Add Topic', to create a new Help Topic.
</p>
<p>
<img src="https://imgur.com/aqD2s17.png" height="70%" width="70%" alt="osTicket"/>
</p>

<p>
Congratulations! You have completed the osTicket Post Installation Configuration! 

To learn about osTicekt's Ticket Lifecycles continue to the [osTicket - Ticket Lifecycle: Intake Through Resolution Lab](https://github.com/andrewkhun/ticket-lifecycle)

</p>
 