# Chapter 1 : Open Source Community

## Open Source Philosophy
Open Source is a software development movement that encourages on open collaboration, freely development .. belief that the source code of software should be available to anyone & this movement has improved the software industry to an unlimited way.


## Open Source Community ASU

Open source Community ASU is a community started in 2013, with a group of students who were passionate about the idea of open source, linux & software development.

Our vision & duty is to spreed the importance of using open source tools & developing your softskills, as a way to improve your skills for your career path.


### Here's Fun Facts about us: 

- We started with only 7 students (Geeks) in 2013, at "Said Abdelwahab Hall" with labtobs & banners: telling other students about LINUX, why to use it & any Linux support for them.

- We are not only a technical community, we also have committees for soft skills & designing (10 committees in total) such as:
    - Blender 3D committee 
    - Ui/Ux & Design committee
    - Content Creation committee (CCC)

- We usually held events & workshops:
    - Get to Git' & Get to Linux' events
    - Linux Distributions Party
    - El Salakhana 
    - OSC Summer Training
    - Docker Workshop - last MidYear holiday 2024
    - Technical Workshops: Linux | Game development | Web 
    - Non-Technical Workshops: Blender | Ux & Design | CCC workshops 


- We are the community who created "The Employment Fair" 1st edition in 2017, it was held in FCIS then replaced in the university campus.

Then days after days, Years after years, here we are celebrating our 10s year, hope to give more value for open source & Ain Shams community.

---
---
---

# Chapter 2 : Linux History

## Difference between OS and Kernel

### ●  What is the Operating system (OS):
Is system program that provides interface between user and computer .. as it manages all the software(SW) & hardware(HW) on the computer.

### How OS manages apps:
there are several different computer programs running at the same time, need to access your computer's central processing unit (CPU), memory, and storage .. so OS coordinates all this to make sure every program gets only it's need. 

---

### ● What is Kernel & How it works:

A kernel is the core component of the operating system.

- It's the first program of operating system that is loaded into the main memory to start the working of system .. and remains in memory till the system is shut down.

- Kernal acts as a bridge between application SW & HW of the system .. as it directly communicates with the HW & let it know which SW app has requested.

