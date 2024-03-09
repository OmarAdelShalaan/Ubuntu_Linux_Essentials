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
### CH05_VID09_Changing Active Group
- chgrp otherGroup fileName
- newgrp groupName ; exit (to out from newgrp command)
- groups
### VID10_Switching Accounts
- su - user2 -c ls
### VID11_"sudo" Command
- /etc/sudoers
- Cmnd_Alias USER = Commands
- user2 ALL=USER
![](![image](https://github.com/OmarAdelShalaan/Ubuntu_Linux_Essentials/assets/61333881/1604c02f-f479-46b0-b67d-95a918c907a8)
)
