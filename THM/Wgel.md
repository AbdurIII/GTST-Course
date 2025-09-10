# Information
- CTF Name: Wgel CTF
- CTF Level: Easy
- CTF Description: Can you exfiltrate the root flag?
- Date: 23-09-2024
- Platform: Kali Linux
- Category: web pentesting
- IP: 10.10.224.190
# Findings
### Credentials
`FoundCREDs`
- I began the wgel CTF by assigning machine IP address to **wgel.thm**.

![[Selection_008.png]]
- Then continued by creating some directories for simplification of documenting files.
![[Selection_006 1.png]]
![[Selection_007.png]]
## External
### Enumeration
`$enum$`
- I used Nmap to enumerate open ports and machine versions.
    - -sV = a flag for version 
![[Selection_009.png]]
## Internal
### Enumeration
`$enum$`
- port 22 and 80 were open that means we can check for its website using port 80(http).
- It was a normal apache2 page.

![[Apache2_Ubuntu_Default_Page_It works - Chromium_001.png]]

- when I checked the source code I found interesting commented text.
![[Selection_010.png]]

- Then I used **dirbuster** to brute force the website directories and some interesting directories and subdirectory popup.
![[Selection_012.png]]

- the directory with **index.html** was the apache2 page that we found first.
- the directory with **server-status** responed 403 which is forbidden site.
- the directory with **sitemap** have a good looking website but I didn't find any valuable clue. 
![[unapp Template - Chromium_001.png]]

- but disbuster discovered a subdirectory for **sitemap** with **.ssh** and I opened it Boom! I got juicy key, Private key to access a shell in the machine.
![[Index of -sitemap-.ssh - Chromium_001.png]]

![[Selection_014.png]]

- then I copied the key and saved it in the directory I created above giving it a read and write permission for owner only.

![[Selection_015.png]]



### Gaining Access
- I tried connecting to ssh using the key and username ( **jessie** ) I found on apache2 page source code and it was successful. 

![[Selection_017.png]]
### Maintaining Access
- now that I had access to jessie I went searching for a flag and got one😎🚩.
![[Selection_018.png]]
![[Selection_019.png]]

- Now finding the next flag(root) continued which needs privilege escalation to root user.
- I searched a way to escalate a privilege in GTFOBins website and found a code which goes with wgel CTF description **exfiltrate file**.
![[Selection_020.png]]

-  used my device IP ( tun0 ) in the code with port 1234.
![[Selection_021 1.png]]

-  opened a port 1234 using netcat for listening the response.
- woohoo I got the root flag🤯🚩.

![[Selection_022.png]]






# Random Notes
- The CTF only got 2 tasks to complete.
    1. The user flag located in **/home/jessie/Documents/user_flag.txt** file.
    2. The root flag located in **/root/root_flag.txt** file.

![[TryHackMe_Wgel CTF - Chromium_002.png]]