.
![OS-Kernal Photo](https://raw.githubusercontent.com/SalmaAlassal/BeRoot/main/Introduction%20to%20Linux/imgs/OS-Kernel.png) 

.
### ● Kernel Creator:

Kernal has been created by one of the greatest developers ever called: Linus Torvalds 

But linux OS itself was created by a collaboration work by: GNU & Linus.

But the question here, What is GNU?

### ● What's GNU:

GNU is an acronym for: GNU’s Not UNIX. The founder of the GNU project is Richard Stallman.

The GNU project is a replacement for UNIX, was created to produce a free software alternative to Unix, and were able to produce most of the programs of the OS but not the Kernel (it was hard to implement acually).

### ●  Popular Linux Distributions:

- Ubuntu
- Fedora OS
- Linux Mint
- Pop_OS!
- Red Hat Linux
- Arch
- Manjaro

### Diffrences between distros are deppending on what you want to do, For Example: 
 - Usual users (Ubuntu)
 - Developer (Most of Linux Distros: Ubuntu, Fedora, Debian)
 - Artists & music production (Arcolinux)
 - Coporate org. (Red Hat Linux)
 - Lightweight flexible Linux distr (Arch Linux)
 - Cyper Security specialists (Kali Linux)

---
---
---

# Chapter 3 : Introduction to the Command Line

## Introduction to the Command Line
### What is the Shell?
When we speak of the command line, we are really referring to the shell. The shell is a
program that takes keyboard commands and passes them to the operating system to carry
out. Almost all Linux distributions supply a shell program from the GNU Project called
bash.
___
### Some Commands

* **echo** : Display a line of a text.  
**Syntax** : echo [option] [text]    
```
 OSC@OSC:~$ echo Hello World
 Hello World
 ```

| Command                  | Description |
|--------------------------|-------------|
| `echo "text" > filename` | redirects the output of echo to a specific file creating the file if it does not exist and overwriting it if it does.|
|`echo "text" >> filename`|appends the text to a specific file| 

|Option |Usage|
|--------|-----|
|-n |    do not output the trailing newline|
|-e|  enable interpretation of backslash escapes|
| -E  |   disable interpretation of backslash escapes (default)|  
```
OSC@OSC:~$ echo -n "Hello, "
echo "World!"
Hello, World!
```
```
OSC@OSC:~$ echo -e "Hello\nWorld"
Hello
World
```
```
OSC@OSC:~$ echo -E "Hello\nWorld"
Hello\nWorld
```



* **clear** : Clear the screen.   
**Syntax** : `clear`.

Before:
```
 OSC@OSC:~$ echo Hello World
 Hello World
 OSC@OSC:~$ clear
 ```
  
After:
```
 OSC@OSC:~$ 



 ```



___
### Navigation Commands
#### Absolute & Relative Paths
##### Absolute Path :  
An absolute pathname begins with the root directory and follows the tree branch by branch until the path to the desired directory or file is completed.  
For example, there is a directory on our system in which most of our system's programs are installed. The directory’s pathname is /usr/bin. This means from the root directory (represented by the leading slash in the pathname) there is a directory called "usr" which contains a directory called "bin".
```
 OSC@OSC:~$ cd /usr/bin
 OSC@OSC:/usr/bin$ pwd
 /usr/bin
 OSC@OSC:/usr/bin$
 ```

##### Relative Path :
 Where an absolute pathname starts from the root directory and leads to its destination, a relative pathname starts from the working directory.  
  * The "." notation refers to the working directory and the ".." notation refers to the working directory's parent directory.  
  
  *  the working directory here is "usr"
  ```
  OSC@OSC:/usr/$ cd ./bin
 OSC@OSC:/usr/bin$ pwd
 /usr/bin
 ```
   
 *  In almost all cases, we can omit the "./"  
 ```
  OSC@OSC:/usr/$ cd bin
 OSC@OSC:/usr/bin$ pwd
 /usr/bin
 ```

 ___
 ### Some Commands
 * **pwd** : Prints the absolute path of the current working directory.  
 **Syntax** : `pwd`.  

```  
  OSC@OSC:~/Downloads$ pwd
  /home/OSC/Downloads
 ```



 
   
 * **ls** : List directory contents.  
 **Syntax** : `ls [option] [file]`
 ```. 
  OSC@OSC:~$ ls
  Desktop  Documents  Downloads  Music  Pictures  Public  Templates  Videos
 ```
 * Besides the current working directory, we can specify the directory to list:
 ```
 OSC@OSC:~$ ls /home
 OSC
 ```
 | Option | Usage |
|--------|-------|
|-l|displays detailed information about files|
|-a|list all files including the hidden files|
|-t|Sort files by modification time, with the newest files appearing first|
|-r|Reverse the order of the sort to display files in reverse order|
|-S|Sort files by size, with the largest files appearing first|
 
* **cd** :  Change directory.  
To change our working directory (where we are standing in our tree-shaped maze) we use
the cd command.  
**Syntax** : `cd path_name(absolute or relative)`. 
``` 
 OSC@OSC:~$ cd /home/OSC/Downloads
 OSC@OSC:~/Downloads$
```
 * Now ,our working directory here is Downloads.

 | Command | Usage |
|--------|-------|
| `cd ..` | Change the current working directory to the parent directory of the current directory|
| `cd` | Change the working directory to your home directory|
|`cd -` |Changes the working directory to the previous working directory|
|`cd ~user_name` |Changes the working directory to the home directory of user_name|
 ___
 ### Exploring Commands
 * **cat** : Display contents of a file,concatenate files and print on the standard output.  
 **Syntax** : `cat [option] [file]
`.
 ```
  OSC@OSC:~/Documents$ cat myFile
  hello world
 ```
 | Option | Usage |
|--------|-------|
|-n| Number the lines of the output|
|-s| suppress repeated empty output lines|
|-E| Display a dollar sign ($) at the end of each line|

 
 * **file** : Determine file type.   
 **Syntax** : `file file_name`.
 ```
  OSC@OSC:~/Documents$ file myFile
  myFile: ASCII text
 ```
     
 * **type** :it is used to find out whether it is built-in or external binary file.  
 **Syntax** : type file_name.  
 ```
  OSC@OSC:~$ type cd
  cd is a shell builtin
 ```

---
---
---

# Chapter 4: Understanding the File System 

- In Linux, most of the operations are performed on files. And to handle these files Linux has directories also known as folders which are maintained in a tree-like structure. Though, these directories are also a type of file themselves. 
  
- *Linux has 3 types of files:*
    - **Regular Files:** It is the common file type in Linux. it includes files like – text files, images, binary files, etc. Such files can be created using the `touch command`. They consist of the majority of files in the Linux/UNIX system. The regular file contains ASCII or Human Readable text, executable program binaries, program data and much more.
    - **Directories:** These are the files that store the list of file names and the related information. `The root directory(/)` is the base of the system, `/home/` is the default location for user’s home directories, /bin for Essential User Binaries, `/boot` – Static Boot Files, etc. We could create new directories with `mkdir command`.
   - **Special Files:** Represents a real physical device such as a printer which is used for IO operations. Device or special files are used for device Input/Output(I/O) on UNIX and Linux systems. You can see them in a file system like an ordinary directory or file.
  
# Creating Directories

**1. `mkdir DirectoryName`**

- This command will create a new directory, provided it doesn't exists.
>
- You can create a new directory his name is **Test** by typing :

    ```
    osc@osc:~$ mkdir Test 
    ```

**2. `mkdir -p Directory/SubDirectory1/SubDirectory2`**

- This command will create nested directories.
>
- You can reate nested directories, **world** directory which is inside the **hello** directory which is inside the **program** directory by typing:

    ```
    osc@osc:~$ mkdir -p program/hello/world
    ```

---
# **Creating Files**

**`touch fileName`**

- This command will create a new file.
>
- To Create a new files file1.txt , file2.txt , file3.txt , you can type:

    ```
    osc@osc:~$ touch file1.txt file2.txt file3.txt
    ```

---
# Renaming & Moving Files

**1. `mv filename DirectoryDestination `** 

- This command can move a file to a new location.
>
- Move **file1** into the **Test** directory , by typing :
>
```
osc@osc:~$ mv file1 Test
```

- You can move that file back to your home directory by using the **special dot reference** to refer to the current directory. Make sure you’re in your home directory, and then run the mv command:
>
```
osc@osc:~$ cd
osc@osc:~$ mv test/file1 . 
```
**2. `mv oldFile newFile `** 

- This command is also used to rename files and directories. In essence, moving and renaming are both just adjusting the location and name for an existing item.
>
- You can rename **file1.txt** into the **file2.txt** by typing: 
>
```
osc@osc:~$ mv file1.txt file2.txt
```
---
# Copying Files & Directories

`mv` command, you could move or rename a file or directory, but you could not duplicate it. 

**1. `cp SourceFile CopyFile`** 

- This command can make a new copy of an existing item
>
- *The following command*,Copy **source.txt** file to a new file called **copy.txt**.
>
```
osc@osc:~$ cp source.txt copy.txt
```
**2. `cp -r SourceDir CopyDir`**

- Copy entire directories, you must include the `-r option` to the command. This stands for “recursive”, as it copies the directory, plus all of the directory’s contents.

- *The following command*, Copy the **test1** directory structure to a new structure called **test2**

```
osc@osc:~$ cp -r test1 test2
```
---
# Removing Directories & Files

**1) `rm filename`**

