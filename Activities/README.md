# Secure Systems Administration - Activities

## Try and solve the labs without looking at the solutions. If you get stuck, the solutions are available

NB. The `desktopX` machine is referred to as the `Desktop1` machine on NetLab - both have student users

Once done, click [here](https://github.com/ComplexSec/secure-systems-admin) to go back to the notes section

<details><summary>Module 1</summary>
<p>
	

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

</p>
</details>

<details><summary>Module 2</summary>
<p>
	

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

</p>
</details>

<details><summary>Module 3</summary>
<p>
	

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

<details><summary>Module 3 - Lab 3 (Research Documentation Under /usr/share/doc)</summary>
<p>
	
## Step 1 - Where can you find the latest news about the vim project?

<details><summary>Solution</summary>
<p>
	
Navigate to the `/usr/share/doc` directory and view the vim-common README

![](/images/vim.png)

</p>
</details>

## Step 2 - What is the wiki URI for the yum package?

<details><summary>Solution</summary>
<p>
	
It is located under yum-3.4.3 and is contained in a README file

![](/images/yum.png)

</p>
</details>

## Step 3 - What examples are provided for the command-line bc calculator?

<details><summary>Solution</summary>
<p>
	
Located in the `bc` directory under the README file

![](/images/bc.png)

</p>
</details>

## Step 4 - How would you read the provided GRUB2 manual?

<details><summary>Solution</summary>
<p>
	
Under the `grub2` directory there is a .html file. Open it with Firefox

![](/images/grub2.png)

</p>
</details>

## Step 5 - What software provides its document as a separate package?

<details><summary>Solution</summary>
<p>
	
Use `yum` to display only those packages that contain -doc, -docs or -documentation in the package name

![](/images/doc.png)

</p>
</details>

</p>
</details>

<details><summary>Module 3 - Lab 4 (Using __sosreport__ Command to Generate a SoS Report)</summary>
<p>
	
## Step 1 - If currently working as a non-root user, switch to root

<details><summary>Solution</summary>
<p>
	
To switch to root, simply type `su -` and use the password `redhat`

![](/images/root2.png)

</p>
</details>

## Step 2 - Run the __sosreport__ command

<details><summary>Solution</summary>
<p>
	
Simply type `sosreport` command

![](/images/sosreport.png)
	
</p>
</details>

## Step 3 - Change directory to /var/tmp and unpack the archive

<details><summary>Solution</summary>
<p>
	
Use the `tar -xvf <filename>` command to unpack it all

![](/images/generate.png)

</p>
</details>

## Step 4 - Change directory to the resulting subdirectory and browse the files founmd there


<details><summary>Solution</summary>
<p>
	
Open files, list directories, and continue to browse to become familiar with the information included in SoS reports. When finished, remove the archive directory and files

![](/images/route.png)
	
</p>
</details>

</p>
</details>

<details><summary>Module 3 - Lab 5 (Research Methods Used by Sys Admins)</summary>
<p>
	
## Step 1 - Research man(1) to determine how to prepare a man page for printing

<details><summary>Solution</summary>
<p>
	
Simply use the `man man` command to research the man command

![](/images/mant.png)

</p>
</details>

## Step 2 - Create a formatted output file of the paswd man page

<details><summary>Solution</summary>
<p>
	
To create this, simply use the `-t` man option with with passwd file and output it to a .ps file

![](/images/pass.png)
	
</p>
</details>

## Step 3 - Research using man to learn the commands used for viewing or printing PostScript files after updating the manual page index cache

<details><summary>Solution</summary>
<p>
	
Using the `man -k` command and searching for either `postscript` or `viewer` will return man pages matching either word

![](/images/mank.png)
	
</p>
</details>

## Step 4 - Research evince(1) using man to learn how to use the viewer in preview mode

<details><summary>Solution</summary>
<p>
	
Simply use `man evince` command and read through it

![](/images/evince.png)
	
</p>
</details>

## Step 5 - View your PostScript file using the various evince options you researched

<details><summary>Solution</summary>
<p>
	
First, you can simply use `evince passwd.ps` to view it normally

![](/images/pass1.png)

Secondly, you can use the `-w` option to preview it

![](/images/pass2.png)

Lastly, using the `-i  3` option will open it at page 3 (exact page nmuber)

![](/images/pass3.png)
	
</p>
</details>

## Step 6 - Using man research lp(1) to determine how to print any document starting on a specific page

<details><summary>Solution</summary>
<p>
	
Simply use `man lp` and find out what the syntax would be to print only pages 2 and 3 of the PostScript file

![](/images/pages.png)

Note that the `-P` option specifies pages. The lp command spools to the default printer.
	
</p>
</details>

## Step 7 - Using pinfo, look for GNU info about the evince viewer

<details><summary>Solution</summary>
<p>
	
Use the `pinfo evince` command to open straight into evince - note that the man page is displayed instead. The pinfo document viewer looks for relevant man page when no appropriate GNU documentation node exists

![](/images/evinceman.png)

</p>
</details>

## Step 8 - Use pinfo to locate and browse all document nodes for the coreutils commands and programs

<details><summary>Solution</summary>
<p>
	
First, open up `pinfo` normally. Then select the `Coreutils: Core GNU` option and press Enter. Then select Introduction. Walk through the Introduction by press n for the next node until node 29

![](/images/tools.png)
	
</p>
</details>

## Step 9 - Using firefox, open the system's package documentation and browse into the man-db package subdirectory

<details><summary>Solution</summary>
<p>
	
Simply type `firefox /usr/share/doc` to open up the directory in Firefox. Once there, navigate to the man-db page. You can view either the .txt file or the .ps file

![](/images/firefox.png)
	
</p>
</details>

## Step 10 - Using the open Firefox browser, locate and browser into the initscripts package subdirectory and view the sysconfig.txt file


<details><summary>Solution</summary>
<p>
	
Simply navigate to the request directory and view the file sysconfig.txt inside Firefox

![](/images/sysconf.png)
	
</p>
</details>

</p>
</details>

</p>
</details>

<details><summary>Module 4</summary>
<p>
	

<details><summary>Module 4 - Lab 1 - (Using Vim)</summary>
<p>
	
## Step 1 - Open vimtutor, read the welcome screen and perform lesson 1.1

<details><summary>Solution</summary>
<p>
	
This lesson talks about navigating via the h, j, k and l keys

![](/images/lessons1_1.png)

</p>
</details>

## Step 2 - Return to the vimtutor window and perform lesson 1.2

<details><summary>Solution</summary>
<p>
	
This lesson talks about quitting vim

![](/images/lessons1_2.png)

</p>
</details>

## Step 3 - Return to the vimtutor window and perform lesson 1.3

<details><summary>Solution</summary>
<p>
	
This lesson talks about editing and deletion of text

![](/images/lessons1_3.png)

</p>
</details>

## Step 4 - Return to the vimtutor window and perform lesson 1.4

<details><summary>Solution</summary>
<p>
	
This lesson talks about inserting text and how to do it

![](/images/lessons1_4.png)

</p>
</details>

## Step 5 - Return to the vimtutor window and perform lesson 1.5

<details><summary>Solution</summary>
<p>
	
This lessons talks about appending text

![](/images/lessons1_5.png)

</p>
</details>

## Step 6 - Return to the vimtutor window and perform lesson 1.6

<details><summary>Solution</summary>
<p>
	
This lesson talks about editing a file

![](/images/lessons1_6.png)

</p>
</details>

## Step 7 - Return to the vimtutor window and read the lesson 1 summary

<details><summary>Solution</summary>
<p>
	
![](/images/lesson_summary.png)

</p>
</details>

</p>
</details>

<details><summary>Module 4 - Lab 2 (Editing with Gedit)</summary>
<p>
	
## Step 1 - Redirect a long listing of all home directory files into a file named gedit_lab.txt

<details><summary>Solution</summary>
<p>
	
First, use the command `ls -al` to display all files and use the `>` operator to redirect output to a file

![](/images/redirect.png)

</p>
</details>

## Step 2 - Open the file with gedit in the background

<details><summary>Solution</summary>
<p>
	
Using the `&` symbol allows us to run files in the background and still be able to use the terminal

![](/images/amper.png)
	
</p>
</details>

## Step 3 - Insert the date at the top of the file via the date command and copying the reuslts

<details><summary>Solution</summary>
<p>
	
In the terminal, use the `date "+%A", "%B", "%d", "%Y"` to display the current date and copy it into gedit using the shortcuts

![](/images/date5.png)	
	
</p>
</details>

## Step 4 - Insert a description for this document including your username and host name via the command line and copy

<details><summary>Solution</summary>
<p>
	
To get the username and hostname, you can use the `$USER` and `$(hostname)` options on the command line to generate a sentence

![](/images/echouser.png)	
	
</p>
</details>

## Step 5 - Remove files that are not hidden configuration files or directories

<details><summary>Solution</summary>
<p>
	
Simply remove them inside gedit like a normal text editor so only the `.<files>` exist
	
![](/images/finish.png)	

</p>
</details>

</p>
</details>

<details><summary>Module 4 - Lab 3 (Editing a File using Vim's Visual Mode)</summary>
<p>
	
## Step 1 - Redirect a long list of all content in student's home directory into a file called editing_final_lab.txt

<details><summary>Solution</summary>
<p>
	
Simply use the `ls -al` option and redirect operators

![](/images/final.png)	

</p>
</details>

## Step 2 - Edit the file using Vim to take advantage of visual mode

<details><summary>Solution</summary>
<p>
	
Simlpy open the file using Vim

![](/images/visual.png)	
	
</p>
</details>

## Step 3 - Remove the first three lines

<details><summary>Solution</summary>
<p>
	
Use the arrow keys to position the cursor at the first character in the first row and hit `V` to enter line-based visual mode. Move down using the down arrow key three to select the first three rows and delete them with `x`

![](/images/first_three.png)	
	
</p>
</details>

## Step 4 - Remove permission columns for group and other on the first list

<details><summary>Solution</summary>
<p>
	
Use the arrow keys to position the cursor at the first character and enter visual mode with `V`. Then, use the arrow keys to position the cursor at the last character and delete with `x`

![](/images/x.png)	
	
</p>
</details>

## Step 5 - Remove the permission columns for group and other on the remaining lines

<details><summary>Solution</summary>
<p>
	
Again, use the arrow keys to position the cursor at the first character, enter visual mode with the control sequence `CTRL+V` and use the arrow keys to position the cursor at the last character of the column then press x to delete

![](/images/x2.png)	
	
</p>
</details>

## Step 6 - Remove the group owner column leaving only one student column on all lines

<details><summary>Solution</summary>
<p>
	
Do the same thing as step 5 - position the cursor at the start, hit CTRL+V, move to the bottom and delete

![](/images/x3.png)	
	
</p>
</details>

## Step 7 - Remove the time column but leave the month and day on all lines

<details><summary>Solution</summary>
<p>
	
Again, do the same but with the time column this time

![](/images/time.png)
	
</p>
</details>

## Step 8 - Remove the Desktop and Public rows

<details><summary>Solution</summary>
<p>
	
Once more, delete the rows this time with normal visual mode (V) and delete using `x`

![](/images/capital.png)
	
</p>
</details>

## Step 9 - Save and exit and make a backup using the date in seconds to create a unique filename

<details><summary>Solution</summary>
<p>
	
Save and exit vim using `:wq` command. Then, make the backup using the `cp editing_final_lab.txt editing_final_lab_$(date +%s).txt` command

![](/images/seconds.png)
	
</p>
</details>

## Step 10 - Mail the file contents as the message not an attachement to the student user

<details><summary>Solution</summary>
<p>
	
To mail it, simply pipe the `cat` command into the mail command. The `-s` option sets the subject line and `student` is the recipient

![](/images/mail.png)
	
</p>
</details>

## Step 11 - Append a dashed line to the file to recognize the beginning of newer content

<details><summary>Solution</summary>
<p>
	
Use the `echo` command to append a dotted line to the end of the file

![](/images/dotted.png)
	
</p>
</details>

## Step 12 - Append a full process listing but only for processes owned by the current user student

<details><summary>Solution</summary>
<p>
	
To list all process use the `ps -f` command (`-f` means full format listing) and then use the `tee -a editing_final_lab.txt` command to append it (`-a` for append)

![](/images/tee.png)
	
</p>
</details>

## Step 13 - Confirm that the process listing is at the bottom

<details><summary>Solution</summary>
<p>
	
Simply cat out the file to confirm it happened

![](/images/confirm.png)
	
</p>
</details>

</p>
</details>

</p>
</details>

<details><summary>Module 5</summary>
<p>
	

<details><summary>Module 5 - Lab 1 (Running Commands as Root)</summary>
<p>

## Step 1 - View the user and group info and display current directory

<details><summary>Solution</summary>
<p>

Simply use the `id` command to view info and `pwd` command to display the current directory

![](/images/usrgroup.png)

</p>
</details>

## Step 2 - View the variables which specify the home directory and locations searched for executable files

<details><summary>Solution</summary>
<p>

Use the `echo $HOME` and `echo $PATH` to read the $HOME and $PATH variables respectively 

![](/images/homepath.png)

</p>
</details>

## Step 3 - Switch to root without the dash

<details><summary>Solution</summary>
<p>

Type the `su` command without any arguments to switch to root

![](/images/nodash.png)

</p>
</details>

## Step 4 - View user and group info and display current directory

<details><summary>Solution</summary>
<p>
	
Use the same commands as step 1 - `id` and `pwd`

![](/images/idpwd.png)

</p>
</details>

## Step 5 - View variables which specify the home directory and locations searched for executable files

<details><summary>Solution</summary>
<p>
	
Use the same commands as step 2 - `echo $HOME/$PATH`

![](/images/pathhome.png)

</p>
</details>

## Step 6 - Exit the shell and return to student user

<details><summary>Solution</summary>
<p>
	
Simply type the `exit` command

![](/images/exit2.png)

</p>
</details>

## Step 7 - Switch to root with the dash

<details><summary>Solution</summary>
<p>
	
To use the dash to switch to root, use the `su -` command

![](/images/withdash.png)

</p>
</details>

## Step 8 - View user and group info and display current directory

<details><summary>Solution</summary>
<p>
	
Use the same commands as step 1 - `id` and `pwd`

![](/images/idpwd2.png)

</p>
</details>

## Step 9 - View variables which specify the home directory and locations searched for executable files

<details><summary>Solution</summary>
<p>
	
Use the same commands as step 2 - `echo $HOME/$PATH`

![](/images/rootid.png)

</p>
</details>

## Step 10 - Exit the shell and return to student user

<details><summary>Solution</summary>
<p>
	
Siomply type the `exit` command

![](/images/exit3.png)

</p>
</details>

## Step 11 - View last 5 lines of /var/log/messages

<details><summary>Solution</summary>
<p>
	
To view the last 5 lines of a file, use the `tail` command with the `-5` option to specify how many lines up you want to display

![](/images/varlogmes.png)

</p>
</details>

## Step 12 - Make backup of a config file in the /etc directory

<details><summary>Solution</summary>
<p>
	
To make a backup, simply copy the file and use a different name as the output via the `cp` command

![](/images/motd.png)

</p>
</details>

## Step 13 - Remove the /etc/motdOLD file

<details><summary>Solution</summary>
<p>
	
To remove a file, simply use the `rm` command on the specified file

![](/images/rmetc.png)

</p>
</details>

## Step 14 - Edit a config file in the /etc directory

<details><summary>Solution</summary>
<p>
	
Use the `echo` command to print text to the string and use the `>>` operator to append it to a specified file

![](/images/sudo.png)

</p>
</details>

</p>
</details>

<details><summary>Module 5 - Lab 2 (Creating Users)</summary>
<p>

## Step 1 - Become the root user at the shell prompt

<details><summary>Solution</summary>
<p>

Use the `su -` or `su` command to become the root uses (the password is redhat)

![](/images/root3.png)

</p>
</details>

## Step 2 - Add the user juliet

<details><summary>Solution</summary>
<p>

Use the `useradd juliet` command to create a new user on the system

![](/images/useradd2.png)

</p>
</details>

## Step 3 - Confirm that juliet was added by examining /etc/passwd

<details><summary>Solution</summary>
<p>

Simply view the contents of the `/etc/passwd` file to see the new user located at the bottom

![](/images/juliet.png)

</p>
</details>

## Step 4 - Use the passwd command to initialize juliet's password

<details><summary>Solution</summary>
<p>

Use the `passwd juliet` command to create a password for the specified user

![](/images/passjuliet.png)

</p>
</details>

## Step 5 - Continue adding the remaining users and set initial passwords: romeo, hamlet, reba, dolly and elvis

<details><summary>Solution</summary>
<p>

Using the same commands for juliet, do the same thing for the remaining 5 users

![](/images/5users.png)

</p>
</details>

</p>
</details>

<details><summary>Module 5 - Lab 3 (Supplementary Groups)</summary>
<p>

## Step 1 - Become root user

<details><summary>Solution</summary>
<p>
	
Use the `su -` command

![](/images/becomeroot.png)

</p>
</details>

## Step 2 - Create supplementary group called shakespeare with a GID of 30000

<details><summary>Solution</summary>
<p>
	
Use the `groupadd -g 30000 shakespeare` command

![](/images/addshake.png)

</p>
</details>

## Step 3 - Create supplementary group called artists

<details><summary>Solution</summary>
<p>
	
Use the `groupadd artists` command

![](/images/addart.png)

</p>
</details>

## Step 4 - Confirm that shakespeare and artists have been added via the /etc/group file

<details><summary>Solution</summary>
<p>
	
Use the `tail -5 /etc/group` command

![](/images/shakeconf.png)

</p>
</details>

## Step 5 - Add juliet user to the shakespeare group as a supplementary group

<details><summary>Solution</summary>
<p>
	
Use the `usermod -G shakespeare juliet` command

![](/images/addjuli.png)

</p>
</details>

## Step 6 - Confirm juliet has been added using the id command

<details><summary>Solution</summary>
<p>
	
Use the `id juliet` command

![](/images/julietid.png)

</p>
</details>

## Step 7 - Add romeo and hamlet to the shakespeare group and add reba, dolly and elvis to the artists group

<details><summary>Solution</summary>
<p>
	
Use the same commands above to add them to the respective groups

![](/images/repeatcomms.png)

</p>
</details>

## Step 8 - Verify the supplemental group memberships by examining the /etc/group file

<details><summary>Solution</summary>
<p>
	
Use the `tail -5 /etc/group` command

![](/images/verifygroups.png)

</p>
</details>

</p>
</details>

<details><summary>Module 5 - Lab 4 (Setting Unique Password Policies)</summary>
<p>

## Step 1 - Lock the romeo account

<details><summary>Solution</summary>
<p>
	
Use the `sudo usermod -L romeo` command to lock the account

![](/images/romeolock.png)

</p>
</details>

## Step 2 - Attempt to login as romeo

<details><summary>Solution</summary>
<p>
	
Use the `su - romeo` command to switch user to romeo

![](/images/romlog.png)

</p>
</details>

## Step 3 - Unlock the romeo account

<details><summary>Solution</summary>
<p>
	
Use the `sudo usermod -U romeo` command to unlock the account

![](/images/romunlock.png)

</p>
</details>

## Step 4 - Change password policy for romeo to require a new password every 90 days

<details><summary>Solution</summary>
<p>
	
Use the `sudo chage -M 90 romeo` and `sudo chage -l romeo` commands

![](/images/pass90days.png)

</p>
</details>

## Step 5 - Force a password change on the first login for romeo

<details><summary>Solution</summary>
<p>
	
Use the `sudo chage -d 0 romeo` command

![](/images/romforce.png)

</p>
</details>

## Step 6 - Login as romeo and change the password to forsooth123

<details><summary>Solution</summary>
<p>
	
Use the `su - romeo` command to login and change the password

![](/images/romloginpass.png)

</p>
</details>

## Step 7 - Determine a date 180 days in the future and set accounts to expire on that date

<details><summary>Solution</summary>
<p>
	
Use the `date -d "+180 days"` command to find the date. Then, use the `sudo chage -E 2014-08-02 romeo` and `sudo chage -l romeo` commands to set the accounts to that date

![](/images/dateexpire.png)

</p>
</details>

</p>
</details>

<details><summary>Module 5 - Lab 5 (Performance Checklist)</summary>
<p>

## Step 1 - Ensure that all newly created users have passwords which must be changed every 30 days

<details><summary>Solution</summary>
<p>

Use a text editor to edit the `/etc/login.defs` file and change the PASS_MAX_DAYS field to 30

![](/images/every30days.png)

</p>
</details>

## Step 2 - Create a new group named consultants with a GID of 40000

<details><summary>Solution</summary>
<p>

Use the `groupadd -g 40000 consultants` command to create the new group

![](/images/consultants.png)

</p>
</details>

## Step 3 - Create three new users (sspade, bboop, dtracy) with a password of __default__ and add them to the consultants group - the primary group should remain as the user private group

<details><summary>Solution</summary>
<p>

Use the `useradd -G consultants <user>` command to add the three new users to the group and then use the `passwd <user>` command to change all three users passwords

![](/images/add3users.png)

</p>
</details>

## Step 4 - Determine the date 90 days from now and set each of the three new user accounts to expire then

<details><summary>Solution</summary>
<p>

Use the `date -d "+90 days"` to determine the date from now and use the `chage -E YYYY-MM-DD <user>` command to set the expiry for the users

![](/images/90days.png)

</p>
</details>

## Step 5 - Change the password policy for the bboop account to require a new password every 15 days

<details><summary>Solution</summary>
<p>

Use the `chage -M 15 <user>` to change the policy and use the `chage -l <user>` to verify it

![](/images/passpolice.png)

</p>
</details>

## Step 6 - Force all users to change their password on first login

<details><summary>Solution</summary>
<p>

Use the `chage -d 0 <user>` to make all users change their password upon login

![](/images/uplogins.png)

</p>
</details>

</p>
</details>

</p>
</details>

<details><summary>Module 6</summary>
<p>
	

<details><summary>Module 6 - Lab 1 (Changing Permissions)</summary>
<p>

## Step 1 - Become the root user

<details><summary>Solution</summary>
<p>

Use the `su -` command

![](/images/becameroot.png)

</p>
</details>

## Step 2 - Run lab permissions setup to create the environment

<details><summary>Solution</summary>
<p>

Run the `lab permissions setup` command

![](/images/labperms.png)

</p>
</details>

## Step 3 - Create a directory in /home called ateam-text

<details><summary>Solution</summary>
<p>

Use the `mkdir ateam-text` command inside the /home directory

![](/images/ateam.png)

</p>
</details>

## Step 4 - Change the group ownership of the ateam-text directory to atem

<details><summary>Solution</summary>
<p>

Use the `chown :ateam /home/ateam-text` command to change group ownership

![](/images/changegroupa.png)

</p>
</details>

## Step 5 - Ensure the permissions of ateam-text allows group members to create/delete files

<details><summary>Solution</summary>
<p>

Use the `chmod g+w /home/ateam-text` command to change permissions

![](/images/ensureperms.png)

</p>
</details>

## Step 6 - Ensure the permissions of ateam-text forbids others from accessing its files

<details><summary>Solution</summary>
<p>

Use the `chmod 770 /home/ateam-text` command to forbid anyone else from accessing it	

![](/images/ensureperms2.png)

</p>
</details>

## Step 7 - Exit the root shell and switch to andy with a password of password

<details><summary>Solution</summary>
<p>

Type `exit` and then `su - andy` to swap users

![](/images/changeandy.png)

</p>
</details>

## Step 8 - Navigate to the /home/ateam-text folder

<details><summary>Solution</summary>
<p>

Use the cd command to navigate to /home/ateam-text folder

![](/images/navatext.png)

</p>
</details>

## Step 9 - Create an empty file called andyfile3

<details><summary>Solution</summary>
<p>

Use the `touch andyfile3` to create a new file

![](/images/andyfile3.png)

</p>
</details>

## Step 10 - Record the default user and group ownership of the new file

<details><summary>Solution</summary>
<p>

Use the `ls -l andyfile3` command to check permissions of the file

![](/images/defug.png)

</p>
</details>

## Step 11 - Change the group ownership of the new file to ateam and record the new ownership and permissions

<details><summary>Solution</summary>
<p>

Use the `chown :ateam andyfile3` to change ownership

![](/images/chgrpown.png)

</p>
</details>

## Step 12 - Exit the shell and switch to user alice with a password of password

<details><summary>Solution</summary>
<p>

Use the `exit` and `su - alice` commands to change users to alice

![](/images/alicechange.png)

</p>
</details>

## Step 13 - Navigate to the /home/ateam-text folder

<details><summary>Solution</summary>
<p>

Use the cd command to change to the /home/ateam-text folder

![](/images/ateamtext.png)

</p>
</details>

## Step 14 - Determine alice's privileges to access and/or modify andyfile3

<details><summary>Solution</summary>
<p>

Use the `echo "text" >> andyfile3` command to write to the file

![](/images/detalice.png)

</p>
</details>

</p>
</details>

<details><summary>Module 6 - Lab 2 (Controlling Default Permissions)</summary>
<p>

## Step 1 - Login as alice and use the umask command without arguments to display the default umask value

<details><summary>Solution</summary>
<p>

Use the `umask` command to view the default value

![](/images/sualice.png)

</p>
</details>

## Step 2 - Create a new directory /tmp/shared and a new file /tmp/shared/defaults to see how the default umask affects permissions

<details><summary>Solution</summary>
<p>

Use the `mkdir /tmp/shared` and `touch /tmp/shared/defaults` to create the directory and file. Then, use the `ls -l /tmp/shared/defaults` command to see the default permissions for the file

![](/images/defaults.png)

</p>
</details>

## Step 3 - Change the group ownership of /tmp/shared to ateam and record the new ownership and permissions

<details><summary>Solution</summary>
<p>

Use the `chown :ateam /tmp/shared` to change ownership of the directory and use the `ls -ld /tmp/shared` to view the permissions

![](/images/ateamshared.png)

</p>
</details>

## Step 4 - Create a new file in /tmp/shared and record the ownership and permissions

<details><summary>Solution</summary>
<p>

Use the `touch /tmp/shared/alice3` to create the file and use `ls -l /tmp/shared/alice3` to view the permissions

![](/images/alice3.png)

</p>
</details>

## Step 5 - Ensure the permissions of /tmp/shared cause files created in that directory to inherit the group ownership of ateam

<details><summary>Solution</summary>
<p>

Use the `chmod g+s /tmp/shared` command to change permissions and the `touch /tmp/shared/alice4` command to create a new file. Then, use the `ls -l /tmp/shared/alice4` to view the permissions

![](/images/alice4.png)

</p>
</details>

## Step 6 - Change the umask for alice such that new files are created with read-only access for the group and no access for others. Create a new file and record the permissions

<details><summary>Solution</summary>
<p>

Use the `umask 027` command to change the value of umask and use `touch /tmp/shared/alice5` to create the new file. Then, view the permissions via `ls -l /tmp/shared/alice5`

![](/images/alice5.png)

</p>
</details>

## Step 7 - Open a new shell and view the umask

<details><summary>Solution</summary>
<p>

Simply type `umask` to see the value

![](/images/newtab.png)

</p>
</details>

## Step 8 - Change the default umask for alice to prohibit all access for users not in their group

<details><summary>Solution</summary>
<p>

Open the `~/.bashrc` file with a text editor and input the line `umask 007` at the bottom 

![](/images/umask007.png)

</p>
</details>

## Step 9 - Log out and back in as alice and confirm that the umask changes are persistent

<details><summary>Solution</summary>
<p>

Typing `umask` should reveal the new default umask value

![](/images/changedef.png)

</p>
</details>

</p>
</details>

<details><summary>Module 6 - Lab 3 (Performance Checklist)</summary>
<p>

## Step 1 - Open a terminal and change to the root user

<details><summary>Solution</summary>
<p>

Use the `su -` command with the password redhat

![](/images/redhat.png)

</p>
</details>

## Step 2 - Create the /home/stooges directory

<details><summary>Solution</summary>
<p>

Use the `mkdir /home/stooges` command to create the directory

![](/images/stooges.png)

</p>
</details>

## Step 3 - Change group permissions on the /home/stooges directory so it belongs to the stooges group

<details><summary>Solution</summary>
<p>

Use the `chown :stooges /home/stooges` to change ownership

![](/images/changestoo.png)

</p>
</details>

## Step 4 - Set permissions on the /home/stooges directory so it is a set GID bit directory, the owner and group have full rwx permissions and other users have no permissions

<details><summary>Solution</summary>
<p>

Use the `chmod 2770 /home/stooges` command to change permissions

![](/images/setguid.png)

</p>
</details>

## Step 5 - Check the permissions were set properly

<details><summary>Solution</summary>
<p>

Simply use the `ls -ld /home/stooges` command to check permissions

![](/images/homestooges.png)

</p>
</details>

## Step 6 - Modify the global login scripts so that normal users have a umask setting which prevents others from viewing or modifying new files and directories

<details><summary>Solution</summary>
<p>

Open the /etc/bashrc and /etc/profile files and edit them with the specific umask

![](/images/umask.png)


</p>
</details>

</p>
</details>

</p>
</details>

<details><summary>Module 7</summary>
<p>
	
<details><summary>Module 7 - Lab 1 (Suspending User Processes)</summary>
<p>

## Step 1 - Open two terminals side by side

## Step 2 - In the left window, start a process that continously appends the word "rock" and a space to the file `~/outfile` at one second intervals

<details><summary>Solution</summary>
<p>

Use the following command - `(while true; do echo -n "rock " >> ~/outfile; sleep 1; done)`. The complete command MUST be contained in brackets for job control to interpret the set as a single job

![](/images/while.png)

</p>
</details>

## Step 3 - In the right window, use tail to confirm the new process is writing to the file

<details><summary>Solution</summary>
<p>

Use the `tail -f ~/outfile` command to constantly update the tail command in real time

![](/images/rock.png)

</p>
</details>

## Step 4 - In the left window, suspend the running process

<details><summary>Solution</summary>
<p>

Hit Ctrl+Z to suspend a running process

![](/images/ctrlz.png)

</p>
</details>

## Step 5 - In the left window, view the jobs list

<details><summary>Solution</summary>
<p>

The + denotes the current job. Use the `bg` command to restart the current job

![](/images/jobs.png)

</p>
</details>

## Step 6 - In the left window, start two more processes to append to the same output file. Replace "rock" with "paper" and then with "scissors"

<details><summary>Solution</summary>
<p>

Use the same command as the first one but appending an `&` at the end to start it in the background

![](/images/rps.png)

</p>
</details>

## Step 7 - In the left window, view jobs to seeall three processes

<details><summary>Solution</summary>
<p>

Use the `jobs` command to see all three processes "Running"

![](/images/jobs3.png)

</p>
</details>

## Step 8 - Using only commands previously learned, suspend the "rock" process. Then, foreground the job and suspend it using Ctrl+Z. Confirm the "rock" process is stopped

<details><summary>Solution</summary>
<p>

Use the `jobs` command to get the number. Once you have the number or job ID, use the `CTRL+Z` combination to suspend the process

![](/images/fg.png)

</p>
</details>

## Step 9 - End the "paper" process. Then, foreground the job, terminate it using Ctrl+C

<details><summary>Solution</summary>
<p>

Do the same as the previous step except use the CTRL+C combination to end the process instead

![](/images/paper.png)

</p>
</details>

## Step 10 - In the left window, view the remaining jobs using ps

<details><summary>Solution</summary>
<p>

Use the `ps j` command to view the remaining jobs. The suspended job has state of "T" while the other background job is sleeping (S)

![](/images/stat.png)

</p>
</details>

## Step 11 - Stop the remaining two jobs. In the left window, foreground either job. Terminate it using CTRL+C and repeat with the remaining job

<details><summary>Solution</summary>
<p>

To stop the remaining two jobs, use the same command as in step 9 for the other two jobs using their appropriate job IDs

![](/images/percent.png)

</p>
</details>

## Step 12 - In the right window, stop the tail command

<details><summary>Solution</summary>
<p>

Simply use CTRL+C to stop the tail command

</p>
</details>

</p>
</details>

<details><summary>Module 7 - Lab 2 (Multiple Shell Processes)</summary>
<p>

## Step 1 - Open two terminals side by side

## Step 2 - In the left, start three processes that append text to an output file at one-second intervals

<details><summary>Solution</summary>
<p>

Use the following commands to start the three processes - `(while true; do echo -n "game " >> ~/outfile; sleep 1; done) &` and simply replace the word with "set" and "match" for the other two commands

![](/images/3proc.png)

</p>
</details>

## Step 3 - In the right, use tail to confirm that all three processes are appending to the file

<details><summary>Solution</summary>
<p>

Simply use the `tail -f ¬/outfile` command to view the file

![](/images/outfile.png)

</p>
</details>

## Step 4 - Suspend the "game" process using signals. Confirm the game process is stopped

<details><summary>Solution</summary>
<p>

Use the `jobs` command to get the job ID and then use the `kill -SIGSTOP %1` to suspend the process

![](/images/gamestop.png)

</p>
</details>

## Step 5 - Terminate the "set" process using signals. Confirm the set process has disappeared

<details><summary>Solution</summary>
<p>

Use the `jobs` command to get the job ID and then use the `kill -SIGTERM %2` to terminate the process

![](/images/set.png)

</p>
</details>

## Step 6 - Resume the "game" process using signals. Confirm the game process is running

<details><summary>Solution</summary>
<p>

Use the `jobs` command to get the job ID and then use the `kill -SIGCONT %1` to continue the process

![](/images/gamestart.png)

</p>
</details>

## Step 7 - Terminate the remaining two jobs. Confirm that no jobs remain

<details><summary>Solution</summary>
<p>

Use the `jobs` command to get the job IDs and then use the `kill -SIGTERM %1` and `kill -SIGTERM %3` to terminate the processes

![](/images/kill.png)

</p>
</details>

## Step 8 - Close your session

<details><summary>Solution</summary>
<p>

Simply close the terminals

</p>
</details>

</p>
</details>

<details><summary>Module 7 - Lab 3 (Using the Top Command)</summary>
<p>

## Step 1 - Open two terminal windows

## Step 2 - In the left, determine the number of logical CPUs on the virtual machine

<details><summary>Solution</summary>
<p>

Run the `grep "model name" /proc/cpuinfo | wc -l` command to view the logical CPUs

![](/images/cpu.png)

</p>
</details>

## Step 3 - In the left, run a single instance of the process101 executable

<details><summary>Solution</summary>
<p>

Simply type `process101`

![](/images/proc1.png)

</p>
</details>

## Step 4 - In the right, observe the top display (use the single keystrokes `l`, `t` and `m` to toggle the load, threads and memory header lines)

<details><summary>Solution</summary>
<p>

Run the `top` command and observe

![](/images/top.png)

</p>
</details>

## Step 5 - Note the PID for process101. View the CPU percentage for the process (25% - 30%)

<details><summary>Solution</summary>
<p>

Simply observe the top command

![](/images/process1.png)

</p>
</details>

## Step 6 - In the left, run a second instance of process101

<details><summary>Solution</summary>
<p>

Run `process101` again

![](/images/proc2.png)

</p>
</details>

## Step 7 - In top, note the PID of the second process101

<details><summary>Solution</summary>
<p>

Simply observe the top command

![](/images/process2.png)

</p>
</details>

## Step 8 - In the left, run a third instance of process101

<details><summary>Solution</summary>
<p>

Run `process101` again

![](/images/proc3.png)

</p>
</details>

## Step 9 - In top, note the PID for the third process101

<details><summary>Solution</summary>
<p>

Simply observe the top command

![](/images/process3.png)

</p>
</details>

## Step 10 - Terminate each of the process101 process from within top

<details><summary>Solution</summary>
<p>

First, press `k`. Then type the PID of the process101 instance and press Enter. Finally, press Enter again to use the default SIGTERM signal 15

![](/images/pid.png)

</p>
</details>

## Step 11 - In the right, press q to exit top

<details><summary>Solution</summary>
<p>

Simply press `q` inside top

</p>
</details>

</p>
</details>

<details><summary>Module 7 - Lab 4 (Performance Checklist)</summary>
<p>

## Step 1 - Run the top utility

## Step 2 - Observe the top display. What are the processes using the most CPU time?

## Step 3 - Change the display to sort by the amount of memory in use

## Step 4 - What are the processes with the largest memory allocations?

## Step 5 - Turn off the use of bold in the display and save the configuration

## Step 6 - Exit top then restart it again

## Step 7 - Modify the display to again sort by CPU utilization and turn on the use of bold

## Step 8 - Open another terminal and suspend the hippo process. In top, observe the process state is now `T`

## Step 9 - The hippo process disappears. List the process information from the command line to confirm the process state

## Step 10 - Resume execution of the hippo process

## Step 11 - Terminate the extra processes elephant and hippo using the command line

## Step 12 - Check the cleanup is sucessful by running the grading script

## Step 13 - Exit the top display

