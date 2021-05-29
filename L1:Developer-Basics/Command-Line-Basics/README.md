# Command Line Basics I: Basics

## What is shell?

Computers understand the language of zeros and ones known as binary language. In the early days of computing, instructions were provided using binary language, which is difficult for all of us to read and write. Therefore, in an operating system, there is a special program called the shell. The shell accepts human-readable commands and translates them into something the kernel can read and process.

* The shell is a user program or it is an environment provided for user interaction.
* It is a command language interpreter that executes commands read from the standard input device such as a keyboard or from a file.
* The shell gets started when you log in or open a console (terminal).
* Quick and dirty way to execute utilities.
* The shell is not part of the system kernel but uses the system kernel to execute programs, create files, etc.
* Several shells are available for Linux including:
    * BASH ( Bourne-Again SHell ) - The most common shell in Linux. It's Open Source.
    * CSH (C SHell) - The C shell's syntax and usage are very similar to the C programming language.
    * KSH (Korn SHell) - Created by David Korn at AT & T Bell Labs. The Korn Shell also was the base for the POSIX Shell standard specifications.
    * TCSH - It is an enhanced but completely compatible version of the Berkeley UNIX C shell (CSH).

Please note that each shell does the same job, but each understands different command syntax and provides different built-in functions. Under MS-DOS, the shell name is ```COMMAND.COM``` which is also used for the same purpose, but it is by far not as powerful as our Linux Shells are!

#### Shell Prompt

There are various ways to get shell access:
* **Terminal** - Linux desktop provides a GUI based login system. Once logged in you can gain access to a shell by running X Terminal (XTerm), Gnome Terminal (GTerm), or KDE Terminal (KTerm) application.
* **Connect via secure shell (SSH)** - You will get a shell prompt as soon as you log in into a remote server or workstation.
* **Use the console** - A few Linux system also provides a text-based login system. Generally, you get a shell prompt as soon as you log in to the system.

#### How do I find out my current shell name?

To find all of the available shells in your system, type the following command:
```
cat /etc/shells
```
In case the /etc/shells file has more than one shell listed under it, then it means that more than one shell is supported by your platform.

#### Command Line Interface (CLI)

The shell provides an interface to Linux where you can type or enter commands using the keyboard. It is known as the command-line interface (CLI). To find out your current shell-type following command.
```
echo $SHELL
ps $$
ps -p $$
```

The following sample output indicate that I am using bash shell:
```
PID TTY          TIME CMD
13931 pts/4    00:00:00 bash
```

## Unix Philosophy

The Unix philosophy is a philosophical approach to developing software based on the experience of leading developers of the Unix operating system. The following philosophical approaches also apply to Linux operating systems.
* *Do one thing and do it well* - Write programs that do one thing and do it well. Write programs to work together. Write programs to handle text streams, because that is a universal interface.
* *Everything is file* - Ease of use and security is offered by treating hardware as a file.
* *Small is beautiful.*
* *Store data and configuration in flat text files* - Text file is a universal interface. Easy to create, backup, and move to another system.
* *Use shell scripts to increase leverage and portability* - Use a shell script to automate common tasks across various UNIX / Linux installations.
* *Chain programs together to complete complex task* - Use shell pipes and filters to chain small utilities that perform one task at a time.
* *Choose portability over efficiency.*
* *Keep it Simple, Stupid (KISS).*

