<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10 Pro, version 22H2 - x64 Gen2

<h2>Post-Install Configuration Objectives</h2>

- Configure Agents/Users
- Configure Teams/Departments/Roles
- Configure SLA (Which is basically a ticket priority system)
- Configure Help Topics
- Set Permissions For Our Users and Agents

<h2>In Depth Photo Guided Configuration Steps</h2>

<p>
<img width="155" height="21" alt="image" src="https://github.com/user-attachments/assets/f82c21ef-d237-4c43-b08a-bbe175cdec9e" /> <img width="150" height="17" alt="image" src="https://github.com/user-attachments/assets/c9f3d5cc-b752-49ec-9f8b-875e394fce4b" />



</p>
<p>
We're gonna start with some important links. http://localhost/osTicket/scp/login.php is the URL that will take you to the Admin/Agent login page, where you can log in and close tickets opened by the users. Now this URL (http://localhost/osTicket) will take you to the user login where you would submit tickets as the customer. We're going to learn how to navigate these as well as create Agents and Users alike to help bring this lab a little reality. To start we will get logged in as the Admin. Once logged in you will see in the upper-right-hand corner it should say "hi..." followed by your name and next to it should say Admin Panel or Agent Panel. These two panels are how you as an admin navigate osTicket, in the Agent Panel you will see pretty much what your agents see, it will be the where they spend most of their day responding to and closing tickets. The Admin Panel is where we will create departments, teams, and roles, as well as move agents around within them etc.. 
</p>
<br />

<p>
<img width="707" height="285" alt="image" src="https://github.com/user-attachments/assets/8d2da101-6b6f-49e9-a56f-0df63e77b949" />
</p>
<p>
First thing we'll do is configure roles, which basically allows us to group people and give certain people certain abilities. To get to that section we'll go to the Admin Panel, then click the Agents tab, and in the tabs under agents you should see roles go ahead and click that. You should see the basic roles already there, like "All Access", "Expanded Access", "Limited Access", and "View Only". So if you want to get an understanding of that you can click "all access" and "view only" then go to permissions and see the difference in permission checked to each role. We are going to create a new role, so go over to the tab labeled "Add New Role", we'll name it "Supreme Admin" and in permissions we'll check every box we can then click "Add Role". 
</p>
<br />

<p>
<img width="697" height="257" alt="image" src="https://github.com/user-attachments/assets/3df22055-463d-4b25-9e30-3643912d351e" />
</p>
<p>
Next we're going to head over to the departments tap, where you should see the default departments, Maintenance, and Support. Departments have unique rules as compared to agents. If a ticket is assigned to the Support Dept. and lets say "Tyler" opened it but his role was View Only he couldn't do the ticket in the site, but if someone else in that dept. had "All Access" then they would be able to complete the ticket. We will be adding a new Dept. called the "SysAdmins" and the "Add New Department" button is in the same place roles was. To start creating SysAdmins we want to make sure the "Parent" option at the top is set to "Top Level Department" and we'll name it SysAdmins obviously, and we can leave the rest default for right now, and we'll head over to the "Access" tab. The access tab is where we would add agents but we don't have any yet, so we'll just click "Create Dept"
</p>
<br />

<p>
<img width="702" height="307" alt="image" src="https://github.com/user-attachments/assets/f288628f-1e15-4861-b1be-91df9772de07" />
</p>
<p>
Now, we'll head over to teams, and teams are basically anybody qualified from any department can be put on the corresponding team. For example if 3 people from the maintenance and 1 person from the support team know how the online banking system works they could all be put on the "Online banking" team. So, we'll head over to the teams tab, and click "add new team". We'll name this new team, "Online Banking" and leave the rest default for now, simply click "create team". 
</p>
<br />

<p>
<img width="497" height="437" alt="image" src="https://github.com/user-attachments/assets/b7b1027c-e90e-4a5b-86b3-f0160ec9fd66" />
</p>
<p>
We will now change the setting so anyone can create a ticket even if they're not registered in the system. So from the Admin Panel, we'll go to the settings tab and then "Users" and just make sure the "Registration Required" box isn't checked. It is a very simple step that I see a lot of people just forget or accidently mess up on, so once you see that the box isn't checked just click "Save changes" and we'll jump to the next step!
</p>
<br />

