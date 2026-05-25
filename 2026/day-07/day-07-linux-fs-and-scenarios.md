Day 07 - Linux File System Practice

Today I learned about important Linux folders and some basic troubleshooting commands.


# Important Linux Directories

## /

This is the main root directory in Linux.

Command:

```bash
ls -l /
Used to see main system folders.

/home
Stores normal user files and folders.
Command:
Bash
ls -l /home
I use this to access user files.

/root
Home folder of root user.
Command:
Bash
ls -l /root
Used when working as admin user.

/etc
Contains system configuration files.

Command:
Bash
ls -l /etc
Used for checking config files.

/var/log
Stores system log files.

Command:
Bash
ls -l /var/log
Used for troubleshooting errors.

/tmp
Stores temporary files.

Command:
Bash
ls -l /tmp
Used for temporary practice files.

Practice Commands
Check large log files
Bash
du -sh /var/log/* 2>/dev/null | sort -h | tail -5
Shows large log files.
Check hostname

Bash
cat /etc/hostname
Shows system name.

Check home directory files
Bash
ls -la ~
Shows files in home folder.

Scenario Practice

Scenario 1 - Service Not Starting
Bash
systemctl status myapp
Checks service status.

Bash
journalctl -u myapp -n 50
Checks service logs.

Bash
systemctl is-enabled myapp
Checks if service starts automatically.
Scenario 2 - High CPU Usage

Bash
top
Shows live CPU usage.

Bash
ps aux --sort=-%cpu | head
Shows high CPU processes.
Scenario 3 - Service Logs

Bash
systemctl status ssh
Checks SSH service.

Bash
journalctl -u ssh -n 20
Shows recent SSH logs.
Scenario 4 - Permission Issue

Bash
ls -l backup.sh
Checks file permissions.

Bash
chmod +x backup.sh
Gives execute permission.
Bash
./backup.sh
Runs the script.

What I Learned

Linux folder basics
How to check logs
How to check services
Basic troubleshooting commands
#90DaysOfDevOps