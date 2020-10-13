# Secure Systems Administration - Activities

## Try and solve the labs without looking at the solutions. If you get stuck, the solutions are available

NB. The `desktopX` machine is referred to as the `Workstation` machine on NetLab - both have student users

Once done, click [here](https://github.com/ComplexSec/secure-systems-admin) to go back to the notes section

<details><summary>Module 1 - Lab 1 (Changing Password)</summary>
<p>

### Step 1: Change the password for student to 55TurnK3y 

<details><summary>Solution</summary>
<p>
	
Done via the `passwd` command when either SSH'd into the workstation or via the GUI accessed via `Activities --> Education` and selecting the workstation VM

![](/images/passwd.png)

You should now be able to log out and back in via the "55TurnK3y" password

</p>
</details>

</p>
</details>

<details><summary>Module 1 - Lab 2 (Using Commands)</summary>
<p>
	
### Step 1 - Change student's password to T3st1ngT1me

<details><summary>Solution</summary>
<p>
	
Done via the `passwd` command when logged in as student. Simply type the old password and then the new password twice

![](/images/passwd2.png)

</p>
</details>

### Step 2 - Show current date and time

<details><summary>Solution</summary>
<p>
	
Simply type the `date` command into the terminal	

![](/images/date2.png)

</p>
</details>

### Step 3 - Display current time in the following format HH:MM:SS A/PM

<details><summary>Solution</summary>
<p>
	
Use the previous command - __date__ - with the %r argument

![](/images/date3.png)

</p>
</details>

### Step 4 - Identify what kind of file /usr/bin/clean-binary-files is

<details><summary>Solution</summary>
<p>
	
There is a problem with this one. Instead of running this task on the workstation VM, exit back out to the `Foundation 0` PC and you will identify the file exists

To identify what type of file it is, simply use the `file` command along with the file you want to identify

![](/images/foundation.png)

</p>
</details>

### Step 5 - Use the wc command and bash shortcuts to display the size of /usr/bin/clean-binary-files

<details><summary>Solution</summary>
<p>
	
Simply use the `wc` command on the file specified. If the previous command has been typed, you can shorten this to using the `Esc+.` shortcut to print the last string of the last command

![](/images/binary.png)

</p>
</details>

### Step 6 - Display the first 10 lines of /usr/bin/clean-binary-files

<details><summary>Solution</summary>
<p>
	
Use the `head` command to display the first 10 lines of a file by default - no need to specify via the `-n` argument

![](/images/first.png)

</p>
</details>

### Step 7 - Display the last 10 lines at the bottom of /usr/bin/clean-binary-files

<details><summary>Solution</summary>
<p>
	
Use the `tail` command to display the last 10 lines of a file by default - no specification needed

![](/images/last.png)

</p>
</details>

### Step 8 - Repeat the previous command but use the `-n 20` option to display the last 20 lines in the file

<details><summary>Solution</summary>
<p>
	
Use the Up Arrow to use the previous command and simply add the `-n 20` option

![](/images/20.png)

</p>
</details>

### Step 9 - Execute the date command without any arguments to display current date and time

<details><summary>Solution</summary>
<p>
	
Simply type `date` into the command line

![](/images/date4.png)

</p>
</details>

### Step 10 - Use bash history to display just the time

<details><summary>Solution</summary>
<p>
	
![](/images/41.png)

</p>
</details>

### Step 11 - Finish the BASH session

<details><summary>Solution</summary>
<p>
	
Simply type `exit` into the shell to exit both the SSH connection and the normal terminal

![](/images/exit.png)

</p>
</details>

</p>
</details>

<details><summary>Module 2 - Lab 1 (File Management)</summary>
<p>
	
## Step 1 - Creat sets of empty files (song1-6.mp3, snap1-6.jpg & film1-6.avi)

<details><summary>Solution</summary>
<p>
	
Simply use the touch command to create all mp3, jpg and avi files in the home directory - using three commands

![](/images/touch.png)

</p>
</details>

## Step 2 - Move songs into Music, snaps into Pictures and films into Videos

<details><summary>Solution</summary>
<p>
	
Simply use the `mv` command with the * after song, snap and film to move all correpsonding files into their respective directory

![](/images/mv.png)

</p>
</details>

## Step 3 - Make three directories (friends, family, work) in your home directory

<details><summary>Solution</summary>
<p>
	
Simply use the `mkdir` command along with the directory names

![](/images/friends.png)

</p>
</details>

## Step 4 - Copy all files containing numbers 1 and 2 to friends folder and all files containing 3 and 4 to the family folder

<details><summary>Solution</summary>
<p>
	
Simply use the `cp` command along with first, the files you want to copy and lastly their destination

![](/images/family.png)

</p>
</details>

## Step 5 - Copy all files containing numbers 5 and 6 to work folder

<details><summary>Solution</summary>
<p>
	
Do the previous command but change it to 5 and 6 and the destination to `~/work`

![](/images/work.png)

</p>
</details>
	
## Step 6 - Attempt to remove the `family` and `friends` directories via `rmdir`

<details><summary>Solution</summary>
<p>
	
Try and remove the directories using the `rmdir family/ friends/` command and you will get an error as they are not empty directories

![](/images/rmdir.png)

</p>
</details>

## step 7 - Use another command that succeeds in deleting the folders

<details><summary>Solution</summary>
<p>
	
To successfully delete directories that contain files, use the `rm -r` command followed by the directories you want to delete

![](/images/delete.png)

</p>
</details>

## Step 8 - Delete all files in work project, but but do not delete the directory

<details><summary>Solution</summary>
<p>
	
Use the `rm ~/work/*` command to delete all files in the work directory

![](/images/work2.png)

</p>
</details>

## Step 9 - From home directory, use the `rmdir` command to delete the work directory

<details><summary>Solution</summary>
<p>
	
Simply use the `rmdir` command on the work directory

![](/images/rmdirwork.png)

</p>
</details>

</p>
</details>