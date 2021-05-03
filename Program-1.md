## cd Command
---
* Switch back to previous directory where you working earlier.
	```bash
	cd -
	```
* Change Current directory to parent directory.
	```bash
	cd ..
	```
	Note: Every directory has . and .. hidden folder. The . is for the current directory and .. is for the parent directory.
* Show last working directory from where we moved (use ‘–‘ switch) as shown.
	```bash
	cd --
	```
* Move two directory up from where you are now.
	```bash
	cd ../../
	```
* Move to users home directory from anywhere.
	```bash
	cd ~
	```
	Note: Tilde is a shortcut to your home directory
* Change working directory to current working directory (seems no use of in General).
	```bash
	cd .
	```
* Navigate from your current working directory to /etc/v__ _, Oops! You forgot the name of directory and not supposed to use TAB.
	```bash
	cd /etc/v*
	```
	This will move to ‘vbox‘ only if there is only one directory starting with ‘v‘. If more than one directory starting with ‘v‘ exist, and no more criteria is provided in command line, it will move to the first directory starting with ‘v‘, alphabetically as their presence in standard dictionary.

## ls Command
---
The general syntax for a command
	```bash
	command [options] [location]
	```

#### List Files using ls with no option
ls with no option list files and directories in bare format where we won’t be able to view details like file types, size, modified date and time, permission and links etc.

#### List Files With option –l
Here, ls -l (-l is character not one) shows file or directory, size, modified date and time, file or folder name and owner of file and its permission.

#### View Hidden Files
List all files including hidden file starting with ‘.‘.

#### List Files with Human Readable Format with option -lh
With combination of -lh option, shows sizes in human readable format.

#### List Files and Directories with ‘/’ Character at the end
Using -F option with ls command, will add the ‘/’ Character at the end each directory.

#### List Files in Reverse Order
The following command with ls -r option display files and directories in reverse order.

#### Recursively list Sub-Directories
ls -R option will list very long listing directory trees. See an example of output of the command.

#### Reverse Output Order
With combination of -ltr will shows latest modification file or directory date as last.

#### Sort Files by File Size
With combination of -lS displays file size in order, will display big in size first

## mkdir and rmdir command
---
* The command mkdir creates an empty directory
The -p options tells mkdir to make parent directories as needed and the -v option makes mkdir tell us what it is doing.
* The command rmdir removes empty directories
rmdir has similar options as mkdir i.e -p, -v but the directories within should also be empty

## pwd (Print Working Directory) Command
---
Command ‘pwd‘ tells where you are – in which directory, starting from the root (/).
* Print working directory from environment even if it contains symlinks
	```bash
	pwd -L
	```
* Print actual physical current working directory by resolving all symbolic links
	```bash
	pwd -P
	```
Tip: tty command gives the pwd of the terminal.

## clear and who command
---
* clear - clears the terminal screen including its scrollback buffer.
* who - shows who is logged on
