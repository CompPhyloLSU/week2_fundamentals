## Filesystem Structure

- [ ] The Unix root (/)
	- The very base of the filesystem
- [ ] Absolute paths
	- All absolute paths begin at the root- start with /
- [ ] Relative paths
	- dont start with /
	- Working directories
	- Shortcuts for current and parent directories
- [ ] Hidden files and folders
	- Names begin with `.`
	- Usually used for configuration files

## Practical Computing Advice

- [ ] Naming files and folders
	- CamelCaseLooksLikeThis
	- `underscores_can_work`
	- __NEVER__ use spaces!! Spaces confuse terminal 
	- Generally a good idea to avoid special characters
- [ ] Plain text files
	- Human readable
	- ASCII and UniCode
		- [ASCII on Wikipedia](https://en.wikipedia.org/wiki/ASCII)
		- [UTF-8 on Wikipedia](https://en.wikipedia.org/wiki/UTF-8)
- [ ] New line characters
	- [New Lines on Wikipedia](https://en.wikipedia.org/wiki/Newline)
- [ ] Activity Monitor
	- CPU Activity
	- Memory
	- Disk spaces
	- Jobs and IDs

## Introduction to the Command Line

- [ ] Terminal
	- Built in to Linux (and Mac OS X)
	- By default, uses the bash shell (interpreter)
	- The command prompt
	- Tab completion
	- double tap tab will list all files with that beginning
	- Scrolling through history
- [ ] Commands related to navigating the filesystem
	- 'touch filename.txt' will create file  
	- `pwd` - print working directory - or - "where am I?"
	- `ls` - list directory contents
		- 'ls -l' - long list
			- Everything has three types of permissions
				- Read
				- Write
				- Execute
			- And three groups whose permissions can be controlled
				- Owner
				- Group
				- Others
			- [Wikipedia on Unix Permissions](https://en.wikipedia.org/wiki/File_system_permissions#Notation_of_traditional_Unix_permissions)
		- la - list with hidden files
	- `cd` - change directory
		- will accept absolute or relative paths
	- `chmod` - change permissions - specify who (ugo), how (+ or -), and what (rwx)
	- `man <command>` - gives us the manual page and options for any Unix command (q will get out of manual page)
- [ ] Commands related to files and folders
	- `cp` - copies a file
		- `cp originalFile.txt newFile.txt`
	- `mv` - moves __or__ renames a file
		- To change location, use paths: `mv myFile.txt ./folder/myFile.txt`
		- To change name, just use different names: `mv myFile.txt newName.txt`
	- `cat filename.txt` - view file contents - can be called on multiple files and will conCATenate their contents
	- 'cat file1.txt file2.txt file3.txt' will show all files in command line
	- 'cat *.txt' shows all text in files with the file ending .txt
	- 'ls *.txt' show all files that end in .txt
	- 'ls ../*.txt' go up one directory then tell me the txt files there (still within the same directory)
	- can add file/filename.txt in nano
	- `head -n #` - view the first # of lines of a file
	- `tail -n #` - view the last # of lines of a file
	- `less` - view the contents of a file a little at a time nice way to scroll through
	- `touch filename.txt` - quickly create a new file
	- `nano filename.txt` - this is actually an entire text editing program (type text like normal)
	- 'write out is save' and ^=control (^O) exit (^X) 
	- `wc` - print out the length of a file in lines, words, and characters
	- `>>` - appends to file
		- echo "some text here" >> myTextFile.txt
	- `>` - writes to (or over!) file
		- echo "more text here" > myTextFile.txt
	- WARNING - BIG WARNING - PAY ATTENTION - `rm` _permanently_ removes a file
		- No going back - always use this VERY carefully
		- I know people who've accidentally erased their entire computers using this command
			- `rm -r` recursively removes a directory and everything inside it - even more dangerous than just `rm`!
		- This is the reason permissions are so important. If someone doesn't have write permissions on a file or folder, they shouldn't be able to delete it.
	- `mkdir MyDirectory` - create a new (empty) directory (folder)
	- `rmdir MyDirectory` - remove an empty directory !!WARNING!!
	- wildcards - * is especially useful - matches anything
	- `grep` - find only lines matching some particular string
	- 'cp filename.txt filename2.txt' will copy contents
	- 'mv filename filename' will change name of file
	- 'mv filename ./Biology/' will move file name into folder that is in current working directory or without './' will work too

	- [ ] Commands related to the Unix environment
		- Can create a variable and assign value using `=`
			- myVariable=2
		- Can print value of variable using `echo` and starting name with `$`
			- echo $myVariable
		- `|` - the Unix pipe can be used to send the output of one command into the input of another
			- `history | tail -n 20 >> endOfHistory.txt`


```
Use the commands you just learned to create and navigate this hierarchy of folders and 
files. This should be done entirely on the command line. Add some text content to the .txt
files after you create them.

 ~/Desktop/Biology/
				README.txt
				CellBiology/
					ImportantCellBioTopics.txt
				Ecology/
					ImportantEcolTopics.txt
				Evolution/
					ImportantEvolTopics.txt
					Phylogenetics/
```
