# Secure Systems Administration - Activities

## Try and solve the labs without looking at the solutions. If you get stuck, the solutions are available

NB. The `desktopX` machine is referred to as the `Workstation` machine on NetLab - both have student users

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

<details><summary>Lab 2 - Using Commands</summary>
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

### Step 6 - Display the first 10 lines of /usr/bin/clean-binary-files

### Step 7 - Display the last 10 lines at the bottom of /usr/bin/clean-binary-files

### Step 8 - Repeat the previous command but use the `-n 20` option to display the last 20 lines in the file

### Step 9 - Execute the date command without any arguments to display current date and time

### Step 10 - Use bash history to display just the time

### Step 11 - Finish the BASH session

</p>
</details>