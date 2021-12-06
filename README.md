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

!ls](/assets/img/ls.jpg)

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
















