# Ubuntu_Linux_Essentials
## Mahara-Tech

## CH05_User and Group Administration
### VID04_Adding a New User Account
- sudo useradd user1
- tail -1 /etc/passwd
- tail -1 /etc/group
- sudo useradd -u 1005 -g user1 -c"user2 HR office 1010" -md /home/user2 -s /bin/bash user2
### VID05_Adding Password to User Accounts
- sudo passwd user1
- su - user2
- id
- exit
### VID06_Modifying User Accounts
- sudo usermod -aG secondaryGroup user2 (g: primary group, G: secondary group, a: add)
- userdel -r user2 (r: to delete user2 with home dir)
### VID07_Password Aging Policies
- chage [option] username
### VID08_Managing Groups
- groupadd groupName
- groupmod -n newGroupName oldGroupName
- groupdel groupName
- find /-nogroup
- gpasswd
### VID09_Changing Active Group
- chgrp otherGroup fileName
- newgrp groupName ; exit (to out from newgrp command)
- groups
### VID10_Switching Accounts
- su - user2 -c ls
### VID11_"sudo" Command
- /etc/sudoers
- Cmnd_Alias USER = Commands
- user2 ALL=USER
  ![sudoers.jpg](./sudoers.jpg)
## CH06_File Ownership and Permissions
### VID01_File Ownership
- chown user1 file1
- chown user1:group1 file1
- chown :group1 file1
### VID02_File Permissions
- chmod u+x file
- chmod 4775 file
### VID03_Changing the Permissions
- Symbolic Mode
  - Operator (+, -, =)
  - Permissions (r, w, x)
  - chmod u+x,go+r file
  - chmod ugo-x testFile
- Octal Mode
  - (owner (rwx)111, group (rwx)111, other (rwx)111) 777
  - chmod 777 file 
### VID04_Set UID Bit
![]()
