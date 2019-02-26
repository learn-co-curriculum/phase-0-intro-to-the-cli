# CLI Essentials: Introduction

## Learning Goals

* Define "Command Line Interface"
* Describe the purpose of CLIs
* Identify differences between command-line interface, terminal emulator, and
  shell

## Introduction

Have you ever noticed in movies or TV shows that when the "awesome computer
hacker person" needs to do something _really important_, you see them typing a
lot of text on a screen and _viol&agrave;_ something seemingly magical happens?

Like this...

![hacking 1](https://curriculum-content.s3.amazonaws.com/prework/hack.gif)

or this...

![hacking 3](https://curriculum-content.s3.amazonaws.com/prework/hacking.gif)

You might have wondered what's going on there. These computer "heroes" are often
using a way of working with the computer called the "command-line interface" or
"CLI." 

Many computer users are familiar with performing actions and executing tasks
with graphical interfaces (also known as the GUI - Graphical User Interface)
like the ones provided by our operating systems (MacOSX, Windows, Linux, etc.)
and therefor find the concept of the CLI "mystical". 

Lots of people worry that using the CLI will get them in trouble - like they'll
break their computer. We'd encourage you to think about the CLI like a good
sharp kitchen knife: if you pay attention when you use it, you're going to have
a valuable ally on your side. Take your time and if you have a question, ask.

## Define "Command Line Interface"

A CLI is a console or text based representation in which the user types the
commands for viewing, handling, and manipulating files on your computer or to
operate software or devices. With a GUI, there’s control over files and the
operating system – but advanced tasks may still need to use the command line.

The CLI asks the user for a command; the user types it in; and then the computer
runs the "sentence" that was typed in and returns output or makes changes. There
are many reasons why developers may prefer the command line for doing these
tasks.

## Describe the Purpose of CLIs

With a CLI, users have all the control over file system and operating system,
and the tasks become simple. 

For example, you can ask, through the CLI, which files are located on the
`Desktop`. You can create a new folder or delete it. But on top of
file-management kinds of activities, you can also find out how busy your CPU is,
how full your hard drive is, and whether your computer can find a network path
to `flatironschool.com`. On top of this you don't have to click through several
menus to get there!

Experienced developers would say "the CLI gives you more control" or that it's
"more powerful." With a GUI you use the mouse and the keyboard to control the
file system or the operating system, which going to be slower than using the
command line once you become familiar with the commands. In a CLI, the users
only need to utilize the keyboard and may need to execute only few commands to
complete the task.

While some tasks may seem "easier" to do with a GUI, if you had a task such as
renaming 100+ files in a folder, which is a very time intensive task, renaming
100+ files in a directory can be done in less than a minute with a single
command in the command line!

Other advantages include:
* Working with computers remotely
* Managing files on a file server or web server (e.g., managing a web page)
* Automating commonly performed tasks
* Learning even more about computers

Developers love the command line and, as a result, write most developer tools
for other users of the command line. As a result, tools you will need to be a
developer will require you to use them through the command-line interface.

## Identify Differences Between Command-Line Interface, Terminal Emulator, and Shell

When you want to use the CLI, you launch a "terminal" program. That's short for
"terminal emulator." A long time ago, people only had keyboards and monitors (no
mouse or graphic interface!) that were tied to a computer that they all shared.
This monitor + keyboard device was called a "terminal." It looked like this:

![Another old school
terminal](https://curriculum-content.s3.amazonaws.com/prework/tty2.jpg "Another
Old School Terminal")

Nowadays, the "terminal" is "emulated" in software. It's "virtual." You launch
the "emulator" by opening a program called `Terminal` on OSX or something
similar on Linux or Windows. Instead of being connected to a remote computer by
a cable, your "terminal emulator" talks to the computer you're actually typing
on.

![TTY](https://curriculum-content.s3.amazonaws.com/prework/tty3.jpg)

When you launch the "terminal emulator" program, it will immediately start a
program called a _shell_ program. The _shell_ program is what actually prompts
you for input and returns the output. The shell most computers default to using
is known as `bash`.

To help keep these terms straight, here's a table

* When discussing the terminal, we mean the "terminal emulation" program, i.e.
  the thing that handles raw input and output and painting a screen. *NOTE:* it
  does not process the input for semantic meaning. Interpretation of the
  commands themselves are handled by the `shell` not the terminal. You can
  _type_ commands into the terminal, though.
* The `shell` takes input, thinks, prints things out. This is used when talking
  about the OS level mechanics. The `shell` doesn't paint the screen.
* `Terminal` is a command used only by Mac users.
* `consoles` exist in applications like Chrome and in an XTerm. It is not
  interchangeable for terminal emulation or `shell`.
* `bash` is a specific `shell` used by Unix systems (like MacOS and Linux).
* The command-line is roughly the same as `shell`. It's a style of of
  interaction with the `shell`.

## Conclusion

Although using a command line interface might seem intimidating at first as it
requires the memorization of dozens of different commands, it can be valuable
resource that makes using a computer easier. Using a command line, you can
perform almost all of the same tasks that can be done with a GUI. However, many
tasks can be performed quicker and can be much easier to automate and do
remotely. You can use CLI, or GUI or both to become a more skilled computer
user.

## Resources

- [Lifehacker on the Command Line](http://lifehacker.com/5633909/who-needs-a-mouse-learn-to-use-the-command-line-for-almost-anything)
- [Command Line Interface (CLI) vs. Graphical User Interface (GUI)](https://www.cybrary.it/0p3n/command-line-interface-cli-vs-graphical-user-interface-gui/)
