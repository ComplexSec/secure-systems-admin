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
9. [File Globbing Review](#FILEREV)
10. [Lab 4 - Managing Files with Shell Expansion](#LAB4)

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

## Lab 3 - File Management <a name="LAB3"></a> ([Back to Index](#INDEX2))

Please refer to [Activities](https://github.com/ComplexSec/secure-systems-admin/tree/main/Activities) for the lab exercises

## File globbing - Path Name Expansion <a name="FILE"></a> ([Back to Index](#INDEX2))

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

## File Globbing Review <a name="FILEREV"></a> ([Back to Index](#INDEX2))

Requested match to find | Patterns
------------ | -------------
Only filenames beginning with b | `b*`
Only filenames ending in b | `*b`
Only filenames containing a b | `*b*` 
Only filenames where first character is not b | `[!b]*`
Only filenames at least 3 characters in length | `???`
Only filenames that contain a number | `*[[:digit:]]*`
Only filenames that begin with an upper-case letter | `[[:upper:]]*`  

## Lab 4 - Managing Files with Shell Expansion <a name="LAB4"></a> ([Back to Index](#INDEX2))

Please refer to [Activities](https://github.com/ComplexSec/secure-systems-admin/tree/main/Activities) for the lab exercises

</p>
</details>

<details><summary>Module 3 - Getting Help in Red Hat Enterprise Linux </summary>
<p>

# Table of Contents <a name="INDEX3"></a>

1. [Introducing the man Command](#MAN)
2. [Navigate and Search man Pages](#NAVIGATE)
3. [Searching for man Pages by Keyword](#KEYWORD)
4. [Lab 5 - Finding Relevant Information Using Man](#LAB5)
5. [Introducing GNU Info](#GNU)
6. [GNU Info vs. Man Page Navigation](#GNUINFO)
7. [Lab 6 - Understanding Program Documentation](#LAB6)
8. [Introducing Package Documentation](#PACKAGE)
9. [Research Documentation under /usr/share/doc](#LAB7)
10. [Using redhat-support-tool to Search Knowledge Base](#REDHAT)
11. [Directly Access Knowledge Base Articles by Document ID](#DIRECT)
12. [Using redhat-support-tool to Manage Support Cases](#SUPPORT)
13. [Managing A Bug Report with redhat-support-tool](#BUG)
14. [Including Diagnostic Information by Attaching a SoS Report Archive](#SOSREP)
15. [Lab 8 - Using __sosreport__ Command to Generate a SoS Report](#LAB8)
16. [Lab 9 - Research Methods Used by Sys Admins](#LAB9)

![](/images/4.png)

## Introducing the man Command <a name="MAN"></a> ([Back to Index](#INDEX3))

The historical __Linux Programmer's Manual__ is where the man page originates. Each contained information for specifiy types of files which have become sections

Section | Content Type
------------ | -------------
1 | User commands (both executable and shell programs)
2 | System calls (kernel routines invoked from user space) 
3 | Library functions (provided by program libraries)
4 | Special files (such as device files)
5 | File format (for many configurations files and structures)
6 | Games (historical section for amusing programs)
7 | Conventions, standards and miscellaneous (protocols, file systems)
8 | System administration and privileged commands (maintenance tasks)
9 | Linux kernel API (internal kernel calls)

Man page references include the section number in parentheses - __passwd(1)__ describes the command and __passwd(5)__ explains the /etc/passwd file

To read specific man pages, use `man <topic>`. Topic contents display one screen at a time. The __man__ command searches manual sections in a configured order - section 1 is displayed first if available - to display a different man page topic, include the section number eg. `man 5 passwd`

## Navigate and Search man Pages <a name="NAVIGATE"></a> ([Back to Index](#INDEX3))

The following table lists basic man navigation commands

Command | Result
------------ | -------------
Spacebar | Scroll forward one scree
PageDown | Scroll forward one screen
PageUp | Scroll backward one screen
DownArrow | Scroll forward one line
UpArrow | Scroll backword one line
d | Scroll foward one half-screen
u | Scroll backward one half-screen
/string | Search forward for __string__ in the man page
n | Repeat previous search forward in the man page
N | Repeat previous search backward in the man page
g | Go to start of the man page
G | Go to end of the man page
q | Exit __man__ and return to command shell prompt

When performing searches, __string__ allows __regex__ syntax. Regex uses meta-characters for more sophisticated pattern matching

## Searching for man Pages by Keyword <a name="KEYWORD"></a> ([Back to Index](#INDEX3))

A keyword search of man pages is performed using __man -k keyword__ which displays a list of keyword matching man page topics with section numbers

![](/images/mank.png)

Popular sections are 1, 5, and 8. Admins using certain troubleshooting tools also use section - remaining sections are commonly for programmer reference or advanced administration

NB. Keyword searches rely on an index generated by the __mandb(8)__ command, which must be run as root. Command runs daily through __cron.daily__ or by __anacrontab__ within an hour of boot

The `man -K` option performs a full-text page search - not just titles and descriptions

## Lab 5 - Finding Relevant Information Using Man <a name="LAB5"></a> ([Back to Index](#INDEX3))

Please refer to [Activities](https://github.com/ComplexSec/secure-systems-admin/tree/main/Activities) for the lab exercises

## Introducing GNU Info <a name="GNU"></a> ([Back to Index](#INDEX3))

Many pages have a formal format useful as a command reference but less useful as general documentation. Info documents are an important resource on RHEL - many fundamental components and utilities such as the __coreutils__ package and glibc standard libraries utilize it

![](/images/pinfo.png)

Info documentation is structured as hyperlinked info nodes - more flexible than man pages. Info nodes are read from CLI using either __info__ or __pinfo__ commands - some commands have both documentation for man and pinfo

The __pinfo__ reader is more advanced than __info__ commands. Info nodes for a particular topic are browsed with __pinfo topic__. New documentation nodes become available in __pinfo__ when their corresponding software packages are installed

## GNU Info vs. Man Page Navigation <a name="GNUINFO"></a> ([Back to Index](#INDEX3))

The __info__ command uses different navigation than __man__

Navigation | pinfo | man
------------ | ------------- | -------------
Scroll forward one screen | PageDown or Space | PageDown or Space
Scroll backward one screen | PageUp or b | PageUp or b
Display directory of topics | d | -
Scroll forward one half-screen | - | d
Display parent node of a topic | u | -
Display the top of a topic | HOME | 1G
Scroll backward one half-screen | - | u
Scroll forward to next hyperlink | DownArrow | -
Open topic at cursor location | Enter | -
Scroll forward one line | - | DownArrow or Enter
Scroll backward to previous hyperlink | UpArrow | -
Scroll backward one line | - | UpArrow
Search for a pattern | /string | /string
Display next node in topic | n | -
Repeat previous search forward | / then Enter | n
Display previous node in topic | p | -
Repeat previous search backward | - | N
Quit the program | q | q

## Lab 6 - Understanding Program Documentation <a name="LAB6"></a> ([Back to Index](#INDEX3))

Please refer to [Activities](https://github.com/ComplexSec/secure-systems-admin/tree/main/Activities) for the lab exercises

## Introducing Package Documentation <a name="PACKAGE"></a> ([Back to Index](#INDEX3))

Developers may choose to include documentation in their application's RPM distribution package. When the package is installed, files recognized as documentation are moved to `/usr/share/doc/<packagename>`. GNU packages also use /usr/share/doc to supplement info nodes

Most packages include files describing package distribution licensing - some include extensive PDF or HTML based documentation

Some packages come with extensive samples, config file templates, scripts, tutorials or user guides

## Lab 7 - Research Documentation under /usr/share/doc <a name="LAB7"></a> ([Back to Index](#INDEX3))

Please refer to [Activities](https://github.com/ComplexSec/secure-systems-admin/tree/main/Activities) for the lab exercises

## Using redhat-support-tool to Search Knowledge Base <a name="REDHAT"></a> ([Back to Index](#INDEX3))

The Red Hat Support Tool utility __redhat-support-tool__ provides a text console interface to the subscription-based Red Hat access services - internet access is required and can be used from any terminal or SSH connection

By default, the program launches in shell mode - use the provided __help__ sub-command to see all available commands. Shell mode supports tab completion and the ability to call programs in the parent shell

When first ran, it asks for credentials. It asks to store account info in home directory - __~/.redhat-support-tool/redhat-support-tool.conf__. If a RedHat account is shared, the `--global` option can save account information to `/etc/redhat-support-tool.conf`

The tool allows subscribers to search and display the same knowledge seen when on the RHCP. Knowledge Base permits keyword searches. Users can enter error codes, syntax from log files or any mix of keywords to produce a list of relevant solutions

## Directly Access Knowledge Base Articles by Document ID <a name="DIRECT"></a> ([Back to Index](#INDEX3))

Locate online articles directly by using the tool's `kb` command with the document ID. Returned documents scroll on the screen without pagination allowing a user to redirect the output.

![](/images/kb.png)

Documents retrieved in unpaginated format are easy to print, convert to PDF or others or to redirect output

## Using redhat-support-tool to Manage Support Cases <a name="SUPPORT"></a> ([Back to Index](#INDEX3))

Before contacting Red Hat Support, gather relevant info for a bug report:

1. Define the problem

Be able to clearly state the problem and its symptoms. Be as specific as possible and detail the steps which will reproduce the problem

2. Gather background information

Things like version and product. Be ready to provide relevant diagnostic information. This can include output of __sosreport__. For kernel problems, this could include the system's __kdump__ crash dump or a digital photo of the kernel backtrace displayed on the monitor of a crashed system

3. Determine the severity level

Red Hat uses four severity levels - __Urgent__ and __High__ severity problem reports should be followed by a phone call to the relevant local support center

Severity | Description
------------ | -------------
Urgent (Severity 1) | A problem that severely impacts your use of the software in a production environment. The situation halts your business operations and no procedural workaround exists
High (Severity 2) | A problem where the software is functioning but your use in a production environment is severely reduced. The situation is causing a high impact to portions of your business operations and no procedural workaround exists
Medium (Severity 3) | A problem that involves partial, non-critical loss of use of the software in a production environment or development environment. For production environments, there is a medium-to-low impact on your business, but your business continues to function, including by using a procedural workaround. For development environments, where the situation is causing your project to no longer continue or migrate into production
Low (Severity 4) | A general usage question, reporting of a documentation error, or recommendation for a future product enhancement or modification. For production environments, there is low-to-no impact on your business or the performance or functionality of your system. For development environments, there is a medium-to-low impact on your business, but your business continues to function, including by using a procedural workaround. 

## Managing A Bug Report with redhat-support-tool <a name="BUG"></a> ([Back to Index](#INDEX3))

Subscribers may create, view modify and close Red Hat Support cases using redhat-support-tool. When support cases are opened users may include files or documentation such as diagnostic reports. The tool uploads and attaches files to online cases.

Case details including product, version, summary, description, severity and case group may be assigned with command options or letting the tool prompt for required information

![](/images/cases.png)

## Including Diagnostic Information by Attaching a SoS Report Archive <a name="SOSREP"></a> ([Back to Index](#INDEX3))

Including diagnostic information when a support case is first created contributes to quicker problem resolution. The __sosreport__ command generates a compressed tar archive of diagnostic information gathered from the running system. The __redhat-support-tool__ prompts to include one if an archive has been created previously

![](/images/sos.png)

If a curren SoS report is not already prepared, an admin can generate and attach one later, using the tool's __addattachment__ command as advised previously

Support cases can also be viewed modified and closed by you as the subscriber

![](/images/listcases.png)

The Red Hat Support Tool has advanced application diagnostic and analytic capabilities. Using kernel crash dump core files, __redhat-support-tool__ can create and extract a backtrace - a report of the active stack frames at the point of a crash dump

The tool also provides log file analysis. Using the tool's __analyze__ command, log files of many types including OS, JBoss, Python, Tomcat, oVirt and others can be parsed to reconggized problem symptoms which can then be viewed and diagnosed indidivualy

## Lab 8 - Using __sosreport__ Command to Generate a SoS Report <a name="LAB8"></a> ([Back to Index](#INDEX3))

Please refer to [Activities](https://github.com/ComplexSec/secure-systems-admin/tree/main/Activities) for the lab exercises

## Lab 9 - Research Methods Used by Sys Admins <a name="LAB9"></a> ([Back to Index](#INDEX3))

Please refer to [Activities](https://github.com/ComplexSec/secure-systems-admin/tree/main/Activities) for the lab exercises

</p>
</details>

<details><summary>Module 4 - Creating, Viewing and Editing Text Files </summary>
<p>

# Table of Contents <a name="INDEX4"></a>

1. [Standard Input, Standard Output and Standard Erro](#STDIN)
2. [Redirecting Output to a File](#REDIRECT)
3. [Example for Output Redirection](#EXAMPLES)
4. [Constructing Pipelines](#PIPE)
5. [Pipeline Examples](#PIPELINE)
6. [Pipeline, Redirection and Tee](#TEE)
7. [Pipeline Examples Using the tee Command](#TEEX)
8. [Pipeline Knowledge Quiz](#QUIZ)
9. [Editing Files with Vim](#VIM)
10. [Rearranging Existing Text](#YANK)

![](/images/5.jpg)

## Standard Input, Standard Output and Standard Error <a name="STDIN"></a> ([Back to Index](#INDEX4))

A running program - or __process__ - needs to read input from somewhere and write output to the screen or to files. A command run from the shell prompt normally reads its input from keyboard and sends output to terminal

A process uses numbered channels called __file descriptors__ to get input and send output. All processes have three file descriptors:

1. Standard input (0) reads input from the keyboard
2. Standard output (1) sends normal output to the terminal
3. Standard error (2) sends error messages to the terminal

If a program opens separate connections to other files, it may use higher-numbered file descriptors

## Redirecting Output to a File <a name="REDIRECT"></a> ([Back to Index](#INDEX4))

__I/O redirection__ replaces the default channel destinations with file names representing output files or devices - process output and error mesages can be captured as file contents, sent to a device or discarded

Redirecting __stdout__ suppresses process output from appearing on the terminal. Redirecting only __stdout__ does not suppress __stderr__ error messages. If the file does not exist, it gets created. The special file __/dev/null__ quietly discards channel output 

Usage | Explanation
------------ | -------------
>file | Redirect stdout to overwrite a file
>>file | Redirect stdout to append to a file
2>file | Redirect stderr to overwrite a file
2>/dev/null | Discard stderr messages by redirecting to /dev/null
>file2>&1 OR &>file | Redirect stdout and stderr to overwrite the same file
>>file2>&1 OR &>>file | Redirect stdout and stderr to append to the same file 

The order of redirection operations is important. The sequence `> file 2>&1` redirects standard output to file and then redirects standard error to the same place as standard output

The sequence `2>&1 > file` redirects standard error to the default place for standard output and then redirects only standard output to file

Some people prefer to use the merging redirection operators

1. `&>file` __instead of__ `>file 2>&1`
2. `&>>file` __instead of__ `>>file 2>&1`

## Example For Output Redirection <a name="EXAMPLES"></a> ([Back to Index](#INDEX4))

1. Save a timestamp for later reference

	`date > /tmp/saved-timestamp`

2. Copy the last 100 lines from a log file to another file

	`tail -n 100 /var/log/dmesg > /tmp/last-100-boot-messages`

3. Concatenate four files into one

	`cat file1 file2 file3 file4 > /tmp/all-four-in-one`

4. List the home directory's hidden and regular file names into a file

	`ls -a > /tmp/my-file-names`

5. Append output to an existing file

	`echo "new line of information" >> /tmp/many-lines-of-information`
	`diff previous-file current-file >> /tmp/tracking-changes-made`

6. Redirecting errors to a file while viewing normal comand output

	`find /etc -name passwd 2> /tmp/errors`

7. Save process output and error messages to separate files

	`find /etc -name passwd > /tmp/output 2> /tmp/errors`

8. Ignore and discard error messages

	`find /etc -name passwd > /tmp/output 2> /dev/null`

9. Store output and generated errors together

	`find /etc -name passwd &> /tmp/save-both`

10. Append output and generated errors to an existing file

	`find /etc -name passwd >> /tmp/save-both 2>&1`

## Constructing Pipelines <a name="PIPE"></a> ([Back to Index](#INDEX4))

A __pipeline__ is a sequence of one or more commands separated by the pipe character - it connects standard output to standard input of next command

Pipelines allow the output of a process to be manipulated and formatted by other processes before it is output to the terminal

## Pipeline Examples <a name="PIPELINE"></a> ([Back to Index](#INDEX4))

`ls -l /usr/bin | less` takes the output of ls and uses less to display it on the terminal

`ls | wc -l` takes output of ls and gets piped to wc -l which counts the number of lines 

`ls -t | head -n 10 > /tmp/ten-last-changed-files` takes the output of ls, takes the first 10 lines of that output and redirects the final output to a file

## Pipeline, Redirection and Tee <a name="TEE"></a> ([Back to Index](#INDEX4))

When redirection is combined with a pipeline, the shell first steps up the entire pipeline, then it redirects input/output - this means if output redirection is used in the middle of a pipeline, the output will go to the file and not to the next command in the pipeline

The example `ls > /tmp/saved-output | less` takes the output of the ls command and puts it in the file and less will display nothing on the terminal

The `tee` command is used to work around this - it copies its standard input to its standard output and will redirect its standard output to the files named as arguments

## Pipeline Examples Using the tee Command <a name="TEEX"></a> ([Back to Index](#INDEX4))

`ls -l | tee /tmp/saved-output | less` redirects the output of ls to the file and passes it to less to be displayed on the terminal

If tee is used at the end of a pipeline, the final output of a command can be saved and output to the terminal at the same time

`ls -t | head -n 10 | tee /tmp/ten-last-changed-files` 

The following example is more sophisticated - it takes advantage of a special device file that exists that represents the terminal. The name of the device file for a particular terminal can be determined by running the __tty__ command at its shell prompt. Then __tee__ can be used to redirect output to that file to display it on the terminal window, while standard output can be passed to some other program through a pipe. In this case, mail will email the output

`ls -l | tee /dev/pts/0 | mail student@desktop1.example.com`

## Pipeline Knowledge Quiz <a name="QUIZ"></a> ([Back to Index](#INDEX4))

Result Needed | Redirection Syntax Used
------------ | -------------
Display command output to terminal, ignore all errors | 2>/dev/null
Send command output to file; errors to different file | >file 2>file2
Send output and errors to the same new, empty file | &>file
Send output and errors to the same file, but preserve existing content | >>file 2>&1
Run a command, but throw away all possible terminal displays | &>/dev/null
Send command output to both the screen and a file at the same time | | tee file
Run command, save output in a file, discard error messages | > file2> /dev/null

## Editing Files with Vim <a name="VIM"></a> ([Back to Index](#INDEX4))

A key design principle of Linux - information is stored in text-based files. Text files include both __flat files__ with rows of similiar information such as configuration files in /etc and __Extensible Markup Language (XML)__ fles which define data structure through text tags seen in application configuration files throughout both /etc and /usr

__Vim__ is highly configurable and efficient - split screen editing, color formatting, and highlighting for editing text

Vim starts up in __command mode__ which is used for navigation, cut and paste, and other text manipulation

Press `i` enters insert mode where all text typed becomes file content - pressing `Esc` returns to command mode

Pressing `v` enters visual mode, where multiple characters may be selected for text manipulation. Use `V` for multi-line and `Ctrl+V` for block selection. The same keystroke used to enter visual mode is used to exit

Pressing `:` begins extended command mode for tasks like writing the file to save it, and quitting the Vim editor

Pressing `u` inside insert mode undoes mistaken edits

Pressing `x` deletes a selection of text

To save or exit, `:w` saves the file and remains in command mode, `:wq` saves and quits Vim and `:q!` quits Vim and discards all file changes

## Rearranging Existing Text <a name="YANK"></a> ([Back to Index](#INDEX4))

In Vim, copy and paste is known as __yank__ and __put__ using command characters `y` and `p`. Begin by positioning the cursor on the first character to be selected and enter visual mode. Use the arrow keys to expand the visual selection. When ready, pres `y` to yank the selection into memory. Position the cursor at the new location, then press `p` to put the selection at the cursor

