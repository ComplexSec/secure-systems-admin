# A list of useful commands for Linux Administrators and Red Hat Enterprise Linux

<details><summary>General Syntax</summary>
<p>
	
Syntax | Description
------------ | -------------
`$()` | syntax that allows command substitution
`*` | matches any string of 0 or more characters
`?` | matches any single character
`~` | current user's home directory
`~username` | matches user home directory
`~+` | matches current working directory
`~-` | matches the previous working directory
`[abc...]` | matches any one character in the enclosed class
`[!abc...]` | matches any one character not in the enclosed class
`[^abc...]`| matches any one character not in the enclosed class
`[[:alpha:]]` | matches any alphabetic character
`[[:lower:]]` | matches any lower-case character
`[[:upper:]]` | matches any upper-case character
`[[:alnum:]]` | matches any alphabetic character or digit
`[[:punct:]]` | matches any printable character not a space or alphanumeric
`[[:digit:]]` | matches any digit
`[[:space:]]` | matches any one whitespace character
`&` | starts process in background 
`Ctrl+Z` | suspends job running in foreground
`Ctrl+C` | terminates job running in foreground
`Ctrl+\` | quit key combination

</p>
</details>

<details><summary>Beginning with A</summary>
<p>
	
Syntax | Description
------------ | -------------
`authconfig --passalgo <md5/sha512/sha256>` | change default password hashing algorithm

</p>
</details>

<details><summary>Beginning with B</summary>
<p>
	
Syntax | Description
------------ | -------------
`bg % <number>`| allow suspended background process to start running
`blkid`| overview of existing partitions with a file system on them and UUID of file system

</p>
</details>

<details><summary>Beginning with C</summary>
<p>
	
Syntax | Description
------------ | -------------
`cat` | displays content of file in CLI
`cd <dir>` | change directory
`cd` | return to the current user's home directory
`cd ~` | change to user's home directory
`cd .` | stay in current directory
`cd ..` | change to parent directory
`cd ../..` | move up two levels 
`cd -` | change to previous working directory
`chage -d username` | last change date for password
`chage -d 0 username` | force password update on login
`chage -l username` | list username current settings
`chage -E YYYY-MM-DD username` | expire an account on specific day
`chage -m digit username` | minimum age for password
`chage -M digit username` | maximum age for password
`chage -W digit username` | set warning for when password must be changed
`chage -I digit username` | set inactive days
`chmod <whowhatwhich> <file/directory>` | change perms (u,g,o,a), (+,-,=), (r,w,x)
`chmod ### <file/directory>` | change perms (r=4, w=2, x=1)
`chmod -R` | sets permissions on files in entire directory
`chmod g+s` | add setgid bit
`chmod u+s` | add setuid bit
`chmod o+t` | add sticky bit
`chmod 2770 <dir>` | add setgid bit and rwx for user/group
`chown <user> <file>` | change file ownership
`chown -R <user>> <dir>` | recursively change ownership of directory
`chown :group <dir>` | change group ownership 
`chown owner:group <dir>` | change both owner and group at same time
`chronyc` | acts as client to the chronyd service
`chronyc sources` | verify NTP server was used to sync system clock
`chronyc sources -v` | verbose output 
`cp` | copy file
`cp file1 file2` | copies file1 as file2
`cp file1 file2 <dir>` | copies both files to directory
`cp -r` | copies directory

</p>
</details>

<details><summary>Beginning with D</summary>
<p>
	
Syntax | Description
------------ | -------------
`date` | display current date and time
`date` | used by root to set system clock
`date +%R` | display current time
`date +%x` | display current date
`date +%M` | displays the minutes 
`date +%p` | dispalys am or pm
`date +%l` | displays the hour
`date +%r` | displays time in HH:MM:SS A/PM format
`date +%A` | displays day of the week
`date +%Y` | displays year
`date +%B` | displays month
`date +%d` | displays day of month
`date +%A”, “%B”, “%d”, “%Y"` | displays date like Wednesday, December 23, 2020
`date -d "+45 days"` | calculates the date 45 days into the future
`df` | reports total disk space, used disk space and free disk space
`df -h/-H` | displays human readable outputs
`du /root` | show disk usage for the /root directory
`0du -h /var/log` | show disk usage report in human readable format for /var/log

</p>
</details>

<details><summary>Beginning with E</summary>
<p>

Syntax | Description
------------ | -------------
`echo` | prints string to the screen

</p>
</details>

<details><summary>Beginning with F</summary>
<p>
	
Syntax | Description
------------ | -------------
`fg % <jobnumber>` | takes background process and runs it in foreground
`file` | scans beginning of file and displays what type it is
`find` | searches file system in real time

</p>
</details>


<details><summary>Beginning with G</summary>
<p>
	
