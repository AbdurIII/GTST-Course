# Advanced Linux User
### Further on user management
##### some advanced user comands
- to change password of user = ==sudo passwd username
- to change user id = ==sudo usermod -u new_id username
- to delete user = ==sudo userdel -r username
- to change user on terminal = ==su - username
- to allocate a user created by *useradd* command in home directory = ==usdo mkhomedir_helper username
- to change users shell type = ==sudo usermod username -s /bin/shelltype
- The *sudoers file* is a file Linux and Unix administrators use to allocate system rights to system users.
- The user you created doesn’t have power to use sudo as the original one.
- to access this file = ==sudo visudo
- then to grant the user to access sudoers add ==ALL=(ALL:ALL) ALL== or ==ALL=ALL== in user privilege specifictions and the user can use sudo command after this.
### Linux File Permissions
- Every file on linux have their own **owner** and **permissions**
- there are 5 main parts on the listing
    - permission
    - owners 
    - size
    - date 
    - file name
- ownership have two kinds **user** and **group**
- to change the owner of the file ==sudo chown user:group filename
- there are 3 types of permissions
    - Read(r)
    - Write(w)
    - Execute(x)
- begins with **d** = file and begins with **-** = file
- permission have 3 parts **user(u)**, **group(u)**, **other(o)**. 
- to change file permission = ==sudo chmod [option] filename
- Each of the permission have a number representations.
    - Read(r) = 4
    - write(w) = 2
    - Execute = 1
- syntax = ==sudo chmod [parameter] filename 
- **+** = giving perission and **-** removing permission
##### there are 3 special file permissions
1. **SUID bits(s) - set user ID bit -** add 4 infront of our numeric value  -> e.g  4000
2. **SGID bits(S) - set group ID bit -** add 2 infront of our numeric value -> e.g 2777
3. **Sticky bits(t) - set other ID bit -** add 1 in front of our numeric value -> 1602
- They are permissions like the execute(x), but they will set the execute permission to the user who settled them.
##### package installation on Linux
- **package managers** are a free-software user interface that work with an online server to handle the installation and removal of software on Debian, and Debian-based Linux distributions.
- On debian the package manager is called **APT**(Advanceed Package Tool) also there is called **dpkg**(Debian package manager)
- the site/server kali use to upload the packages is [http.kali.org/kali](http.kali.org/kali)
- **APT** is a free-software user interface that work with an online server to handle the installation and removal of software on Debian, and Debian-based Linux distributions.used for online and offline purpose.
- commands to use
    - sudo apt update
    - sudo apt search [software name]
    - sudo apt install [software name]
    - sudo apt remove [software name]
    - sudo apt upgrade
    - sudo apt purge [software name]
- A software can be built based on another program called **modules**.
- so, a program to work properly, the **package dependencies** have to be installed successfully.
- **Dpkg** is an offline package managing program.
- syntax
    - sudo dpkg -i [package name]
    - sudo dpkg -r [package name]
    - sudo dpkg -p [package name]
