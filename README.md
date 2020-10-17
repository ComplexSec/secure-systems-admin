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
	
# Table of Contents <a name="INDEX2"></a>

1. [The File System Hierarchy](#HEIR)
2. [File System Hierarchy Review](#REV)
3. [Absolute Paths and Relative Paths](#ABS)
4. [Navigating Paths](#PATHS)
5. [Paths Review](#PAREV)
6. [Command-Line File Management](#CLFM)
7. [Lab 3 - File Management](#LAB3)
8. [File Globbing: Path Name Expansion](#FILE)

![](/images/linux2.png)

## The File System Hierarchy <a name="HEIR"></a> ([Back to Index](#INDEX2))

All files on Linux are stored on file systems which are organized into a single __inverted tree__ known as a __file system hierarchy__. The root of the tree is at the __top__ and the branches stretch __below__

![](/images/filesys.png)

The top directory is the root (/) directory. Subdirectories of `/` are used for standardized purposes to organize files by type and purpose. The following terms are encountered in describing file system directory contents:

* __Static__ is content that remains unchanged until explicitly edited or reconfigured
* __Dynamic__ or __variable__ is content typically modified or appended by active processes
* __Persistent__ is content, particularly configuration settings, that remain after a reboot
* __Runtime__ is a process or system specific content or attributes cleared during reboot

The following table lists some of the most important directories on the system by name and purpose:

Location | Purpose
------------ | -------------
/usr | Installed software, shared libraries, include files, and static read-only program data. Important subdirectories are `/usr/bin` which contains __user commands__, `/usr/sbin` which contains __system administration commands__ and `/usr/local` which contains __locally customized software__.
/etc | Configuration files specific to this system
/var | Variable data specific to this system that should persist between boots. Files that dynamically change (e.g. databases, cache directories, log files, printer-spooled documents and website content) may be found here
/run | Runtime data for processes started since the last boot. This includes process ID files and lock files, among other things. The contents of this directory are recreated on reboot
/home | __Home directories__ where regular users store their personal data and configuration files
/root | Home directory for the administrative superuser, root
/tmp | A world-writable space for temporary files. Files which have not been accessed, changed or modified for 10 days are deleted from here automatically. Another temporary directory exists `/var/tmp` in which files that have not been accessed, changed, or modified in more than 30 days are deleted automatically
/boot | Files needed in order to start the boot process
/dev | Contains special device files which are used by the system to access hardware

In RHEL 7, four older directories in `/` now have identical contents as their counterparts located in /usr:

* __/bin__ and __/usr/bin__
* __/sbin__ and __/usr/sbin__
* __/lib__ and __/usr/lib__
* __/lib64__ and __/usr/lib64__

In older versions of RHEL, these were distinct directories containing different sets of files. In RHEL 7, the directories in `/` are symbolic links to the matching directories in __/usr__

## File System Hierarchy Review <a name="REV"></a> ([Back to Index](#INDEX2))

Directory Purpose | Location
------------ | -------------
This directory contains static, persistent system configuration data | /etc
This is the system's root directory | /
User home directories are located under this directory | / home 
This is the root account's home directory | /root
This directory contains dynamic configuration data such as FTP and websites | /var
Regular user commands and utilities are located here | /usr/bin 
System administration binaries, for root user, are here | /usr/sbin
Temporary files are stored here | /tmp
Contains dynamic, non-persistent application runtime data | /run
Contains installed software programms and libraries | /usr

## Absolute Paths and Relative Paths <a name="ABS"></a> ([Back to Index](#INDEX2))

The path of a file or directory specifies its unique file system location

An __absolute path__ is a fully qualified name, beginning at the root directory and specifying each subdirectory traversed. Every __absolute path__ will start with `/`. When a user logs in and opens a terminal, the initial location is normally the user's home directory. System processes also have an initial directory

Users and processes navigate to other directories as needed; the terms __working directory__ or __current working directory__ refer to their __current__ location

A __relative path__ identifies a unique file, specifying only the path necessary to reach the file from the working directory

For standard Linux file systems, the path name of a file, including all `/` characters may be no more than 4095 bytes long. Each component of the path name seperated may be no more than __255 bytes long__. File names can use any UTF-8 encoded Unicode chararacter __EXCEPT__ `/` and the `NUL` character

Linux file systems - ext4, XFS, BTRGS, GFS2 and GlusterFS - are __case sensitive__ in terms of filenames. The VFAT file system is NOT case-sensitive. However, VFAT along with Microsoft's NTFS and Apple's HFS+ has __case preserving__ behaviour

## Navigating Paths <a name="PATHS"></a> ([Back to Index](#INDEX2))

The `pwd` command displays the full path name of the current location. The `ls` command lists directory contents for specified or current directory

![](/images/pwdls.png)

Use the `cd` command to change directories. Can use absolute or relative paths

![](/images/cd.png)

At any time, return to the user's home directory using `cd` without any destination

The `touch` command normally updates a file's timestamp to the current data and time without otherwise modifying it. Useful for creating empty files. The `ls` command has multiple options for displaying attributes on files - most common being `-l` for long listing, `-a` for including hidden files, and `-R` for recursive to include contents of all subdirs

File names beginning with a dot indicate files __hidden__ from normal view using `ls` and other commands. Hidden files keep necessary user configuration files from cluttering home directories. Many commands process hidden files only with specific command-line options, preventing one user's configuration from being accidentally copied to other directories

The `cd` command has many options. The `cd -` command changes to the previous directory. The `cd ..` command uses the `..` hidden directory to move up one level to the parent directory

## Paths Review <a name="PAREV"></a> ([Back to Index](#INDEX2))

Action to accomplish | Command
------------ | -------------
List the current user's home directory (long format) in simplest syntax, when it is not the current location | ls - l ~
Return to the current user's home directory | cd
Determine the absolute path name of the current location | pwd
Return to the most previous working directory | cd -
Move up two levels from the current location | cd ../..
List the current location (long format) with hidden files | ls -al
Move to the binaries location, from any current location | cd /bin
Move up to the parent of the current location | cd ..
Move to the binaries location, from the root directory | cd bin 

## Command-Line File Management <a name="CLFM"></a> ([Back to Index](#INDEX2))

File management involves creating, deleting, copying and moving files. Additionally, directories can be created, deleted, copied and moved to help organize files logically

Activity | Single Source | Multiple Sources
------------ | ------------- | -------------
Copy File | cp file1 file2 | cp file1 file2 file3 dir <sup>(4)</sup>
Move File | mv file1 file2 <sup>(1)</sup> | mv file1 file2 file3 dir <sup>(4)</sup>
Remove File | rm file1 | rm -f file1 file2 file3 <sup>(5)</sup>
Create directory | mkdir dir | mkdir -p par1/par2/dir <sup>(6)</sup>
Copy directory | cp -r dir1 dir2 <sup>(2)</sup> | cp -r dir1 dir2 dir3 dir4 <sup>(4)</sup>
Move directory | mv dir1 dir2 <sup>(3)</sup> | mv dir1 dir2 dir3 dir4 <sup>(4)</sup>
Remove directory | rm -r dir1 <sup>(2)</sup> | rm -rf dir1 dir2 dir3 <sup>(5)</sup>
Remove empty directory | rmdir dir1 | rmdir -p dir1/dir2/dir3


SuperScript | Note
------------ | -------------
<sup>(1)</sup> | The result is a rename
<sup>(2)</sup> | The "recursive" option is required to process a source directory
<sup>(3)</sup> | If dir2 exists, the result is a move. If dir2 doesn't exist, the result is a rename
<sup>(4)</sup> | The last argument must be a directory
<sup>(5)</sup> | Use caution with "force" option; you will NOT be prompted to confirm your action 
<sup>(6)</sup> | Use caution with "create parent" option; typing errors are NOT caught

The `mkdir` command creates one or more directories - generates errors if file name already exists. The `-p` option creates missing parent directories for requested destination - accidental spelling errors create unintended directories without error messages

![](/images/mkdir.png)

The `cp` command copies one or more files to become new, independent files. Can copy existing file to new file in current/other directory or copy multiple files into another directory. If new file name is NOT unique, it overwrites existing file. When copying multiple files with one command, last argument MUST be a directory. Multiple `cp` commands ignore directories specified as a source. Copying non-empty directories, with contents, requires the `-r` option

The `mv` command renames files or relocates files. Files moved to different file system require creating new file by copying source file, and deleting source file. 

The `rm` deletes files but NOT directories. To delete directories, use the `-r` option. Using `-i` interactively prompts for each deletion. The `rmdir` command deletes empty directories.

## Lab 3 - File Management <a name="LAB3"></a> ([Back to Index](#INDEX))

Please refer to [Activities](https://github.com/ComplexSec/secure-systems-admin/tree/main/Activities) for the lab exercises

## File globbing - Path Name Expansion <a name="FILE"></a> ([Back to Index](#INDEX))

BASH has a path name-matching capability historically called __globbing__ which makes managing large numbers of files easier by using meta-characters that expand to match file and path names being sought

Globbing is a __shell command-parsing operation__ that expands a wildcard pattern into a list of matching path names. Patterns - especially square-bracketed character classes - that do not return matches display the original pattern request as literal text

Pattern | Matches
------------ | -------------
`*` | Any string of zero or more characters
`?` | Any single character 
`~` | The current user's home directory
`~username` | User's home directory
`~+`  | The current working directory
`~-`  | The previous working directory
`[abc...]`  | Any one character in the enclosed class
`[!abc...]`  | Any one character NOT in the enclosed class
`[^abc...]`  | Any one character NOT in the enclosed class
`[[:alpha:]]` | Any alphabetic character
`[[:lower:]]` | Any lower-case character
`[[:upper:]]` | Any upper-case character
`[[:alnum:]]` | Any alphabetic character or digit
`[[:punct:]]` | Any printable character not a space or alphanumeric
`[[:digit:]]` | Any digit 0-9
`[[:space:]]` | Any one whitespace character (tabs, newline, carriage returns, space)
`Note` | pre-set POSIX character class; adjusts for current locale

![](/images/glob.png)

The tilde character (`~`) when followed by a slash delimiter matches the current user's home directory. When followed by a string of characters up to a slash, it is interpreted as the username

![](/images/echoglob.png)

Brace expansion is used to generate discretionary strings of characters. Braces contain a comma-separated list of strings, or a sequence expression. Brace expansions may be nested one inside another

![](/images/brace.png)

Command substitution allows the output of a command to replace the command itself. Occurs when command is enclosed with beginning dollar sign and brackets or with backticks

The backticks have two disadvantages - easy to visually confused and cannot be nested inside backticks

![](/images/command.png)

Many characters have special meaning in the BASH shell. To ignore special meanings, __quoting__ and __escaping__ can be used. The `/` is an escape character protecting the single character following it from special interpretation.

To protect longer strings, single or double quotes can be used. Using double quotes still allows command and variable substitution. Variable substitution is conceptually identical to command substitution but may use optional brace syntax

![](/images/user.png)

Use single quotes to interpret __all__ text literally. Besides suppressing globbing and shell expansion, quotations direct the shell to additionally suppress command and variable substitution. The question mark is a meta-character that also needed protection from expansion

![](/images/single.png)

## File Globbing Review <a name="FILEREV"></a> ([Back to Index](#INDEX))

Requested match to find | Patterns
------------ | -------------
Only filenames beginning with b | `b*`
Only filenames ending in b | `*b`
Only filenames containing a b | `*b*` 
Only filenames where first character is not b | `[!b]*`
Only filenames at least 3 characters in length | `???`
Only filenames that contain a number | `*[[:digit:]]*`
Only filenames that begin with an upper-case letter | `[[:upper:]]*`  

</p>
</details>
