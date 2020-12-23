# A list of useful commands for Linux Administrators and Red Hat Enterprise Linux

<details><summary>General Syntax</summary>
<p>
	
Syntax | Description
------------ | -------------
$() | syntax that allows command substitution
* | matches any string of 0 or more characters
? | matches any single character
~ | current user's home directory
~username | matches user home directory
~+ | matches current working directory
~- | matches the previous working directory
[abc...] | matches any one character in the enclosed class
[!abc...] | matches any one character not in the enclosed class
[^abc...] | matches any one character not in the enclosed class
[[:alpha:]] | matches any alphabetic character
[[:lower:]] | matches any lower-case character
[[:upper:]] | matches any upper-case character
[[:alnum:]] | matches any alphabetic character or digit
[[:punct:]] | matches any printable character not a space or alphanumeric
[[:digit:]] | matches any digit
[[:space:]] | matches any one whitespace character
& | starts process in background 
Ctrl+Z | suspends job running in foreground
Ctrl+C | terminates job running in foreground
Ctrl+\ | quit key combination

</p>
</details>

<details><summary>Beginning with A</summary>
<p>
	
Syntax | Description
------------ | -------------
authconfig --passalgo <md5/sha512/sha256> | change default password hashing algorithm

</p>
</details>

<details><summary>Beginning with B</summary>
<p>
	
Syntax | Description
------------ | -------------
bg % <number> | allow suspended background process to start running
blkid | overview of existing partitions with a file system on them and UUID of file system

</p>
</details>

<details><summary>Beginning with C</summary>
<p>
	
Syntax | Description
------------ | -------------
cat | displays content of file in CLI
cd <dir> | change directory
cd | return to the current user's home directory
cd ~ | change to user's home directory
cd . | stay in current directory
cd .. | change to parent directory
cd ../.. | move up two levels 
cd - | change to previous working directory
chage -d username | last change date for password
chage -d 0 username | force password update on login
chage -l username | list username current settings
chage -E YYYY-MM-DD username | expire an account on specific day
chage -m digit username | minimum age for password
chage -M digit username | maximum age for password
chage -W digit username | set warning for when password must be changed
chage -I digit username | set inactive days
chmod <whowhatwhich> <file/directory> | change perms (u,g,o,a), (+,-,=), (r,w,x)
chmod ### <file/directory> | change perms (r=4, w=2, x=1)
chmod -R | sets permissions on files in entire directory
chmod g+s | add setgid bit
chmod u+s | add setuid bit
chmod o+t | add sticky bit
chmod 2770 <dir> | add setgid bit and rwx for user/group
chown <user> <file> | change file ownership
chown -R <user>> <dir> | recursively change ownership of directory
chown :group <dir> change group ownership 
chown owner:group <dir> | change both owner and group at same time
chronyc | acts as client to the chronyd service
chronyc sources | verify NTP server was used to sync system clock
chronyc sources -v | verbose output 
cp | copy file
cp file1 file2 | copies file1 as file2
cp file1 file2 <dir> | copies both files to directory
cp -r | copies directory

</p>
</details>