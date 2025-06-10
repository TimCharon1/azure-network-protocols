<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />



- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Item 1
- Item 2
- Item 3
- Item 4
- Item 5

<h2>Installation Steps</h2>

![image](https://github.com/user-attachments/assets/8d7615ec-9ebe-483d-a86d-fd559130bc9c)


<p>

📁 Create File Shares with Varying Permissions

1. **Log into `DC-1`** as `mydomain.com\jane_admin`

2. **Log into `Client-1`** as a standard domain user (e.g., `mydomain\someuser`)

3. **On `DC-1`, create folders on `C:\`:**

   * `read-access`
   * `write-access`
   * `no-access`
   * `accounting` *(leave unconfigured for now)*

4. **Configure Share Permissions:**

   * `read-access` → Group: `Domain Users` → **Read only**
   * `write-access` → Group: `Domain Users` → **Read/Write**
   * `no-access` → Group: `Domain Admins` → **Read/Write** *(no access for regular users)*

> Test access from `Client-1` to confirm permissions behave as expected.

</p>
<br />

![image](https://github.com/user-attachments/assets/caf9a377-48ed-4fba-a189-5e896f9e6fb5)

<p>
🧾 Create “ACCOUNTANTS” Security Group & Test Access

1. **On `DC-1`:**

   * Open **Active Directory Users and Computers (ADUC)**
   * Create a new **Security Group**: `ACCOUNTANTS`
   * On the `C:\accounting` folder:

     * Share the folder if not already shared
     * Set permissions: Group `ACCOUNTANTS` → **Read/Write**

2. **On `Client-1`:**

   * Log in as a regular user (e.g., `mydomain\someuser`)
   * Attempt to access `\\DC-1\accounting`
     → ❌ Access denied

3. **Back on `DC-1`:**

   * Add `someuser` to the `ACCOUNTANTS` security group

4. **Return to `Client-1`:**

   * Log back in as `someuser`
   * Retry accessing `\\DC-1\accounting`
     → ✅ Access granted

> Demonstrates group-based access control using domain security groups.

</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
