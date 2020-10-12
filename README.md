# Secure Systems Administration

## Year 2 University module all about Linux - specifically RHEL

<details><summary>Module 1 - Accessing the Command Line</summary>
<p>	
	
![](/images/linux.png)
	
* The Linux command line is provided by a program called the __shell__
* Default shell for users in RHEL is the __GNU Bourne-Again Shell (bash)__
* `$` indicates a normal user, `#` indicates the root user
* Bash provides a scripting language - supports automation of tasks

* Users access the __bash__ shell via __terminal__
* Terminal provides keyboard for input and display for output. Can be configured through serial ports
* A Linux machine's physical console supports multiple virtual consoles - act like separate terminals. Each virtual console supports an independent login session
* If GUI is available, it runs on the __first__ virtual console on RHEL 7
* With GUI running, access a text login prompt on a virtual console by pressing __Ctrl+Alt__ and pressing a function key

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

## The GNOME Desktop Environment

The desktop environment is the GUI on a Linux system. Default desktop environment in RHEL 7 is provided by __GNOME 3__ - provided by __X Windows System__

By default, RHEL 7  uses the __GNOME Classic__ theme for __gnome-shell__. Help can be quickly started by pressing `F1` in gnome-shell, by selecting __Applications --> Documentation --> Help__ or by running the `yelp` command

## Workspaces

__Workspaces__ are seperate desktop screens which have different application windows. Three methods for switching between them:

	1. Clicking the indicator in the right corner of the window list
	2. CTRL+ALT+UpArrow` or `CTRL+ALT+DownArrow
	3. Switch to Activities Overview

Advantage of __Activities Overview__ - windows can be clicked and dragged between

## Starting a Terminal

To get a shell prompt in GNOME, start a terminal application such as GNOME terminal. Three most commonly used methods:

	1. Applications --> Utilities --> Terminal
	2. Right-click and select Open in Terminal from context menu
	3. From Activities Overview, select Terminal from the dash

## Locking the Screen/Shutting Down
To lock the screen, select __(User) --> Lock__ or press __CTRL+ALT+L__
To unlock the screen, press __Enter__ or __Space__

To shut down, select __(User) --> Power Off__ or press __CTRL+ALT+DEL__

## Lab 1 - Changing Password

Please refer to [Activities](https://github.com/ComplexSec/secure-systems-admin/tree/main/Activities) for the first lab

## Basic Command Syntax

The GNU Bourne-Again Shell(__BASH__) is a program that interprets commands typed in by the user. Each command is typed on a separate line and the output from each displays before the shell displays a prompt. To type more than one command on a line, use the `;`symbol as a __command separator__

The semicolon is in a class of characters called __metacharacters__ that has special meanings for BASH

## Examples of Simple Commands

The __date__ command displays current date and time - used by root to set the system clock. An argument that begins with `+` specifies a format string for date

![](/images/date.png)

The __passwd__ command changes a user's own password. Root can use the __passwd__ command to change other user's passwords

Linux 
</p>
</details>