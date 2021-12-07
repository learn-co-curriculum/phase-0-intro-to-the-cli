# Introduction to the Command Line Interface

## Learning Goals

- Define "Command Line Interface"
- Describe the purpose of CLIs
- Identify differences between command-line interface, terminal emulator, and
  shell

## Introduction

Most computer users these days are familiar with performing actions and executing
tasks using a _Graphical User Interface_ (GUI). When you use things like
MacOSX's "Finder" or Windows' "File Explorer", you're using a GUI.

Prior to the early 1990's, however, the only way to interact with a computer was
by using a _command-line interface_ (CLI). Accomplishing tasks in those days
(e.g., creating, viewing or manipulating files; launching software) required
the user to type commands into a _terminal_.

Given how prevalent GUIs are at this point, the average computer user will
probably rarely or never need to use a command line to accomplish their tasks.
The same is not true for developers, however. Learning to use a CLI will allow
you to accomplish many tasks more quickly and reliably than you can using a GUI.
Furthermore, there are some tools you will need as a developer that can only be
used through the command-line interface.

Lots of people worry that using the CLI will get them in trouble, that they'll
break their computer. We encourage you to think about the CLI like a high-quality,
sharp kitchen knife: if you pay attention when you use it, you're going to have
a valuable ally on your side.

> **WARNING**: It's true, it is easier to run dangerous commands through the CLI
> than through a GUI. Commands that list files or create directories are not
> likely to break anything. Commands that remove files or directories, however,
> _should_ be used with caution.

## Define "Command Line Interface"

A CLI is a program that allows us to have a text-based conversation with the
computer in which we type the commands for accomplishing tasks. With a CLI,
users have wide control over the file system and operating system, and the tasks
become simple. For example, you can ask, through the CLI, which files are
located on the `Desktop`. You can create a new folder or delete it. But on top
of file-management kinds of activities, you can also find out how busy your CPU
is, how full your hard drive is, and whether your computer can find a network
path to `flatironschool.com`. On top of this, you don't have to click through
several menus to get there!

Experienced developers would say "the CLI gives you more control" or that it's
"more powerful." With a GUI you use the mouse and the keyboard to control the
file system or the operating system, which is going to be slower than using the
command line (once you become familiar with the commands). In a CLI, users only
use the keyboard and may need to execute only a few short commands to complete
their equivalent GUI tasks. CLI users' fingers never leave the "home row"
(assuming they can touch type) which _adds_ to their speed.

While some tasks may seem "easier" to do with a GUI, development-like tasks are
often much more easily completed in the CLI. If you had a task such as renaming
100+ files in a folder according to a formula based on their file size, you
might well spend hours on it in the GUI. Doing the same with the CLI on your
side could be completed in seconds. And if you do that sort of thing often, you
can save that process and run it again whenever you wish! This is called
"scripting."

## Identify Differences Between Command-Line Interface, Terminal Emulator, and Shell

In the early days of computers, users didn't work on standalone, "personal"
computers. Instead, their workstation consisted of only a keyboard and monitor —
no mouse and no graphical user interface. This monitor + keyboard device was
called a "terminal," and multiple terminals were connected to a _shared_
computer called a "mainframe."

!["Mainframe Computers"](https://curriculum-content.s3.amazonaws.com/cli-essentials/bash-intro/Image_56_MainFrameDiagram.png)

Nowadays, the "terminal" is emulated in software. It's virtual. You launch the
emulator by opening a program. And instead of being connected to a remote
computer by a cable, your "terminal emulator" talks to the computer you're
actually typing on. For Mac users, the default terminal emulator program is
called **Terminal**. For WSL users, the **Ubuntu** application will act as your
"terminal."

When you launch the "terminal emulator" program, it will immediately start a
program called a _shell_ program. The _shell_ program is what actually prompts
you for input and returns the output. `bash` and `zsh` are specific `shell`s
used by Unix systems (like Mac OSX and Linux).

To summarize:

- When discussing the terminal, we mean the "terminal emulation" program, i.e.
  the thing that handles raw input and output.

- The `shell` is what handles _interpreting_ the commands you type in to the
  terminal. It takes input, thinks, prints things out. It knows when a command
  doesn't exist or make sense, and it knows how to ask the CPU to do work.

- The phrase "command-line" is roughly the same as `shell`. It's a style of
  interaction with the `shell`.

## Conclusion

Although using a command line interface might seem intimidating at first as it
requires learning dozens of different commands, it can be a valuable resource
that makes using a computer easier. Using a command line, you can perform almost
all of the same tasks that can be done with a GUI. However, many tasks can be
performed quicker and can be much easier to automate.

Ultimately though, many programming languages and programming tools assume that
you're comfortable with the CLI. You must have this comfort in order to be a
successful programmer.

## Resources

- [Lifehacker on the Command Line](http://lifehacker.com/5633909/who-needs-a-mouse-learn-to-use-the-command-line-for-almost-anything)

- [Command Line Interface (CLI) vs. Graphical User Interface (GUI)](https://www.cybrary.it/0p3n/command-line-interface-cli-vs-graphical-user-interface-gui/)