> To know more, read this [Unix philosophy](https://en.wikipedia.org/wiki/Unix_philosophy)


## Directory Strucuture and File System Hierarchy

![](https://learn.mountblue.io/rails/active_storage/blobs/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBdmdCIiwiZXhwIjpudWxsLCJwdXIiOiJibG9iX2lkIn19--193c69add61582fd9dee20c3405c84076dbc146c/linux-folders.jpg)

If you’re coming from Windows, the Linux file system structure can seem particularly alien. The C:\ drive and drive letters are gone, replaced by a / and cryptic-sounding directories, most of which have three-letter names.

The Filesystem Hierarchy Standard (FHS) defines the structure of file systems on Linux and other UNIX-like operating systems. However, Linux file systems also contain some directories that aren’t yet defined by the standard.

**/ – The Root Directory**

Everything on your Linux system is located under the / directory, known as the root directory. You can think of the / directory as being similar to the C:\ directory on Windows – but this isn’t strictly true, as Linux doesn’t have drive letters. While another partition would be located at D:\ on Windows, this other partition would appear in another folder under / on Linux.

**/bin – Essential User Binaries**

The /bin directory contains the essential user binaries (programs) that must be present when the system is mounted in single-user mode. Applications such as Firefox are stored in /usr/bin, while important system programs and utilities such as the bash shell are located in /bin. The /usr directory may be stored on another partition – placing these files in the /bin directory ensures the system will have these important utilities even if no other file systems are mounted. The /sbin directory is similar – it contains essential system administration binaries.

**/etc – Configuration Files**

The /etc directory contains configuration files, which can generally be edited by hand in a text editor. Note that the /etc/ directory contains system-wide configuration files – user-specific configuration files are located in each user’s home directory.

**/home – Home Folders**

The /home directory contains a home folder for each user. For example, if your user name is bob, you have a home folder located at /home/bob. This home folder contains the user’s data files and user-specific configuration files. Each user only has to write access to their own home folder and must obtain elevated permissions (become the root user) to modify other files on the system.

**/opt – Optional Packages**

The /opt directory contains subdirectories for optional software packages. It’s commonly used by proprietary software that doesn’t obey the standard file system hierarchy – for example, a proprietary program might dump its files in /opt/application when you install it.

**/root – Root Home Directory**

The /root directory is the home directory of the root user. Instead of being located at /home/root, it’s located at /root. This is distinct from /, which is the system root directory.

**/sbin – System Administration Binaries**

The /sbin directory is similar to the /bin directory. It contains essential binaries that are generally intended to be run by the root user for system administration.

**/tmp – Temporary Files**

Applications store temporary files in the /tmp directory. These files are generally deleted whenever your system is restarted and may be deleted at any time by utilities such as tmpwatch.

**/usr – User Binaries & Read-Only Data**

The /usr directory contains applications and files used by users, as opposed to applications and files used by the system. For example, non-essential applications are located inside the /usr/bin directory instead of the /bin directory and non-essential system administration binaries are located in the /usr/sbin directory instead of the /sbin directory. Libraries for each are located inside the /usr/lib directory. The /usr directory also contains other directories – for example, architecture-independent files like graphics are located in /usr/share.
The /usr/local directory is where locally compiled applications install to by default – this prevents them from mucking up the rest of the system.

**/var – Variable Data Files**

The /var directory is the writable counterpart to the /usr directory, which must be read-only in normal operation. Log files and everything else that would normally be written to /usr during normal operation are written to the /var directory. For example, you’ll find log files in /var/log.

## Command Line Basics Crash Course

[Basic Command Line - 20:33 minutes](https://www.youtube.com/watch?v=cBokz0LTizk&feature=emb_imp_woyt)

## Drills

* **Exercise** \
Create the following directory structure. (Create empty files where necessary)

```
hello
├── five
│   └── six
│       ├── c.txt
│       └── seven
│           └── error.log
└── one
    ├── a.txt
    ├── b.txt
    └── two
        ├── d.txt
        └── three
            ├── e.txt
            └── four
                └── access.log
```

* Delete all the files having the ```.log``` extension
* Add the following content to ```a.txt```

> Unix is a family of multitasking, multiuser computer operating systems that derive from the original AT&T Unix, development starting in the 1970s at the Bell Labs research center by Ken Thompson, Dennis Ritchie, and others

* Delete the directory named ```five```
* Rename the ```one``` directory to ```uno```
* Move ```a.txt``` to the ```two``` directory