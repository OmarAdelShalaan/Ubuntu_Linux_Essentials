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
