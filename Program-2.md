## cd, mv and rm command
---
* The copy command makes a duplicate copy of the file or directory.
	```bash
	cp [options] <source> <destination>
	```
	Using the -r option, which stands for recursive, we may copy directories. Recursive means that we want to look at a directory and all files and directories within it, and for subdirectories, go into them and do the same thing and keep doing this.
* To move a file we use the command mv which is short for move. It operates in a similar way to cp. One slight advantage is that we can move directories without having to provide the -r option.
	```bash
	mv [options] <source> <destination>
	```
	moving and renaming can be done using mv command only
	```bash
	mv ~/Desktop/project ~/Desktop/new_project
	```
* The command to remove or delete a file is rm which stands for remove.
	```bash
	rm [options] <file>
	```
	When rm is run with the -r option it allows us to remove directories and all files and directories contained within. A good option to use in combination with r is i which stands for interactive.
	```bash
	rm -ri project
	```
	Linux has no undo feature so the destructive operations must be done with precaution
## vi command
---
Vi is a command line text editor. There are two modes in Vi. Insert (or Input) mode and Edit mode. In input mode you may input or enter content into the file. In edit mode you can move around the file, perform actions such as deleting, copying, search and replace, saving etc. A common mistake is to start entering commands without first going back into edit mode or to start typing input without first going into insert mode. If you do either of these it is generally easy to recover so don't worry too much.
```bash
vi <file name>
```
You always start off in edit mode so the first thing we are going to do is switch to insert mode by pressing i.
#### Saving and exiting
|Command(Note the capitals)| Functionality|
|--------|-------------|
|:ZZ | Save and exit|
|:q!| discard all changes, since the last save, and exit|
|:w|save file but don't exit|
|:wq|again, save and exit|
#### Navigating a file in vi
* Arrow keys - move the cursor around
* j, k, h, l - move the cursor down, up, left and right (similar to the arrow keys)
* ^ (caret) - move cursor to beginning of current line
* $ - move cursor to end of the current line
* nG - move to the nth line (eg 5G moves to 5th line)
* G - move to the last line
* w - move to the beginning of the next word
* nw - move forward n word (eg 2w moves two words forwards)
* b - move to the beginning of the previous word
* nb - move back n word
* { - move backward one paragraph
* } - move forward one paragraph

Note: If you type :set nu in edit mode within vi it will enable line numbers. I find that turning line numbers on makes working with files a lot easier.
#### Deleting content
* x - delete a single character
* nx - delete n characters (eg 5x deletes five characters)
* dd - delete the current line
* dn - d followed by a movement command. Delete to where the movement command would have taken you. (eg d5w means delete 5 words)
#### undoing
* u - Undo the last action (you may keep pressing u to keep undoing)
* U (Note: capital) - Undo all changes to the current line
## chmod command
---
Changes file mode bits

The digits you can use and what they represent are listed here:
* 0: (000) No permission.
* 1: (001) Execute permission.
* 2: (010) Write permission.
* 3: (011) Write and execute permissions.
* 4: (100) Read permission.
* 5: (101) Read and execute permissions.
* 6: (110) Read and write permissions.
* 7: (111) Read, write, and execute permissions.
## umask
---
* umask (user file-creation mode) is a Linux command that lets you set up default permissions for newly created files and folders.
## df command
---
It reports file system disk space usage

Options
* -a, --all - include pseudo, duplicate, inaccessible file systems
* -B, --block-size=SIZE scale - sizes  by SIZE before printing them; e.g., '-BM' prints sizes in units of 1,048,576 bytes;
* -h, --human-readable - print sizes in powers of 1024 (e.g., 1023M)
* -H, --si - print sizes in powers of 1000
## du command
---
Reports the size of directory trees inclusive of all of their contents and the sizes of individual files.
## touch command
---
It is used to create new and empty files. It can also be used to change the timestamps on existing files and directories.