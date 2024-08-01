# Further on Linux
### Linux File Hierarchy
- File system is a directory structure that the OS uses.
- windows : local disk C
- Linux : root directory( / )
#### Linux file structure
1. **/( root )** : Every single file and directory starts from the root directory.
2. **bin** - Binary executables : Essential command binaries that need to be available in single-user mode; for all users.
    - e.g - cat, ls
3. **/boot** - Boot loader files : files used when booting linux.
    - e.g  - kernel initrd
4. **/dev** - Essential device files :  terminal devices, usb, or any device attached to the system.
    - e.g - tty1
5. **/etc - et cetera** : Contains configuration files required by all programs.
    - e.g - resolv.conf
6. **/home - Home directory** : Home directories for all users to store their personal files.
    - e.g - /home/abdiii
7. **/lib - Libraries** : contains libraries for the built-in and downloaded softwares.
8. **/media** : Temporary mount directory for removable devices. such as CD-ROMs.
9. **/mnt** : Temporary mount directory where sysadmins can mount filesystems.
10. **/opt** : Optional application software packages.
    - e.g - Telegram, Microsoft
11. **/sbin - Essential system binaries** : binary executables used typically by system administrator(root). 
    - e.g - adduser.
12. **/tmp - Temporary Files** : temporary files created by system and users.
13. **/usr - User Utilities** : Contains binaries, libraries, documentation, and source-code for second level programs.
##### Text Editors
1. Linux command line text editors
    - VIM (difficult)
    - Nano (user friendly)
2. Linux graphical text editors
    - sublime
    - Vscode
#### Linux User Management
- on linux there are two kinds of users.
    - Root- id=0
    -  Normal user- id 1-999
- The root user have the power to do everything on linux.
- **SUDO = Superuser do** : a command that gives a user root access. 
##### users can be created using commands:-
1. useradd(simple)
2. adduser(detailed) - automatically created in /home directory.
- The Users file are stored inside */etc/passwd*.
- Thee users password are stored inside */etc/shadow*.
- **sudo su** - a command that gives root user privilege. 
