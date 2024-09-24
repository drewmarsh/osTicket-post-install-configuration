<p align="center">
  <a href="https://github.com/drewmarsh/osTicket-post-install-configuration">
    <img src="/images/osticket-banner.png" width="598" alt="Banner">
  </a>
</p>

### 👉 [Prerequisites & osTicket Installation](https://github.com/drewmarsh/osTicket-installation)

# 🧠 Skills & Technologies Used
- osTicket (Help Desk Ticketing System)
- System Administration
- Microsoft Azure (Cloud computing)
- Microsoft Remote Desktop
- Internet Information Services (IIS)

# ⚙️ Post-Installation Configuration

### 🗑️ Deleting "setup" folder

To get rid of the `⚠️ Please take a minute to delete setup directory (../setup/) for security reasons.` message:

1. Navigate to `C:\inetpub\wwwroot\osTicket`, right-click the `setup` folder and then click `Delete`

<img src="/images/delete-setup-folder.png" alt="Delete Setup Folder">

### 👑 Adding a New "Master Admin" role

Now that osTicket is successfully installed from scratch,  it is time to do some configuration and system administration work. To start this off, we will create a new Role in osTicket called "Master Admin". This will be the highest level administrator that has every single permission available to them. Roles are used to determine an Agent's permissions. Generally, most Agents will not have every single permission as the Master Admin does.

1. Open `http://localhost/osTicket/scp/logs.php` in a web browser, enter the correct credentials

2. Navigate to `Agents` > `📋 Roles` > `(+) Add New Role`

3. In the `📄 Definition` tab:
    - In the **Name:** field, enter the desired role. In this case, it is `Master Admin`
    - Optionally, add any desired details regarding the new role in the __*Internal Notes*__ field

4. In the `🔒 Permissions` tab, give all available permissions to the Master Admin:
    - ✅ `Assign — Ability to assign tickets to agents or teams`
    - ✅ `Close — Ability to close tickets`
    - ✅ `Create — Ability to open tickets on behalf of users`
    - ✅ `Delete — Ability to delete tickets`
    - ✅ `Edit — Ability to edit tickets`
    - ✅ `Edit Thread — Ability to edit thread items of other agents`
    - ✅ `Link — Ability to link tickets`
    - ✅ `Mark as Answered — Ability to mark a ticket as Answered/Unanswered`
    - ✅ `Merge — Ability to merge tickets`
    - ✅ `Post Reply — Ability to post a ticket reply`
    - ✅ `Refer — Ability to manage ticket referrals`
    - ✅ `Release — Ability to release ticket assignment`
    - ✅ `Transfer — Ability to transfer tickets between departments`

<img src="/images/add-master-admin.png" alt="Add Master Admin">

### 🖥️ Adding a New "System Administrators" Department

Each Agent is appointed a specific department which is determined by their assigned role within the helpdesk. For now, we'll just create a "System Administrators" department where the Master Admins will be designated. Various other settings such as email settings, service level agreements (SLAs), and managers can also be configured in the `Departments` tab.

1. Navigate to `Agents` > `🧑‍💻 Departments` > `(+) Add New Department`

2. In the **Name:** field, enter `System Administrators`

3. Scroll to the bottom of the page and click the orange `Create Dept` button

<img src="/images/add-sys-admin-department.png" alt="Add System Administrators Department">

### 🤝 Adding a New "Level II Support" Team

 Teams enable cross-departmental collaboration by aggregating skilled agents from various units. This structure facilitates the creation of specialized groups. For instance, you can develop a help topic related to a specific product and assign it to a team of agents with expertise in that product. In this demonstration, we'll create a "Level II Support Team" to illustrate this concept.

1. Navigate to `Agents` > `👨🏻👨🏾 Teams` > `(+) Add New Team`

2. In the **Name:** field, enter `Level II Support`

3. At the bottom of the page, click the orange `Create Team` button

<img src="/images/add-level2-support-department.png" alt="Add Level II Support Team">

### 🎟️ Allowing Non-registered Users to Create Tickets

Out-of-the-box installations of osTicket require users to be registered and logged-in before they can create tickets. Since this isn't always ideal, the setting regarding this functionality needs to be adjusted.

1. Navigate to `Settings` > `👥 Users` > Tick ✅ `Require registration and login to create tickets`

2. At the bottom of the page, click the orange `Save Changes` button

<img src="/images/adjust-ticket-permissions.png" alt="Adjust Ticket Permissions">

### 📝 Adding New Agents

Next, we'll proceed to create Agents. Agents  are the helpdesk staff responsible for resolving tickets. Each Agent is assigned a primary department and role for tickets within their designated area. Agents can be granted access to multiple departments, with potentially different roles in each. The Access, Permissions, and Teams tabs are used to adjust access levels, manage permissions, and assign teams for each staff member.

1. Navigate to `Agents` > `👤 Agents` > `(+) Add New Agent`

2. In the `Account` tab, fill out the **Name:**, **Email Address:**, and **Username:** fields for the particular Agent being added. Do the same for any desired settings in the `Access` and `Permissions` tabs as well.

3. At the bottom of the page, click the orange `Create` button

4. Repeat these steps until as many Agents as desired have been added

<img src="/images/add-agents.png" alt="Add Agents">

<img src="/images/agents-list.png" alt="Agents List">

### 📃 Adding Service Level Agreements (SLAs)

SLA (Service Level Agreement) Plans define the expected resolution time for specific ticket types. Each SLA incorporates a schedule and a grace period. For instance, in our example, the SEV-A (Severity A) SLA operates on a 24/7 schedule with a one-hour grace period. This structure ensures clear expectations for ticket resolution timeframes.

1. Navigate to `Manage` > `📚 SLA` > `(+) Add New SLA Plan`

2. Fill out the information in accordance to the SLA plan of choice

3. At the bottom of the page, click the orange `Add Plan` button

<img src="/images/add-SLAs.png" alt="Add SLAs">

### ❓ Adding Help Topics

Help Topics facilitate ticket categorization for users. For example, we can create a "Business Critical Outage" topic, which could be used for scenarios such as customers being unable to access mobile banking services. This categorization streamlines the ticket management process and prioritization.

1. Navigate to `Manage` > `❓ Help Topics` > `(+) Add New Help Topic`

2. In the **Topic:** field, enter the relevant information for the topic of choice

3. At the bottom of the page, click the orange `Add Topic` button

<img src="/images/add-help-topic.png" alt="Add Help Topic">