- this command could be used to delete a file. 
>
- To remove **test** file from the directory, you can type:
>
```
osc@osc:~$ rm test 
```
**2) `rmdir directoryname`**

- Remove empty directories, this will only succeed if there is nothing in the directory in question. Let's remove **example** directory within the **testing** directory:
>
```
osc@osc:~$ rmdir testing/example 
```

**3) `rm -r directoryname`**
- To remove a *non-empty* directory, you will use the rm command with the -r option, which removes all of the directory’s contents recursively, plus the directory itself.
>
- To remove the **Testing** directory and everything within it, you can type:

```
osc@osc:~$ rm -r Testing
```
>
| *Command* | *Description* |
| ---- |----|
| **`rm filename`** |Deletes a file|
| **`rm -f filename`** |Deletes by force and don't prompt the user|
| **`rm -r DirectoryName`** |Deletes a non-empty directory| 
| **`rm -d directory_name`**|Deletes an empty directory|



---

# Getting Help

**1) `man [options] [command]`**

- This command can display the manual pages (documentation) for various commands and utilities. It provides information about the command's syntax, options, usage, and often includes examples. 

- So let's view the manual page for the **ls** command (which lists directory contents), by typing:
>
```
osc@osc:~$ man ls
```
![alt text](<images/man command.png>)

**2) `apropos`**
- Apropos will list several commands that match the keyword you used. 
>
- The list includes a short description of what the command does,works by looking through the entire description sections of the man pages for the matching keyword you provide with the apropos command.
>
- The word apropos is derived from the French word "à propos" which means **"about."**
 Let's assume you want to copy a file but do not know which command to use. Simply use the apropos command followed by the task you want to complete.
>
```
osc@osc:~$ apropos copy
```
>
**3) `--help`**

Most commands have the `--help` command argument or option. You can use it to display helpful information about how a command is used and its arguments in a simplified manner.

Get more help on the **cp** command by typing:
```
osc@osc:~$ cp --help
```
![alt text](<images/--help command.png>)
