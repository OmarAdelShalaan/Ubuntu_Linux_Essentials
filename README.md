# Ubuntu_Linux_Essentials
## Mahara-Tech
([CH05_User and Group Administration](#ch05_user-and-group-administration)) ([CH06_File Ownership and Permissions](#CH06_File-Ownership-and-Permissions)) ([CH07_Shutting Down/Rebooting the System](#ch07_shutting-downrebooting-the-system)) ([CH08_Overview_ Network Configuration & Initialization Files](#ch08_overview_-network-configuration--initialization-files))


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
- /etc/sudoersin
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
![VID04_Set_UID_Bit.jpg](./VID04_Set_UID_Bit.jpg)
### VID05_Set GID Bit
- 
### VID06_Sticky Bits
- Sticky Bits make available creation and prevent deletion
### VID07_The Default Permissions
- umask
- umask 000 (default)


## CH07_Shutting Down/Rebooting the System
### VID01_The Default PermissionsVirtual Consoles
- Ctrl + Alt + (F1 to F7)
### VID02_The Default PermissionsSystem Shutdown and Reboot
- shutdown
  - init 0
  - poweroff
  - shutdown -h time (Halt after shutdown)
  - shutdown -k now
- reboot
  - shutdown -r
  - reboot
  - init 6
  -  Ctrl + Alt + Del
 
## CH08_Overview_ Network Configuration & Initialization Files
### VID01_The Default PermissionsNetwork Configuration
- hostname
- /etc/host
- ls /sys/class/net
- ifconfig -a
### VID02_Shell Initialization Files
- .bashrc
- .profile



