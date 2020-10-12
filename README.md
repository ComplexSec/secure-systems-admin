# Secure Systems Administration
Year 2 University module all about Linux - specifically RHEL

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
`item 1 | item 2` | Means only __one__ of them can be specified
`<filename>` | Represents variable data

</p>
</details>
