Overview
The Email Trigger is basically GECS job designed to automatically send email notifications to the product owner and a specified distribution list. The emails notify recipients about the expiration status of system passwords. The project is built using C# and SQL, and it includes several key functionalities to monitor and alert based on the expiration dates of passwords.

Features
Password Expiry Notification:

The get_pwd_expiry_date stored procedure fetches records from the database for users whose passwords are due to expire within the one month.
Based on the number of days remaining until the password expires, the system triggers an email with color-coded status:
Red: Password expired or expiring within 7 days.
Amber: Password expiring within 8-15 days.
Yellow: Password expiring within 16-30 days.

Email Subject Customization:

The system names are printed in the subject line for specific login names whose passwords are expiring.

Setting Up Temporary Password for Gmail:

To generate a temporary password from your Gmail account to use in this project, follow these steps:

1.] Go to "Manage your Google account."
2.] Navigate to the "Security" section.
3.] Enable "2-Step verification."
4.] After enabling 2-Step verification, go to "App passwords."
5.] In "App passwords," select "Mail" and "Windows Computer" from the dropdown menu.
6.] Password will be generated, copy that password and paste it into the appropriate field in the C# code.

Project Structure: 
1.] EmailTrigger.sln: The solution file for the Email Trigger project.
2.] EmailTrigger: Contains the main C# project files.
3.] SQLScripts: Contains SQL scripts used by the application.
4.] Description: Contains documentation and descriptions of the project's functionality.

Requirements:
1.] .NET Framework: Required for running the C# project.
2.] SQL Server: Required for running the database scripts and stored procedures.
3.] Gmail Account: For sending emails, with app-specific passwords configured as described above.

Getting Started:
1.] Clone or download the repository.
2.] Set up the database using the scripts provided in the SQLScripts directory.
3.] Open the EmailTrigger.sln solution file in Visual Studio.
4.] Update the email configuration in the C# code with your Gmail app-specific password as well as emails.
5.] Build and run the project.
