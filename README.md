# Warning this is a temporal fix for VMware 17.6 Installer

# What's happend?

Some people reported some issues for install the VMware Workstation Pro 17.6 in Non-English Systems.

I discover how to fix that.

# How to fix that?

- Press Ctrl + R and appears the Run window.
- Write `compmgmt` and press enter
- Find "Users and Local Groups"
- Find "Groups"
- ![image](https://github.com/user-attachments/assets/dea9874b-c49d-40e9-83bb-3c1805d7b20c)

- Find Users group of your system (example: In Spanish it's Usuarios but in your case can be other name) Rename it to Users
- And finally Create a group with name "Authenticated Users"
- Run the installer and cross your fingers!

- ![image](https://github.com/user-attachments/assets/9fa170da-c067-4d57-b912-4d09f107f922)

- After do that changes and installed VMware Workstation you can revert the changes renaming The Users group to the original name
- And the new fake "Authenticated Users" group created successfully

  # How this work?

  The installer it's finding the groups in English only and when you install Windows the groups of the system renames to your language
  So thinking this renaming the users to English can bypass this error