Syntax | Description
------------ | -------------
`gedit` | text editor
`gedit <file>` | edit specific file
`gedit + <file>` | begin editing session at end of file 
`gedit <file> &` | allow shell prompt to return while gedit running
`getent hosts <hostname>` | test host name resolution with /etc/hosts file
`grep "model name" /proc/cpuinfo (pipe) wc -l` | determine number of logical CPUs
`groupadd <name>` | uses next available GID from range specified in /etc/login.defs
`groupadd -g GID` | specifies GID
`groupadd -r` | create system group using GID from range of valid system GID 
`groupdel` | remove group
`groupmod` | change a group name to a GID mapping
`groupmod -n` | specify a new name
`groupmod -g` | specify a new GID

</p>
</details>

<details><summary>Beginning with H</summary>
<p>
	
Syntax | Description
------------ | -------------
`head` | dispalys beginning of a file (10 lines by default)
`history` | display list of previous executed command 
`host <hostname>` | test DNS server connectivity
`hostname` | display hostname
`hostnamectl` | used to modify the /etc/hostname file
`hostnamectl set-hostname desktopX.example.com` | modifies hostname
`hostnamectl status` | view status of system's fully qualified host name

</p>
</details>

<details><summary>Beginning with I</summary>
<p>
	
Syntax | Description
------------ | -------------
`id -` | show info about current user
`id <username>` | show info about a user
`ip addr show` | review IP address settings
`ip addr show <interface>` | review IP address settings for specific interface
`ip -s link show <interface>` | show IP stats
`ip route` | display IP routing table

</p>
</details>

<details><summary>Beginning with J</summary>
<p>
	
Syntax | Description
------------ | -------------
`jobs` | display table of jobs per session 
`journalctl` | shows full system journal, starting with oldest log entry
`journalctl -n <number>` | specify number of log entries
`journalctl -p err` | filter output to only list any priority err or above
`journalctl -f` | output last 10 lines of journal
`journalctl --since today` | output all journal entries today
`journalctl --since "2014-02-10 20:30:00" -- until "2014-02-13 12:00:00"` | output journal entries from a date to another date
`journalctl -o verbose` | turn on verbose output
`journalctl _SYSTEM_UNIT=sshd.service _PID=1182` | show journal entries related to processes started by systemd unit file sshd.service which also have PID of 1182
`journalctl _PID=1` | output only systemd journal messages that originate from the systemd process with PID of 1
`journalctl _UID=81` | display all systemd journal messages that originate from the system service started with UID of 81
`journalctl -p warning` | output journal messages with prioirity warning and above
`journalctl | head <-number>` | display specified number of lines at top of journal
`journalctl -b` | reduce output by only showing log messages since last boot
`journalctl -b -1` | limit journal query to previous reboot

</p>
</details>

<details><summary>Beginning with K</summary>
<p>

Syntax | Description
------------ | -------------
`kill <PID>` | kill process by PID
`kill -signal %PID` | kill process by PID
`kill -l -` | lists signals
`killall <command_pattern>` | send a signal to one/more processes matching selection criteria such as command name, processes owned by user, or all system-wide processes
`killall -signal <command_pattern>` | command name criteria
`killall -signal -u <-username> <command_pattern>` | username criteria
`killall -USR1 systemd-journald` | send special signal USR1 as root to systemd-journald process when making journal persistent

</p>
</details>

<details><summary>Beginning with L</summary>
<p>
	
Syntax | Description
------------ | -------------
`ln` | copies and renames files
`locate` | searches database for filenames/file paths
`locate passwd` | searches for files with "passwd" in name or path
`locate -i` | performs case insensitive search
`locate -n` | limits the number of returned search results by locate
`logger` | can send messages to rsyslog service
`logger -p local7.notice "Log entry created on serverX"` | sends message to rsyslogd that gets recorded in /var/log/boot.log
`ln` | creates hard links between files
`ln /usr/share/doc/qemu-kvm/qmp-commands.txt /root/qmp-manual.txt` | creates hard link and links it to the qmp-commands.txt file
`ln -s` | creates soft links between files
`ln -s /tmp /root/tempdir` | creates soft link pointing to /tmp
`ls` | list directory contents
`ls -l` | displays in long-listing format
`ls -a` | displays all files including hidden files
`ls -la` | displays all files in long format
`ls -R` | recursive, includes all subdirectories
`ls -lR` | displays content of all subdirectories in long format
`ls -l ~` | list current user's home directory in long format
`ls -ld dir` | show expanded listing of all files inside directory
`lsof` | list all open files and process accessing them in provided directory

</p>
</details>

<details><summary>Beginning with M</summary>
<p>
	
Syntax | Description
------------ | -------------
`man` | manual command
`man topic` | display topic contents one screen at a time
`man topic` | displays topic(1) by default
`man 5 topic` | displays section5
`man -k keyword` | search man page by keyword
`man -K keyword` | performs full text page search not just titles and descriptions
`mkdir` | create directory
`mkdir -p` | creates subdirectory in existing parent directory
`mount` | mount a file
`mount /dev/vdb1 /mnt/mydata` | mount by device file of the partition that holds the file system
`mount UUID=”46f543fd-78c9-4526-a857-244811be2d88” /mnt/mydata` | mount file system by universal unique ID
`mv` | moves/renames files
`mv file1 file2` | renames file1 to file2
`mv file1 dir` | moves file1 to directory
`mv dir1 dir2` | if dir2 exists, results in a move

