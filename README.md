# Ad_User_Management
Automating Active Directory User Management with Python
This project provides a comprehensive Python-based solution for automating key Active Directory (AD) tasks such as:

Creating users

Resetting passwords

Disabling accounts

Managing AD group memberships

It uses the pyad library to interact with Active Directory. Ideal for system administrators and IT professionals looking to streamline repetitive AD management tasks.

🚀 Features
✅ Create new AD users

🔁 Reset user passwords

🚫 Disable user accounts

👥 Add users to AD groups

📃 List group members

📝 Logging of all operations

🛠️ Prerequisites
Python 3.6+

Domain-joined Windows machine with access to your Active Directory

pyad library installed:

bash
Copy
Edit
pip install pyad
Environment Variables Set:

AD_USERNAME

AD_PASSWORD

To set environment variables temporarily (Windows Command Prompt):

bash
Copy
Edit
set AD_USERNAME=admin@yourdomain.com
set AD_PASSWORD=YourStrongPassword123
Or permanently via:
Control Panel → System and Security → System → Advanced System Settings → Environment Variables

⚙️ Usage
bash
Copy
Edit
python ad_user_management.py [options]
Available Options:
Command	Description
--create USER PASS	Create a new user
--reset USER NEWPASS	Reset password for a user
--disable USER	Disable a user account
--addgroup USER GROUP	Add a user to a group
--listgroup GROUP	List all members of a group

Examples:
bash
Copy
Edit
python ad_user_management.py --create johndoe P@ssw0rd123
python ad_user_management.py --reset johndoe N3wP@ssword!
python ad_user_management.py --disable johndoe
python ad_user_management.py --addgroup johndoe "HR Team"
python ad_user_management.py --listgroup "Site Engineers"
🧩 Automation with Task Scheduler
Create a Batch File (Optional):
bat
Copy
Edit
@echo off
set AD_USERNAME=admin@yourdomain.com
set AD_PASSWORD=YourStrongPassword123
python "C:\Scripts\ad_user_management.py" --listgroup "Site Engineers"
Schedule It:
Open Task Scheduler

Click Create Basic Task

Set trigger (e.g., daily)

Action: Start a program → select the .bat file

🔐 Best Practices
Security: Never hard-code passwords. Use encrypted secrets when possible.

Logging: All actions are logged to ad_user_management.log.

Testing: Test on a staging AD before production use.

🧪 Real-World Use Cases
Automate onboarding (user creation + group assignments)

Offboarding (account disabling)

Bulk password resets

Group membership audits

🧰 Files
ad_user_management.py: Main automation script

run_ad_script.bat: (Optional) Batch file for automation

ad_user_management.log: Log file generated during script execution

📞 Support
For help or customization, contact with me at rana.farooqhassan@gmail.com.

