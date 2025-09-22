# linux-for-devops

# 📂 Linux Commands Cheatsheet
This document organizes and explains a wide range of Linux commands, grouped by functionality. It covers navigation, file manipulation, user management, networking, process monitoring, compression, and more.

---

## ✅ File and Directory Management

Commands for navigating, creating, and manipulating files and directories.

### Install vim: if not install already then install vim package.
```bash
apt install vim
```

| Command | Description | Example |
|------|--------------|--------|
| `cd` | Change directory | `cd /home/user` |
| `cd ..` | Move to parent directory | `cd ..` |
| `pwd` | Show current directory | `pwd` |
| `ls` | List files and folders | `ls` |
| `ls -l` | Long listing format | `ls -l` |
| `ls -ltr` | List files sorted by time (oldest first) | `ls -ltr` |
| `ls -a` | List all files including hidden ones | `ls -a` |
| `mkdir` | Create a directory | `mkdir new_folder` |
| `rmdir` | Remove an empty directory | `rmdir old_folder` |
| `rm` | Remove file(s) | `rm file.txt` |
| `rm -r` | Recursively remove directories | `rm -r folder` |
| `touch` | Create an empty file or update timestamp | `touch newfile.txt` |
| `cat` | Show file content | `cat file.txt` |
| `head` | Show first lines | `head file.txt` |
| `cut -b 1 filename` | Extract specific byte(s) | `cut -b 1 file.txt` |
| `echo "something" > file.txt` | Write to file (overwrite) | `echo "Hello" > file.txt` |
| `cp source destination` | Copy file | `cp file.txt backup.txt` |
| `cp -r source destination` | Copy directories recursively | `cp -r folder backup_folder` |
| `mv source destination` | Move or rename files | `mv file.txt folder/` |
| `mv oldname newname` | Rename file | `mv oldname.txt newname.txt` |
| `ln source destination` | Create hard link | `ln file.txt linkfile.txt` |
| `ln -s source destination` | Create symbolic link | `ln -s file.txt symlink.txt` |
| `wc` | Count lines, words, characters | `wc file.txt` |
| `tee` | Write to file and display | `echo "Hi" | tee file.txt` |
| `sort` | Sort file content | `sort file.txt` |
| `diff file1 file2` | Compare two files | `diff file1.txt file2.txt` |

---

## ✅ Disk Usage and Storage

Commands to check and manage disk space and usage.

### Install zip: if not install already then install zip package.
```bash
apt install zip
```

| Command | Description | Example |
|------|--------------|--------|
| `df` | Show disk space usage | `df` |
| `df -h` | Human-readable disk usage | `df -h` |
| `du` | Show directory size | `du` |
| `zip zipfile.zip file` | Compress files | `zip backup.zip file.txt` |
| `zip -r zipfile.zip folder` | Compress directories recursively | `zip -r backup.zip folder/` |
| `unzip zipfile.zip` | Extract zip files | `unzip backup.zip` |
| `tar -cvzf archive.tar.gz folder/` | Create compressed archive | `tar -cvzf backup.tar.gz folder/` |
| `tar -xvzf archive.tar.gz` | Extract compressed archive | `tar -xvzf backup.tar.gz` |

---

## ✅ Process Monitoring and System Info

Commands to view and control processes and system state.

| Command | Description | Example |
|------|--------------|--------|
| `top` | Real-time process monitoring | `top` |
| `ps` | List processes | `ps aux` |
| `fuser` | Show process using a file | `fuser file.txt` |
| `kill` | Terminate process | `kill PID` |
| `free` | Show memory usage | `free -h` |
| `nohup` | Run process immune to hangups | `nohup script.sh &` |
| `vmstat` | System resource statistics | `vmstat` |
| `uname` | Show system info | `uname -a` |
| `uptime` | Show how long system is running | `uptime` |
| `date` | Show current date/time | `date` |
| `who` | Show who is logged in | `who` |
| `whoami` | Show current user | `whoami` |
| `which` | Find executable location | `which python` |
| `shutdown` | Shutdown system | `sudo shutdown now` |
| `reboot` | Restart system | `sudo reboot` |

---

## ✅ User and Group Management

Commands for handling users, groups, and permissions.

