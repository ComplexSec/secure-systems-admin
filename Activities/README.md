# Secure Systems Administration - Activities

## Try and solve the labs without looking at the solutions. If you get stuck, the solutions are available

NB. The `desktopX` machine is referred to as the `Desktop1` machine on NetLab - both have student users

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

<details><summary>Module 2 - Lab 2 (Managing Files with Shell Expansion)</summary>
<p>

## Step 1 - Create files called `tv_seasonX_episodeY.ogg` and replace X with season number and Y with episode number - two seasons of six episodes each

<details><summary>Solution</summary>
<p>
	
Simply use the `touch` command

![](/images/touch2.png)

</p>
</details>

## Step 2 - Create eight files with names `mystery_chapterX.odf` and replace X with numbers 1 through 8

<details><summary>Solution</summary>
<p>
	
Using the same command as above - `touch` - create 8 mystery chapters

![](/images/8files.png)
	
</p>
</details>

## Step 3 - Create two directories named `season1` and `season2` under the Videos directory

<details><summary>Solution</summary>
<p>
	
Simply use the `mkdir` command

![](/images/seasons.png)
	
</p>
</details>

## Step 4 - Move the appropriate TV episodes into the season subdirectories using two commands only

<details><summary>Solution</summary>
<p>
	
Using the `mv` command and the asterisk, simply move them to their respsective folders

![](/images/moved.png)
	
</p>
</details>

## Step 5 - Create two level directory hierarchy with one command. Create `my_bestseller` under the Documents directory and `chapters` beneath the new `my_bestseller` directory

<details><summary>Solution</summary>
<p>
	
Use the `mkdir` command once again and create the directories with the `-p` option to create the parents

![](/images/chapters.png)

</p>
</details>

## Step 6 - Using one command, create 3 more subdirectories directly under `my_bestseller` directory. Name these `editor`, `plot_change` and `vacation`

<details><summary>Solution</summary>
<p>
	
Use the `mkdir` command and create the directories. You do not need the -p option this time as the parent directory already exists

![](/images/three.png)

</p>
</details>

## Step 7 - Change to chapters directory. Move all book chapters into the `chapters` directory using the simplest syntax

<details><summary>Solution</summary>
<p>
	
Use the `cd` command and the `mv` command to move the chapters to the current directory using the `.` symbol

![](/images/mystery.png)
	
</p>
</details>

## Step 8 - Move the first two chapters to the `editor` directory using relative syntax

<details><summary>Solution</summary>
<p>
	
Simply use the `mv` command and relative pathing to move it to the upper directory and the editor directory

![](/images/editor.png)
	
</p>
</details>

## Step 9 - Move chapters 8 and 9 to the vacation folder using one command without wildcard characters

<details><summary>Solution</summary>
<p>
	
Copy the same command as above but simply change names and directories

![](/images/vacation.png)
	
</p>
</details>

## Step 10 - With one command, change directory to season 2 TV episodes location, then copy the first episode to the vacation directory

<details><summary>Solution</summary>
<p>
	
Use the `cd` command to move into the directory `~/Videos/season2` and use the `cp` command to copy the first episode of season 2 into the vacation directory

![](/images/season2.png)
	
</p>
</details>

## Step 11 - With one command, change the working directory to `vacation` then list files. Return to the season 2 directory using the `previous working directory` shortcut. Copy the episode 2 file into `vacation`. Return to `vacation` using the shortcut again

<details><summary>Solution</summary>
<p>
	
Use the `cd`, `cp` commands to carry out this task

![](/images/prev.png)
	
</p>
</details>

## Step 12 - Copy chapters 5 and 6 into `plot_change` then move up one directory to `vacation` parent directory then use one command from there

<details><summary>Solution</summary>
<p>
	
Simply use the `cp` command with the `[]` operators to move 5 and 6 at the same time

![](/images/plot.png)
	
</p>
</details>

## Step 13 - Make three backups of chapter 5. Move to `plot_change` directory and copy chapter5 as a new file name to include the full date. Make another copy appending the current timestamp to ensure a unique file name. Also make a copy appending the current user to the file name

<details><summary>Solution</summary>
<p>
	
Simply use the `cp` command to make backups and use the `date` command to add the dates at the end with various modifiers and the `$USER` variable to add the username

![](/images/dates.png)
	
</p>
</details>

## Step 14 - Delete the `plot_change` directory by first deleting all of the files inside and removing it by first trying the rm command and then the rmdir command

<details><summary>Solution</summary>
<p>
	
Use the `rm` command with asterisk to delete all files inside plot change
	
![](/images/plotchange.png)

</p>
</details>

## Step 15 - Delete the `vacation` directory using the rm command with the recursive option then return to home directory

<details><summary>Solution</summary>
<p>
	
Use the `rm -r` command to recursive delete the vacation folder and all files inside

![](/images/vac.png)
	
</p>
</details>

</p>
</details>

<details><summary>Module 3 - Lab 1 (Finding Relevant Information Using Man)</summary>
<p>
	
## Step 1 - View the gedit(1) man page

<details><summary>Solution</summary>
<p>
	
Simply type `man 1 gedit` to open the relevant man page 

![](/images/man1.png)

</p>
</details>

## Step 2 - Research how to edit a specific file using gedit

<details><summary>Solution</summary>
<p>
	
