# linux-administration-Commands-Cheat-Sheet
linux administration Commands Cheat Sheet
Here’s a Linux Administration Commands Cheat Sheet to help you with the most commonly used commands for system administration tasks in a Linux environment.

1. System Information
Display system information (OS, kernel, architecture, etc.):

 bash

uname -a

Display detailed information about the system:

 bash

uname -r

Display OS version:

 bash

cat /etc/os-release

Display system uptime and load averages:

 bash

Uptime

Display the kernel version:

 bash

uname -s

Show all logged-in users:

 bash

who

Show users currently logged into the system:

 bash

w

2. User and Group Management
Add a new user:

 bash

sudo useradd USERNAME

Set password for a user:

 bash

sudo passwd USERNAME

Delete a user:

 bash

sudo userdel USERNAME

Add a new group:

 bash

sudo groupadd GROUPNAME

Add a user to a group:

 bash

sudo usermod -aG GROUPNAME USERNAME

Display group memberships for a user:

 bash

groups USERNAME
Display user information:

 bash

id USERNAME

List all users:

 bash

cat /etc/passwd

3. File and Directory Management
Create a new directory:

 bash

mkdir DIRECTORY_NAME

Remove a directory:

 bash

rmdir DIRECTORY_NAME

Change the current directory:

 bash

cd DIRECTORY_NAME

List files and directories:

 bash

Ls

List all files (including hidden files):

 bash

ls -a

Show detailed information about files:

 bash

ls -l

Copy a file:

 bash

cp SOURCE_FILE DESTINATION

Move or rename a file:

 bash

mv SOURCE_FILE DESTINATION

Remove a file:

 bash

rm FILE_NAME

Change file permissions:

 bash

chmod PERMISSIONS FILE_NAME

Change file owner:

 bash

chown USERNAME:GROUPNAME FILE_NAME

Change file group:

 bash

chgrp GROUPNAME FILE_NAME


4. Process Management
List running processes:

 bash

ps aux

Show process tree:

 bash

Pstree

Search for a process by name:

 bash

ps aux | grep PROCESS_NAME

Display system resource usage (CPU, memory):

 bash

Top

View real-time system resource usage:

 bash

htop  # Install 'htop' if it's not available
Kill a process by PID:

 bash

kill PID

Force kill a process:

 bash

kill -9 PID

List all open files by a specific process:

 bash

lsof -p PID


5. Disk Management
Display disk usage:

 bash

df -h

Display disk space usage by directories:

 bash

du -sh *

List all mounted file systems:

 bash

Mount

Check disk partitions:

 bash

fdisk -l

Create a new partition:

 bash

sudo fdisk /dev/sdX

Format a partition:

 bash

sudo mkfs.ext4 /dev/sdX1

Check disk for errors:

 bash

sudo fsck /dev/sdX1

Create a swap file:

 bash

sudo fallocate -l 1G /swapfile
sudo chmod 600 /swapfile
sudo mkswap /swapfile
sudo swapon /swapfile

6. Network Management
Display IP address and network configuration:

 bash

ip a

Display network interfaces:

 bash

Ifconfig

Ping a remote server to check connectivity:

 bash

ping SERVER_IP

Traceroute to check the network route:

 bash

traceroute SERVER_IP

Display network routing table:

 bash

Route

View open ports:

 bash

netstat -tuln

Display network connections:

 bash

netstat -tulnp

Test network speed:

 bash

speedtest-cli  # Requires 'speedtest-cli' to be installed

7. Package Management (Ubuntu/Debian)
Update package list:

 bash

sudo apt update

Upgrade all packages:

 bash

sudo apt upgrade

Install a package:

 bash

sudo apt install PACKAGE_NAME

Remove a package:

 bash

sudo apt remove PACKAGE_NAME

Search for a package:

 bash

apt search PACKAGE_NAME

Display information about a package:

 bash

apt show PACKAGE_NAME

8. System Monitoring and Logs
View system logs:

 bash

Journalctl

View system log (useful for debugging issues):

 bash

tail -f /var/log/syslog

View last system logins:

 bash

Last

Check system boot logs:

 bash

Dmesg

Monitor file changes in real-time:

 bash

inotifywait -m DIRECTORY_NAME  # Requires 'inotify-tools'

9. Backup and Restore
Create a tarball (backup) of a directory:

 bash

tar -czvf backup.tar.gz /path/to/directory

Extract a tarball:

 bash

tar -xzvf backup.tar.gz

Create a compressed backup using rsync:

 bash

rsync -avz /source/directory /backup/directory

Restore from a backup using rsync:

 bash

rsync -avz /backup/directory /restore/directory

10. System Services
Start a service:

 bash

sudo systemctl start SERVICE_NAME

Stop a service:

 bash

sudo systemctl stop SERVICE_NAME

Restart a service:

 bash

sudo systemctl restart SERVICE_NAME

Enable a service to start on boot:

 bash

sudo systemctl enable SERVICE_NAME

Disable a service from starting on boot:

 bash

sudo systemctl disable SERVICE_NAME

Check the status of a service:

 bash

sudo systemctl status SERVICE_NAME

Bonus: Useful Command Options
-h: Human-readable format (e.g., df -h for human-readable disk usage).


-r: Recursive option for copying or listing directories (cp -r).


-f: Force the operation (e.g., rm -f to force remove a file).



This cheat sheet should help you with most system administration tasks on a Linux machine.
