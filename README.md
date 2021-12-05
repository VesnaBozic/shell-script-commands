# Shell Script Basic

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

with command

```
ls
```
we can find out what is in our current directory.

> ls - short for listing

## How to move?

with 

```
cd
```

we can move around. It stands for "change directory".


## How to move up in directory?

The parent of a directory is the directory above it.

>in the example above Shell is parent of assets

We can always move around using absolute paths










