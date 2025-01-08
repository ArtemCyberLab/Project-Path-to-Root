Project Description: In this project, I practiced exploiting vulnerabilities on a test machine using network scanning, password cracking, and privilege escalation techniques. The task was completed legally on the TryHackMe platform for educational purposes.

Steps:

System Scanning:
Using nmap, open ports 22 (SSH) and 80 (HTTP) were discovered, indicating the availability of the SSH and web servers.

Directory Enumeration:
By using gobuster, several interesting directories were found, such as /images and robots.txt.

Password Cracking:
With the help of hydra and the rockyou.txt wordlist, I successfully cracked the password for the user meliodas, granting access via SSH.

User Flag:
After successfully logging in via SSH, the user flag (user.txt) was located in the home directory of meliodas.

Privilege Escalation:
Running the command sudo -l revealed that the user meliodas had permission to execute the script /home/meliodas/bak.py with root privileges.
I decided to delete the original bak.py file and replace it with my own script that launches a root shell.

Root Flag:
After executing the modified script, I gained root access, and the root flag (root.txt) was successfully retrieved.

Conclusion: The project demonstrated the importance of properly configuring permissions for privileged commands and controlling access to critical files. All steps were performed within the framework of an educational task on the TryHackMe platform, ensuring the process was completely legal and ethical.