<p>
<img width="522" height="296" alt="image" src="https://github.com/user-attachments/assets/8663050b-4d2f-4473-bcce-2df1fd4b64a2" /> <img width="715" height="297" alt="image" src="https://github.com/user-attachments/assets/d7b89f19-9216-45c9-9200-f8b3399bbb9d" />
</p>
<p>
Now we will configure some agents to work on some tickets with! For my lab I will call my agents "Jane Doe" and "John Doe", in the same panel as the last step we're going to click the "agents" tab and you should see the default agent is just you. Now we'll go to "add new agent" on the right hand side of the screen, and I'll name mine "Jane Doe" with a fake email address, leave the rest blank until we get to "Username" and I'll put just "jane" for my user, then we'll click "set password" and uncheck the box in the prompt then set the password as "Password1". Now under the access tab we'll put her in the SysAdmins department and give her the "Supreme Admin" role we made earlier. Then we can go to the teams tab and assign her to the "Online Banking" team. Then we'll hit "Create" and Jane will be added to the system. Now we'll John, go to "add new agent" on the right hand side of the screen, and I'll name mine "John Doe" with a fake email address, leave the rest blank until we get to "Username" and I'll put just "john" for my user, then we'll click "set password" and uncheck the box in the prompt then set the password as "Password1". Now under the access tab we'll put him in the "Support" Department, and give him "All Access" and we can just leave the rest blank. Now we can click "create" and it will add john to the system as well.
</p>
<br />

<p>
<img width="502" height="313" alt="image" src="https://github.com/user-attachments/assets/14aeede4-6e0b-4b26-929d-f71b5ce75df6" />
</p>
<p>
Now we can go to the Agent Panel, and from there click "Users" and on the right side we'll click "add new user". This is where we will add our customers or our "users" who will be creating tickets for our agents. After you click add new user we will input the fake email and full name of our user. My user will be just Karen, once you input the fake email and "Karen" for the name you can simply click "add user" (Make sure you keep track of Karen's Email).
</p>
<br />

<p>
<img width="492" height="222" alt="image" src="https://github.com/user-attachments/assets/c3342b87-5df0-4615-a6f5-bc8c07e41cad" />
</p>
<p>
Next we'll configure our SLA's (which is basically a ticket priority system). We'll switch back to our Admin Panel, then go to the manage tab and click "Add New SLA Plan". We will create 3 new SLA Plans, first we'll start with Sev-A which in our case we'll make it the most urgent (Urgency is usually scaled on overall business impact), for name obviously we'll put "Sev-A", for "Grace period" we'll do 1 hour, and for schedule we'll do "24/7" so when a ticket like this gets posted the Help Desk has 1 hour to respond and needs to be ready 24/7. The next SLA will be Sev-B which in our case we'll make it the second most urgent, for name obviously we'll put "Sev-B", for "Grace period" we'll do 4 hour, and for schedule we'll do "24/7" so when a ticket like this gets posted the Help Desk has 4 hour to respond and needs to be ready 24/7. For our last SLA it'll be Sev-C which in our case we'll make it the least urgent, for name obviously we'll put "Sev-C", for "Grace period" we'll do 8 hour, and for schedule we'll do "Mon - Fri 8am - 5pm with U.S. Holiday" so when a ticket like this gets posted the Help Desk has 8 hours to respond within business hours. 
</p>
<br />

<p>
<img width="645" height="397" alt="image" src="https://github.com/user-attachments/assets/ec66eefb-1e2c-4e21-8684-505f2c66008b" />
</p>
<p>
Finally from the same place as the last step we will configure Help Topics. Under the manage tab in the Admin Panel, we will select "Help Topics" and then we'll click "add new help topic" (we'll be creating 5 different help topics). Once that's open we will put "Business Critical Outage" as the topic and the parent topic will be "Report a Problem" then click "Add Topic" and then go back under the help topics tab. Next we'll create another one and we will put "Personal Computer Issues" as the topic and the parent topic will be "Report a Problem" then click "Add Topic" again. Next we'll create another one and we will put "Equipment Request" as the topic and the parent topic will be "General Inquiry" then click "Add Topic" once more. Next we'll create another one and we will put "Password Reset" as the topic and the parent topic will be "Report a Problem" then click "Add Topic" again. Lastly we'll create another one and we will put "Other" as the topic and the parent topic will be "General Inquiry" then click "Add Topic". 
</p>
<br />

<p>
<img width="1375" height="412" alt="image" src="https://github.com/user-attachments/assets/41ec249a-1d7f-406b-b7b3-b8f1c0497683" />
</p>
<p>
That's it for this section, as a recap we created some roles, departments, teams, and agents who will resolve tickets in the next lab, and users who will be making some tickets in the next lab as well. We also set up some SLA's and help topics to help the agents navigate the tickets posted. We are now ready to begin making and closing fake tickets in the next section! If you happen to be taking a break in-between sections and don't want your VM's to be racking up some charges you can go to Azure and just stop them from running until you wanna get started on the next section! My VM's in the image above are a little different, they are for another project I'm working on right now but it should show you how to do it and what the status should look like if you have successfully stopped them.
</p>
<br />






