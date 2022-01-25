# Complete intro to linux and the cli

## What Is Linux?
Just like Windows, iOS, and Mac OS, Linux is an operating system. In fact, one of the most popular platforms on the planet, Android, is powered by the Linux operating system. An operating system is software that manages all of the hardware resources associated with your desktop or laptop. To put it simply, the operating system manages the communication between your software and your hardware. Without the operating system (OS), the software wouldn?t function.

## Unix
Linux is considered a Unix-like operating system which basically means that Linux derives heavy inspiration from Unix without actually conforming to be a full Unix operating system. macOS and FreeBSD would be two more examples of a Unix-like operating system. Linux isn't directly Unix, just directly inspired by it.

## Why Linux
First, it's free. Anyone can use Linux to do anything without paying anyone a dime. This is useful for college students who don't have any money but it's also critical for large businesses running thousands or tens-of-thousands of servers. It can save them millions of dollars to not have to pay for an operating system.

a few things you need to know why linux:
1. it's free.
2. It's very well maintained.
3. It runs just about anywhere.
4. Most of the the things you need already exist for it.
5. The knowledgebase for Linux is enormous.

# The CLI
## Anatomy of a CLI Command
What you're looking at is often called a REPL, a Read Evaluate Print Loop. It's basically an interactive way of programming where you're writing one line of code at a time, feeding data in and out of little programs. Using commands here, you can navigate around you computer, read and write data, make network calls, and all sorts of other stuff. Basically most anything you can do with a desktop you can do with a command line, it's just a little less obvious how to do it.

The way a REPL works is that you send one command at a time and the shell runs the command and returns to you a result. During the course of running that one command, it may print some things out. And you can, using some rudimentary programming syntax, write a line that runs multiple times (or, another way of saying "runs multiple times" is looping.) That's it! That's whole concept of what we're going to learning today.

## Shells and Emulators
The first thing we should do is get some terminology out of the way. You are using a shell right now, and that shell is almost certainly called bash.

There are other shells and we'll talk more about them later, the most common of which are zsh, ash, PowerShell, and cmd.exe. We'll chat about those later.

Your shell is running inside some sort of emulator. That emulator could be Terminal.app or iTerm2 if you're on macOS, or it could be the Windows Terminal if you're on Windows 10. This the window that's containing the shell, and you can use that emulator to switch out what shell is running inside of it. For now we want to be on bash (or zsh is basically the same too.)

## File System
The way bash works is that you are always in a folder somewhere on your computer. Think of it like your computer's File Explorer or Finder: you can navigate into and out of folders while you look for files.

Our first command we're going to run in your computer is pwd. So type pwd and hit enter. This will send the command pwd to the shell which will evaluate that and print out the answer.

pwd is a little program that tells you the current path of where you are in the file system. pwd stands for present working directory. It's basically like asking the computer "where am I right now?" Mine says /home/ubuntu. I am inside of the ubuntu folder which itself is inside of the home directory. The terms folder and directory are interchangeable and I say both all the time.

## Help
I forget all the time how to use various different programs. pwd is very simple but others are way more complex. For most programs, you can add --help at the end and it'll usually spit out some brief instructions of how to use the program. This one isn't super necessary right now but go ahead and type pwd --help to see its help text. --help is called a flag. We'll talk more about those later.



## Navigating Around
So right now we're in the home directory of the ubuntu user if you've been following along with me. Every user gets their own folder in the /home folder. Since our user is named ubuntu, they have their own folder called ubuntu. Let's first see if we have any files inside of our home directory. Type ls and hit enter. ls stands for list, and it means show me everything inside of the folder where I am.

## Arguments / Parameters
In the case of `cd`, we're passing data into `cd` to tell it how to run. If we run `cd ..`, the `..` is an argument or parameter. Not all programs need parameters or sometimes they're optional. Let's look at pwd it never needs any arguments. Or ls which has optional arguments. If you say ls, it's the same as saying `ls ..` The `.` in this case means "this directory". which will tell you the path to where the program you're running is. Arguments are just bits of information you give to a program, frequently they're paths to files or folders but they can often be other things.

## Flags
`--help` which is a flag but this commands can take all sorts of flags to customize how they'll act. Like parameters, they're bits of information that change how the command works. Many programs allow you to be lazy and combine flags together. In this case, we can say `ls -la` and that's the same as `ls -a -l` (order doesn't matter either.) This is usually true but it depends on the individual command you're running.

## Editors
Nano is included on just about every Linux/Unix-like OS and is frequently the default text editor, due its tiny size, light weight, and permissive license.

Let's try now, type `nano textfile.txt`. This will create a new file called `textfile.txt` in the directory in your folder. Type something in there and take a look at the bottom bar and you'll see a bunch of available actions.
