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

# ⚙️ Post-installation Configuration

### 🗑️ Deleting "setup" folder

To get rid of the `⚠️ Please take a minute to delete setup directory (../setup/) for security reasons.` message:

1. Navigate to `C:\inetpub\wwwroot\osTicket`, right-click the `setup` folder and then click `Delete`

<img src="/images/delete-setup-folder.png" alt="Delete Setup Folder">

### 👑 Adding a New "Master Admin" role

2. Open `http://localhost/osTicket/scp/logs.php` in a web browser, enter the correct credentials

1. Navigate to `Agents` > `📋 Roles` > `(+) Add New Role`

2. In the `📄 Definition` tab:
    - In the **Name:** field, enter the desired role. In this case, it is `Master Admin`
    - Optionally, add any desired details regarding the new role in the __*Internal Notes*__ field

3. In the `🔒 Permissions` tab, give all available permissions to the Master Admin:
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

1. Navigate to `Agents` > `🧑‍💻 Departments` > `(+) Add New Department`

2. In the **Name:** field, enter `System Administrators`

3. Scroll to the bottom of the page and click the orange `Create Dept` button

<img src="/images/add-sys-admin-department.png" alt="Add System Administrators Department">

### 🤝 Adding a New "Level II Support" Team

1. Navigate to `Agents` > `👨🏻👨🏾 Teams` > `(+) Add New Team`

2. In the **Name:** field, enter `Level II Support`

3. At the bottom of the page, click the orange `Create Team` button

<img src="/images/add-level2-support-department.png" alt="Add Level II Support Team">

### 🎟️ Allowing Non-registered Users to Create Tickets

1. Navigate to `Settings` > `👥 Users` > Tick ✅ `Require registration and login to create tickets`

2. At the bottom of the page, click the orange `Save Changes` button

<img src="/images/adjust-ticket-permissions.png" alt="Adjust Ticket Permissions">

### 📝 Adding New Agents

1. Navigate to `Agents` > `👤 Agents` > `(+) Add New Agent`

2. In the `Account` tab, fill out the **Name:**, **Email Address:**, and **Username:** fields for the particular Agent being added. Do the same for any desired settings in the `Access` and `Permissions` tabs as well.

3. At the bottom of the page, click the orange `Create` button

4. Repeat these steps until as many Agents as desired have been added

<img src="/images/add-agents.png" alt="Add Agents">

<img src="/images/agents-list.png" alt="Agents List">

### 📃 Adding Service Level Agreements (SLAs)

1. Navigate to `Manage` > `📚 SLA` > `(+) Add New SLA Plan`

2. Fill out the information in accordance to the SLA plan of choice

3. At the bottom of the page, click the orange `Add Plan` button

<img src="/images/add-SLAs.png" alt="Add SLAs">

### ❓ Adding Help Topics

1. Navigate to `Manage` > `❓ Help Topics` > `(+) Add New Help Topic`

2. In the **Topic:** field, enter the relevant information for the topic of choice

3. At the bottom of the page, click the orange `Add Topic` button

<img src="/images/add-help-topic.png" alt="Add Help Topic">
