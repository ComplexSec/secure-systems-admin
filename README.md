# Secure Systems Administration

## Year 2 University module all about Linux - specifically RHEL

<details><summary>Module 1 - Accessing the Command Line</summary>
<p>	
	
# Table of Contents <a name="INDEX"></a>

1. [The BASH Shell](#BASH)
2. [Virtual Consoles](#VCONS)
3. [Shell Basics](#SHELL)
4. [Terminology](#TERM)
5. [The GNOME Desktop Environment](#GNOME)
6. [Workspaces](#WORK)
7. [Starting a Terminal](#START)
8. [Locking the Screen/Shutting Down](#LOG)
9. [Lab 1 - Changing Password](#LAB)
10. [Basic Command Syntax](#SYN)
11. [Examples of Simple Commands](#SIMP)
12. [Command History](#HIST)
13. [Editing the Command Line](#EDIT)
14. [Lab 2 - Using Commands](#LAB2)

![](/images/linux.png)

## The BASH Shell <a name="BASH"></a> ([Back to Index](#INDEX))
	
* The Linux command line is provided by a program called the __shell__
* Default shell for users in RHEL is the __GNU Bourne-Again Shell (bash)__
* `$` indicates a normal user, `#` indicates the root user
* Bash provides a scripting language - supports automation of tasks

## Virtual Consoles <a name="VCONS"></a> ([Back to Index](#INDEX))

* Users access the __bash__ shell via __terminal__
* Terminal provides keyboard for input and display for output. Can be configured through serial ports
* A Linux machine's physical console supports multiple virtual consoles - act like separate terminals. Each virtual console supports an independent login session
* If GUI is available, it runs on the __first__ virtual console on RHEL 7
* With GUI running, access a text login prompt on a virtual console by pressing __Ctrl+Alt__ and pressing a function key

## Shell Basics <a name="SHELL"></a> ([Back to Index](#INDEX))

* Commands entered at the shell prompt have three basic parts:
	* Command to run
	* Options to adjust the behaviour of the command
	* Arguments which are typically targets of the command

The __command__ is the name of the program to run. Might be followed by one or more __options__. Options adjust the behaviour of the command - normally start with one or two dashes

Arguments often indicate a target that the command should operate on

Most commands have a __--help__ or __-h__ option. Usage statements have a few basic conventions

Symbols | Description
------------ | -------------
`[]` | Surround optional items
`<something>..` | represents an arbitrary length list of items of that type
item 1 __pipe__ item 2 | Means only __one__ of them can be specified
`<filename>` | Represents variable data

When a user is finished using the shell, use the `exit` command to terminate the current shell session or press `CTRL+D` 

## Terminology <a name="TERM"></a> ([Back to Index](#INDEX))

Description | Term
------------ | -------------
The interpreter that executes commands typed as strings | Shell
The visual cue that indicates an interactive shell is waiting for the user to type a command | Prompt
The name of a program to run | Command
The part of the command line that adjusts the behaviour of a command | Option
The part of the command line that specifies the target that the command should operate on | Argument
The hardware display and keyboard used to interact with a system | Physical console
One of multiple logical consoles that can each support an independent login session | Virtual console
An interface that provides a display for output and a keyboard for input to a shell session | Terminal

## The GNOME Desktop Environment <a name="GNOME"></a> ([Back to Index](#INDEX))

The desktop environment is the GUI on a Linux system. Default desktop environment in RHEL 7 is provided by __GNOME 3__ - provided by __X Windows System__

By default, RHEL 7  uses the __GNOME Classic__ theme for __gnome-shell__. Help can be quickly started by pressing `F1` in gnome-shell, by selecting __Applications --> Documentation --> Help__ or by running the `yelp` command

## Workspaces <a name="WORK"></a> ([Back to Index](#INDEX))

__Workspaces__ are seperate desktop screens which have different application windows. Three methods for switching between them:

	1. Clicking the indicator in the right corner of the window list
	2. CTRL+ALT+UpArrow` or `CTRL+ALT+DownArrow
	3. Switch to Activities Overview

Advantage of __Activities Overview__ - windows can be clicked and dragged between

## Starting a Terminal <a name="START"></a> ([Back to Index](#INDEX)) 

To get a shell prompt in GNOME, start a terminal application such as GNOME terminal. Three most commonly used methods:

	1. Applications --> Utilities --> Terminal
	2. Right-click and select Open in Terminal from context menu
	3. From Activities Overview, select Terminal from the dash

## Locking the Screen/Shutting Down <a name="LOG"></a> ([Back to Index](#INDEX))
To lock the screen, select __(User) --> Lock__ or press __CTRL+ALT+L__
To unlock the screen, press __Enter__ or __Space__

To shut down, select __(User) --> Power Off__ or press __CTRL+ALT+DEL__

## Lab 1 - Changing Password <a name="LAB"></a> ([Back to Index](#INDEX))

Please refer to [Activities](https://github.com/ComplexSec/secure-systems-admin/tree/main/Activities) for the lab exercises

## Basic Command Syntax <a name="SYN"></a> ([Back to Index](#INDEX))

The GNU Bourne-Again Shell(__BASH__) is a program that interprets commands typed in by the user. Each command is typed on a separate line and the output from each displays before the shell displays a prompt. To type more than one command on a line, use the `;`symbol as a __command separator__

The semicolon is in a class of characters called __metacharacters__ that has special meanings for BASH

## Examples of Simple Commands <a name="SIMP"></a> ([Back to Index](#INDEX))

The __date__ command displays current date and time - used by root to set the system clock. An argument that begins with `+` specifies a format string for date

![](/images/date.png)

The __passwd__ command changes a user's own password. Root can use the __passwd__ command to change other user's passwords

Linux does not require file name extensions to classify files. The `file` command scans the beginning of a file's content and displays what type it is

![](/images/file.png)

The `head` command displays the top 10 lines automatically. The `tail` command displays the bottom 10 lines. Both have the `-n` option to specify a number of lines

![](/images/tail.png)

The `wc` comand counts lines, words and chars in a file. Takes a `-l`, `-w` or `-c` option to display only lines, words and chars respectively

![](/images/wc.png)

Arguments and options can be matched with tab completion for MANY commands. The `useradd` command is used by root to create additional users on the system. It has many options. Tab completion following a partial option can be utilized

![](/images/useradd.png)

## Command History <a name="HIST"></a> ([Back to Index](#INDEX))

The `history` command displays a list of previously executed commands prefixed via number. The `!` character is used to expand previous commands without retyping. The `!3` command would run the 3rd last command entered. The `!ls` command would expand to the most recent command that begins with `ls`

![](/images/history.png)

Can also use arrow keys to navigate previous commands. The `Esc+.` key combination causes the shell to copy the last word of the previous command.

## Editing the Command Line <a name="EDIT"></a> ([Back to Index](#INDEX))

Shortcut | Description
------------ | -------------
`CTRL+A` | Jump to beginning of command
`CTRL+E` | Jump to end of command
`CTRL+U` | Clear from cursor to the beginning of command
`CTRL+K` | Clear from cursor to end of command
`CTRL+LEFT` | Jump to beginning of previous word on CL
`CTRL+RIGHT` | Jump to end of next word on CL
`CTRL+R` | Search history of commands for pattern

## Lab 2 - Using Commands <a name="LAB2"></a> ([Back to Index](#INDEX))

Please refer to [Activities](https://github.com/ComplexSec/secure-systems-admin/tree/main/Activities) for the lab exercises

</p>
</details>

<details><summary>Module 2 - Managing Files from the Command Line</summary>
<p>
	


</p>
</details>