Simply look through the gedit man page and you will find it

![](/images/filename.png)
	
</p>
</details>

## Step 3 - Research the gedit option used to begin an editing session with the cursor at the end

<details><summary>Solution</summary>
<p>
	
Again, look through the man page and you will find the relevant option

![](/images/line.png)
	
</p>
</details>

## Step 4 - Research the su(1) man page

<details><summary>Solution</summary>
<p>
	
Simply use the same command we did for gedit using the 1 option

![](/images/mansu.png)
	
</p>
</details>

## Step 5 - Research what su does when username argument is omitted

<details><summary>Solution</summary>
<p>
	
You will find this answer by reading the man page
	
![](/images/su2.png)

</p>
</details>

## Step 6 - Research how su behaves when a single dash option is used

<details><summary>Solution</summary>
<p>
	
![](/images/root.png)
	
</p>
</details>

## Step 7 - Consult the passwd(1) man page and determine the options that lock and unlock an account

<details><summary>Solution</summary>
<p>
	
Simply open the man page and look through it

![](/images/lock.png)
	
</p>
</details>

## Step 8 - Locate the two principles to remember according to passwd man page

<details><summary>Solution</summary>
<p>
	
Using the `/principle` command inside the man page, we find the two principles via the string search

![](/images/princ.png)

</p>
</details>

## Step 9 - Consult the man page documenting the syntax of the /etc/passwd file and find out what the third field means

<details><summary>Solution</summary>
<p>
	
To see the syntax documenting the syntax of passwd file instead of the passwd command, we use section 5 when searching for passwd

![](/images/sec5.png)
	
</p>
</details>

## Step 10 - Which command will list detailed information about a zip archive?

<details><summary>Solution</summary>
<p>
	
Using the `man -k zip` command, we can see man pages relating to zips

![](/images/zipinfo.png)
	
</p>
</details>

## Step 11 - Which man page contains a list of parameters that can be pased to the kernel at boot?

<details><summary>Solution</summary>
<p>
	
Again, using the `man -k` command, we can search for the keyword of boot

![](/images/boot.png)
	
</p>
</details>

## Step 12 - Which command is used to tune ext4 file system parameters?

<details><summary>Solution</summary>
<p>
	
Finally, for the third time, use the `man -k` command with the keyword ext4

![](/images/tune2fs.png)
	
</p>
</details>

</p>
</details>

<details><summary>Module 3 - Lab 2 (Understanding Program Documentation)</summary>
<p>
	
## Step 1 - Invoke __pinfo__ without arguments

<details><summary>Solution</summary>
<p>

Simply type `pinfo` into the CLI
	
![](/images/pinfo.png)

</p>
</details>

## Step 2 - Navigate to the __Common Options__ topic

<details><summary>Solution</summary>
<p>
	
Use the Down Arrow to move to Common Options - it will be highlighted red. Once there, hit Enter

![](/images/common.png)

</p>
</details>

## Step 3 - Browse through this __Info__ topic and learn if long-style options can be abbreviated

<details><summary>Solution</summary>
<p>
	
Read through the documentation and you will find it.

![](/images/common.png)

</p>
</details>

## Step 4 - Determine what the symbols `--` signify when used as an argument

<details><summary>Solution</summary>
<p>
	
The symbols signify the end of command options and the start of command arguments in complex commands

![](/images/--.png)

</p>
</details>

## Step 5 - Without exiting __pinfo__ move up to the GNU Coreutils node

<details><summary>Solution</summary>
<p>
	
To go up one node, use the `u` character inside of pinfo

![](/images/u.png)

</p>
</details>

## Step 6 - Move up again to the top topic

<details><summary>Solution</summary>
<p>
	
Once again, hit the `u` character

![](/images/u2.png)

</p>
</details>

## Step 7 - Search for the pattern __nano__ and select that topic

<details><summary>Solution</summary>
<p>
	
To search simply hit `/` followed directly by your string and hit Enter

![](/images/nano.png)

</p>
</details>

## Step 8 - In the Introduction locate and select Command Line Options and browse the topic

<details><summary>Solution</summary>
<p>
	
It is located under Nano -> Introduction -> Command Line Options

![](/images/clop.png)

</p>
</details>

## Step 9 - Move up one level to return to Introduction and move to the next topic

<details><summary>Solution</summary>
<p>
	
Once read, hit `u` once again to back up one topic and then hit `n`. The new location will be in Editor Basics under nano

![](/images/un.png)

</p>
</details>

## Step 10 - Exit __pinfo__

<details><summary>Solution</summary>
<p>
	
Simply press `q` to quit pinfo

</p>
</details>

## Step 11 - Invoke __pinfo__ again specifying nano as the destination topic

<details><summary>Solution</summary>
<p>
	
Simply type `pinfo nano` to open directly up to the nano topic

![](/images/pnano.png)

</p>
</details>

## Step 12 - Select the Editor Basics topic

<details><summary>Solution</summary>
<p>
	
Use arrow keys to select the Editor Basics

![](/images/edbas.png)

</p>
</details>

## Step 13 - Read the Entering Text and Special Functions subtopics

<details><summary>Solution</summary>
<p>
	
Press n to move to the next topic directly instead of going up one node and then back

![](/images/specfunc.png)

</p>
</details>

</p>
</details>