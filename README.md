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
In the osTicket User Interface (UI), there are two primary sections: the Agent Panel and the Admin Panel. The top-right corner will indicate the opposite panel, letting you know your current view. You’ll frequently switch between these panels as part of the post-configuration lab. 
  
In the image below, you’ll notice we are on the Agent Panel, as the Admin Panel option is visible in the top right of the UI.
</p>
<p>
<img src="https://imgur.com/bV72KPM.png" height="70%" width="70%" alt="osTicket"/>
</p>


<h2>Configure Roles</h2>
<p>
To configure osTicket correctly, log in with the ‘user_admin’ account created during the osTicket - Prerequisites and Installation Lab.
</p>
<p>
Login using the account created.
</p>
<p>
<img src="https://imgur.com/0YfQFj8.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
Roles determine the permissions granted to Agents within each Department they can access. In the Admin Panel, navigate to Agents -> Roles, then click on Add New Role to proceed.
</p>
<p>
<img src="https://imgur.com/YekL3QB.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
We’ll set up a new Role titled ‘Supreme Admin’. Enter the name, then navigate to the Permissions tab and check all permissions under the Tickets, Tasks, and Knowledgebase tabs to provide full access for this Role. After confirming all boxes are selected, click Add Role.
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
Once every box is checked, press Add Role to complete the process.
</p>


<h2>Configure Deparments</h2>
<p>
Departments help organize and manage tickets by routing them according to priority or specific guidelines.
o set up Departments, go to the Admin Panel, choose Agents -> Departments, and click Add New Department.
</p>
<p>
<img src="https://imgur.com/FIknaQW.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
To set up Departments, go to the Admin Panel, choose Agents -> Departments, and click create New Department.
</p>
<p>
<img src="https://imgur.com/ftyyfpP.png" height="70%" width="70%" alt="osTicket"/>
</p>




<h2>Configure Teams</h2>
<p>
With Teams, you can assemble Agents from different Departments to collaboratively manage a specific issue or user request through a Help Topic or Ticket Filter.
To set up Teams, return to the Admin Panel, navigate to Agents -> Teams, and select Add New Team. Name the new team ‘Level II Support’ and include your current user account in the Team.
</p>
<p>
<img src="https://imgur.com/bWC5aor.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
<img src="https://imgur.com/xGbRUFS.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
When finished, click on 'Create Team'.
</p>





<h2>Configure Agents</h2>
<p>
Agents are authorized to access the help desk in osTicket for responding to, resolving, and updating ticket statuses. To set up the Agents responsible for ticket resolution, head to the Admin Panel, select Agents -> Add New, and then click Add New Agent.
</p>
<p>
<img src="https://imgur.com/cKtoFdN.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
In this step, we will set up two new agents. The first agent will be ‘jane doe’, using the email ‘jane.doe@osticket.com’ and the username ‘jane.doe’. 
<p>
<img src="https://imgur.com/e7okRmE.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
After entering the necessary information, click on Set Password. Make sure to uncheck the options ‘Send the agent a password reset email’ and ‘Require password change at next login’. This will enable you to set the password to ‘Password1’ and use it for the next login without needing to change it. 
</p>
<p>
<img src="https://imgur.com/WvkjIeB.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
Navigate to the Access tab and select the System Administrators department, assigning the role of Supreme Admin. For Extended Access, include the Support department and set the role to Supreme Admin as well. In the Teams tab, choose the Level II Support team and press Add.
</p>
<p>
<img src="https://imgur.com/aLLJRoN.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
Lastly, click on Save Changes to create the new Agent.
</p>
<p>
<img src="https://imgur.com/XkHoEHJ.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
Next, we will create a second Agent called ‘john smith’. This process is similar to creating the first Agent, with a few adjustments. Ensure that the name, email, username, and password are accurately entered.
Within the Access tab, configure the Primary Department as Support and select the Supreme Admin role.

Then, in the Teams tab, include the Level I Support team and click Save Changes to finalize.
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
It’s important to remember that in a real work or production environment of osTicket, you should apply the principle of ‘Least Privilege’ to grant users only the minimum access necessary for their responsibilities. However, for this lab, we will assign john smith a ‘Supreme Admin’ role.
</p>




<h2>Configure Users</h2>
<p>
In osTicket, Users are responsible for creating and owning tickets, allowing them to monitor their ticket status. To configure Users who will submit tickets into the osTicket system, navigate to the Agent panel and select Users -> Add New. We will add two new Users in this step.
</p>
<p>
<img src="https://imgur.com/d75tPfh.png" height="70%" width="70%" alt="osTicket"/>
</p>
<p>
We will create two new users: ‘karen karen’ with the email ‘karen@osticket.com’, and ‘ken ken’ with the email ‘ken@osticket.com’. Once you have filled in the necessary details for each user, click Add User.
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
 