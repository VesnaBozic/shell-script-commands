# Shell Script Basic

## Content

- [What is the difference between the graphical file explorer and the command-line shell?](#what-is-the-difference-between-the-graphical-file-explorer-and-the-command-line-shell)
- [Where are we in terminal?](#where-are-we-in-terminal)
- [What is version control system?](#what-is-version-control-system)
- [What are absolute and relative path?](#what-are-absolute-and-relative-path)
- [What is in there?](#what-is-in-there)
- [How to move?](#how-to-move) 
- [How to move up in directory?](#how-to-move-up-in-directory) 
- [What is tilde ~ ?](#what-is-tilde-~) 
- [Coping files](#coping-files) 
- [How to move a file?](#how-to-move-a-file)
- [Rename files](#rename-files) 
- [How to delete file?](#how-to-delete-file) 
- [How to delete directory?](#how-to-delete-directory)
- [Create directory](#create-directory) 
- [Tmp directory](#tmp-directory) 
- [How to see a file's content?](#how-to-see-a-file's-content) 
- [Use less to see page output](#use-less-to-see-page-output) 
- [How to see first few lines in a file?](#how-to-see-first-few-lines-in-a-file)
- [How to see everything that exist in directory?](#how-to-see-everything-that-exist-in-directory) 
- [HELP](#help)
- [REPEATING COMMANDS](#repeating-commands)

Windows, Linux or Mac Os are operating systems that are controling the computer's processor, hard drive, network connection and they run other programs.

Humans, when doing something on the computer, he interacts with the operating system. Today computers have a pretty self-explanatory graphical interface. With double-clicks into commands, we can open, delete, create a new folder.

Before computers had graphical interfaces, though, people typed instructions into a program called a command-line shell. Each time a command is entered, the shell runs some other programs, prints their output in human-readable form, and then displays a prompt to signal that it's ready to accept the next command. (Its name comes from the notion that it's the "outer shell" of the computer.)

## What is the difference between the graphical file explorer and the command-line shell?

> They are both interfaces for issuing commands to the operating system.

## Where are we in terminal?

![pwd](/assets/img/pwd.jpg)

with 

```
pwd
```

we can find out where we are in the filesystem. Pwd - print working directory

> ***pwd*** prints the apsolute path of our current working directory, which is where the shell runs commands and looks for files by default

## What are absolute and relative path?

* An ***absolute path*** is defined as specifying the location of a file or directory from the root directory(/). In other words,we can say that an absolute path is a complete path from start of actual file system from / directory.

> An absolute path has the same value no matter where you are.

* ***Relative path*** is defined as the path related to the present working directly(pwd). It starts at your current directory and never starts with a / .

> A relative path specifies a location starting from where you are.

The shell decides if a path is absolute or relative by looking at its first character: If it begins with /, it is absolute. If it does not begin with /, it is relative.

## What is in there?

![ls](/assets/img/ls.jpg)

with command

```
ls
```
we can find out what is in our current directory.

> ls - short for listing

## How to move?

![cd](/assets/img/cd.jpg)

with 

```
cd
```

we can move around. It stands for "change directory".


## How to move up in directory?

![cd](/assets/img/cd.jpg)

The parent of a directory is the directory above it.

>in the example above Shell is parent of assets

We can always move around using absolute paths.

but with 

```
..
```

or 

```
cd ..
```
we can move one directory above the one we are currently in. So in parent directory.

A single dot

```
.
```

always means current directory.

So if do

```
ls .
```

is same as just

```
ls
```

## What is tilde ~ ?

> it means your home directory.

```
ls ~
```

will always list content of out home directory no matter where we are

and

```
cd ~
```

will always take as home.

![home](/assets/img/home.jpg)

## Coping files

with 

```
cp
```

we can copy files, move them to other directories, organize or rename thame.

> cp stands for Copy


comand
```
cp original.txt duplicate.txt
```

if original.txt will create a copy called duplicate.txt
if there already was a file called duplicate.txt it will be overwritten.

command with last parameter is an existing directory

``` 
cp folder/original.txt folder/duplicate.txt folder2
```

will copy all the fils into folder2


## How to move a file?

with 
```
mv
```

we can move file from one dorectory to another

```
mv first.txt second.txt ..
```

will move files first.txt and second.txt from current working directory to its parent directory

## Rename files

```
mv name.txt newName.txt
```

name.txt is "moved" to the newName.txt

> mv will like cp overwrite existing files

## How to delete file?

we use command

```
rm
```

> it stands for remove

```
rm file1.txt file2.txt
```

will remove both file1.txt and file2.txt

rm removes files and it can't be reversed since the shell doesn't have trash can.

## How to delete directory?

```
rmdir directory
```

this command only works wheb=n directory is empty.
To use this command we would have to delete all files in directory before deleting directory.

## Create directory

```
mkdir directoryName
```

## Tmp directory

/tmp directory  is where people and programs often keep files they only need briefly. (Note that /tmp is immediately below the root directory /, not below your home directory.)


## How to see a file's content?

```
cat README.md
```

will print the contents of files onto the screen

![cat](/assets/img/cat.jpg)

> cat is short form concatenate meaning to link things together, since it will print all the files whose names we give it one after another.


## Use less to see page output

We can use cat to print large files and then scroll through the output, but we can use 

``` 
less file1.txt file2.txt
```

to display one page at the time

press ***spacebar*** to page down

press ***q*** to quit

press ***:n*** (colon and lower-case n) to move to the next file

press ***:p*** to go back to previous file

## How to see first few lines in a file?

A quick way to figure out what it contains is to look at the first few rows.

We can do this in the shell using a command called ```head```.

As its name suggests, it prints the first few lines of a file (where "a few" means 10), so the command:

```
head file1.txt
```

would display first ten line of the file.

if we write in command flag -n (number of lines)

```
head -n 3 file1.txt
```

it will display only first three lines of the file


## How to see everything that exist in directory?

if we give -R (recursive) flag to the command

```
ls -R
```

it will show every file and directory in the current level, and everything is each subdirectory and so on.

## HELP

To find out what commands do we use ```man``` command, short from manual

```
man head
```

show us informations about head

use spacebar to page throught the information

```q```` for quit

## REPEATING COMMANDS

We can use up-arrow key to cycle back trough commands that we used

or with command

```
history
```

we can see list of commands that we used recently

and with 
```
!2
```

where 2 is number of command that we want to re-run

## GREP

Grep selects lines according to what they contain.

```grep``` takes a piece of text followed by one or more filenames and prints all of the lines inthose files that contain that text.

```
grep something file.txt
```

print all of the lines from file.txt that contain "something"

## GREP FLAGS

- ```c```  print a count of matching lines rather than the lines themselves
- ```h```  do not print the names of files when searching multiple files
- ```i```  ignore case (e.g., treat "Regression" and "regression" as matches)
- ```l```  print the names of files that contain matches, not the matches
- ```n```  print line numbers for matching lines
- ```v```  invert the match, i.e., only show lines that don't match

## Storing output in a file

We can redirect any command's output anywhere we want.

```
head -n 5 file1.txt > file2.txt
```

will write first 5 lines from file1.txt write into a new file called file2.txt

Sign ```>``` tells the shell to redirect output to a file.
It will work with every shell output.











