</p>
</details>

<details><summary>Beginning with N</summary>
<p>
	
Syntax | Description
------------ | -------------
`nmcli con show` | display list of all connections 
`nmcli con show --active` | display list of active connections
`nmcli con show "connection name"` | specify a connection ID to see details
`nmcli con up ID` | activate a connection
`nmcli con down ID` | deactivate a connection
`nmcli dev dis device` | bring down an interface and disable auto connect
`nmcli net off` | disabled all managed interfaces
`nmcli dev status` | show device status
`nmcli dev show interface` | show device details
`nmcli con add con-name "default" type ethernet ifname eth0` | define a new connection named default which autoconnects as Ethernet connection on eth0 device using DHCP
`nmcli con add con-name “static” ifname eth0 autoconnect no type ethernet ip4 172.25.X.10/24 gw4 172.25.X.254` | create new connection named static and specify IP address and gateway
`nmcli con up “static”` | change to the static connection
`nmcli con up “default"` | change to the default connection
`nmcli dev disconnect devicename` | administratively disable an interface and prevent any autoconnection
`nmcli con add help` | useful for usage
`nmcli con mod “static” connection.autoconnect no` | turn off autoconnect
`nmcli con mod “static” connection.autoconnect yes` | turn on autoconnect
`nmcli con mod “static” ipv4.dns 172.25.X.254` | specify a DNS server
`nmcli con mod “static” +ipv4.dns 8.8.8.8` | add a secondary DNS server
`nmcli con mod “static” ipv4.addresses “172.25.X.10/24 172.25.X.254”`  | set IP address
`nmcli con del ID` | delete connection
`nmcli con mod ID ipv4.dns IP` | default behaviour is to replace any previous DNS settings with new IP provided

</p>
</details>

<details><summary>Beginning with P</summary>
<p>
	
Syntax | Description
------------ | -------------
`passwd` | change password
`passwd -d <username>` | delete password
`passwd -e <username>` | expires password & force reset
`passwd -l <username>` | lock user
`passwd -u <username>` | unlock user
`passwd -n <username> DAYS` | set minimum password lifetime
`passwd -x <username> DAYS` | set maximum password lifetime
`passwd -w <username> DAYS` | sets number of days in advanced to notify user of expire
`passwd -S <username>` | display information about account status
`pinfo <topic>` | brings up pinfo page of topic
`ping <host>` | check connectivity
`ping -c <number> <host>` | ping specified number of times
`pgrep -l -u <user>` | list running procecss for user
`pkill -u <user>` | kill everything a user is running
`pkill -t <terminal-device>` | kill everything running in window
`pkill -P` | tell parent to kill children
`pkill command_pattern` | kill processes with a pattern-matched command name
`pkill -signal command_pattern` | send signal to all process with pattern match
`pkill -G GID command_pattern` | kill all processes owned by a group
`pkill -P PPID command_pattern` | kill all child provesses of parent PPID
`pkill -t terminal-name -U UID command_pattern` | kill all processes on terminal for user ID
`pkill -SIGKILL -u username` | kill all processes for a user
`pkill -SIGKILL -t terminal-name` | kill all processes on a terminal 
`pkill -SIGKILL -P PPID` | kills all child processes of parent PPID
`pkill -SIGSTOP process` | suspends process
`pkill -SIGCONT process` | resumes suspended process
`pkill -SIGTERM process` | terminates process
`ps` | lists processes with same effective UID as user
`ps -f` | return full process listing
`ps a` | returns all processes with a terminal
`ps u` | view user associated with process
`ps aux` | displays all processes with columns
`ps lax` | displays processes in more technical detail 
`ps -ef` | displays all processes
`ps -o OR ps --sort` | lists processes in chronological order
`ps j` | display information relating to jobs
`pstree -p <user>` | show processes in tree format for user
`ps -f $(pgrep process-name)` | list process information of specific process
`ps -up PID` | verify that process is running 
`pwd` | display full path name of current location

</p>
</details>

<details><summary>Beginning with R</summary>
<p>
	
Syntax | Description
------------ | -------------
rm
rm -i
rm -r
rm -rf
rm -ri
rm -f
rmdir
rpm
rpm -q
rpm -q -a
rpm -q PACKAGENAME
rpm -q -p PACKAGEFILE
rpm -q -f FILENAME
rpm -q -p PACKAGE -l 
rpm -q -c
rpm -q -d
rpm -q --scripts
rpm -q -p PACKAGE -i
rpm -q -p PACKAGE --scripts 
rpm -q --changelog
rpm -ivh PACKAGEFILE.rpm
repoquery 
rsync 
rsync -n
rsync -v
rsync -a
rsync -H
rsync -aA
rsync -aX

</p>
</details>

<details><summary>Beginning with S</summary>
<p>
	

	
</p>
</details>