| Command | Description | Example |
|------|--------------|--------|
| `sudo` | Run commands as superuser | `sudo apt update` |
| `apt` | Package manager | `sudo apt install package` |
| `apt-get` | Lower-level package manager | `sudo apt-get upgrade` |
| `useradd` | Add user | `sudo useradd username` |
| `useradd -m` | Add user with home directory | `sudo useradd -m username` |
| `passwd` | Change user password | `sudo passwd username` |
| `su` | Switch user | `su username` |
| `exit` | Exit shell session | `exit` |
| `userdel` | Delete user | `sudo userdel username` |
| `groupadd groupname` | Add group | `sudo groupadd mygroup` |
| `gpasswd -a username groupname` | Add user to group | `sudo gpasswd -a user group` |
| `gpasswd -M "user1,user2" groupname` | Set group members | `sudo gpasswd -M "user1,user2" mygroup` |
| `groupdel groupname` | Delete group | `sudo groupdel mygroup` |
| `list groups` | Show groups | `cat /etc/group` |
| `list users` | Show users | `cat /etc/passwd` |
| `chmod 777 filename` | Change file permissions | `chmod 777 file.txt` |
| `umask` | Set default permissions | `umask 022` |
| `chown` | Change file owner | `sudo chown user file.txt` |
| `chgrp` | Change group ownership | `sudo chgrp group file.txt` |

---

## ✅ Remote Access and File Transfer

Commands to access or transfer files over a network.

| Command | Description | Example |
|------|--------------|--------|
| `ssh` | Secure shell to remote host | `ssh user@host` |
| `ssh -i` | SSH with private key | `ssh -i key.pem user@host` |
| `scp -i pem_file source destination` | Copy files over SSH | `scp -i key.pem file.txt user@host:/path` |
| `rsync -e ssh -avc source destination` | Sync files over SSH | `rsync -e "ssh -i key.pem" -avc src/ dest/` |

---

## ✅ Networking Commands

Commands for testing and managing networks.

### Installing ping: The ping utility is typically part of the iputils-ping package. To install it on Ubuntu, execute the following commands in a terminal:
```bash
sudo apt update
sudo apt install iputils-ping -y
```

### Installing netstat: The netstat utility is part of the net-tools package. To install it on Ubuntu, execute the following commands in a terminal:
```
sudo apt update
sudo apt install net-tools -y
``` 

| Command | Description | Example |
|------|--------------|--------|
| `ping site` | Test network connection | `ping google.com` |
| `netstat` | Show network stats | `netstat -tuln` |
| `ifconfig` | Show network interfaces | `ifconfig` |
| `traceroute` | Trace path to host | `traceroute google.com` |
| `tracepath` | Trace path without root | `tracepath google.com` |
| `mtr` | Interactive trace route | `mtr google.com` |
| `nslookup` | DNS lookup | `nslookup google.com` |
| `telnet` | Test port connection | `telnet example.com 80` |
| `ip` | IP configuration | `ip addr` |
| `iwconfig` | Wireless settings | `iwconfig` |
| `ss` | Show sockets | `ss -tuln` |
| `dig` | Detailed DNS query | `dig example.com` |
| `whois` | Domain info lookup | `whois example.com` |
| `ifplugstatus` | Show network cable status | `ifplugstatus eth0` |
| `curl` | Transfer data via URL | `curl http://example.com` |
| `wget` | Download files | `wget http://example.com/file` |
| `iptables` | Configure firewall | `sudo iptables -L` |
| `watch` | Run command repeatedly | `watch ls -l` |
| `arp` | Show MAC addresses | `arp -a` |
| `route` | Show routing table | `route -n` |
| `awk '' filename` | Pattern scanning and processing | `awk '{print $1}' file.txt` |

---

## ✅ Editors

| Command | Description | Example |
|------|--------------|--------|
| `vi` | Simple text editor | `vi file.txt` |
| `vim` | Enhanced editor with more features | `vim file.txt` |

---

## ✅ Additional Notes

✔ This file includes commands from navigation, file handling, disk usage, user management, networking, compression, processes, and remote access.

✔ Commands like `chmod`, `chown`, `iptables`, and `sudo` require root privileges.

✔ `ssh`, `scp`, and `rsync` are essential for managing servers remotely.

✔ `awk`, `curl`, `wget`, and `nslookup` are versatile tools for scripting and automation.

✔ Always be cautious when using commands like `rm -r`, `chmod 777`, and `userdel`, as they can alter or delete critical files and users.
