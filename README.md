# CLI Essentials: Basic Commands in Bash

## Learning Goals

* Identify differences between command-line interface, terminal emulator, and shell
~* Demonstrate how to navigate with Bash~ KG
~* Demonstrate manipulating files in the command line~ KG

## Introduction

Have you ever noticed in movies or TV shows that when the "awesome computer
hacker person" needs to do something _really important_, you see them typing
a lot of text on a screen....

![Terminal Work](https://media.giphy.com/media/12W5Sg2koWYnwA/giphy.gif)

...and _viol&agrave;_ they save the day:

![Lex saves the day on a Unix system (she knew this!)](https://media.giphy.com/media/uMbMEyGDprR7y/giphy.gif)

And then that person is all-powerful, like:

![Neo sees "The Matrix"](https://media.giphy.com/media/fV0oSDsZ4UgdW/giphy.gif)

You might have wondered what's going on there (besides some lazy screenwriting).

The text-based way that these computer heroes are talking to the computer is called the "command-line interface" or
"CLI." The CLI asks, or "prompts," the user for a command; the user types it in; and then the
computer runs the "command" that was typed in and returns output and / or uses
the computer's resources (network card, printer, monitor).

For example, you can ask, through the CLI, which files are located on the
`Desktop`. You can create a new folder or delete it. On top of
file-management kinds of activities, you can _also_ find out how busy your CPU
is, how full your hard drive is, and whether your computer can find a network
path to `flatironschool.com`. A real benefit of this way of working with a computer
is that you don't have to click through several menus to get there! You can capture
output, store it to files and use that output as input to _other commands_ (we'll give
plent more examples of in this module).

Experienced developers would say "the CLI gives you more control" or that it's
"more powerful" for those reasons.

Developers love the command line and, as a result, write most developer tools
for other users of the command line. As a result, tools you will need to be a
developer ***will require you to use them through the command-line interface.***

Lots of people worry that using the CLI will get them in trouble - like they'll
break their computer. While the CLI makes it easier to do things that permanently
affect your computer, daily caution _usually_ prevents it. We'd encourage you to think about the CLI like a good
sharp kitchen knife: if you pay attention when you use it, you're going to have
a valuable ally on your side. Days and months and even years will likely go by
before you ever think to do something dangerous or harmful with the knife. While the
risk is certainly there every time you touch it, you'll make a lot of meals without
the least bit of trouble. As you start out, take your time and if you have a question, ask.

## Identify Differences Between Command-Line Interface, Terminal Emulator, and Shell

When you want to use the CLI, you launch a program called a "terminal" program.
That's short for "terminal emulator." A long time ago, people only had keyboards
and monitors (no mouse or graphic interface!) that were connected to a computer that
they all shared. This monitor + keyboard device was called a "terminal." So the
"accounting department" might share a computer and every person
in the department would have a "terminal" connected to this computer. It looked
like this:

<KG: Add pic of "vt100 terminal" >

<KG: tie to AT table we added today: graphic of terminal cabled to a shared computer >

Nowadays, the "terminal" is "emulated" in software. It's "virtual." You launch
the "emulator" by opening a program called `Terminal` on OSX or something
similar on Linux or Windows. Instead of being connected to a remote computer by
a cable, your "terminal emulator" talks to the computer that it's running on.

<KG: graphic of terminal cabled to itself >

When you launch the "terminal emulator" program, it will immediately start within
itself a program called a _shell_ program. The _shell_ program is what actually prompts
you for input and returns the output. The shell most computers default to
using is known as `bash`.

<KG: Screenshot of terminal running bash with text arrows pointing to the outer window = Emulator; inner part of window
with pref. the bash-2.04$ prompt labeled "bash"; the line with the `$` should be labeled prompt; to the prompt we shoul
d type `ls` and label that `command` and then the output should be labeled as `output`>

To help keep these terms straight, here's a table

<KG: insert table derived from style guide >

## Conclusion

In this lesson we've seen the terminal emulator program launch and have seen it run a program called a "shell" inside. The "shell" program we'll be using in our examples is called "bash." 

Through "bash," we've seen the "Command-Line Interface" which:

* Prompts for a command
* Reads in the command
* Decides if the command is valid (`tickle-elmo`, for example, is not valid)
* Does something based on the command
* Returns output

In the subsequent lessons you will use the command-line interface to explore your computer's hard disk.

## Resources

- [Lifehacker on the Command Line](http://lifehacker.com/5633909/who-needs-a-mouse-learn-to-use-the-command-line-for-almost-anything)
- [Environment Variables](http://cbednarski.com/articles/understanding-environment-variables-and-the-unix-path/)
- [Built-in Shell Commands](https://www.gnu.org/software/bash/manual/html_node/Bash-Builtins.html) *Very useful*
- [15 Useful Bash Commands](http://www.thegeekstuff.com/2010/08/bash-shell-builtin-commands/)
- [The One True Path](http://blog.seldomatt.com/blog/2012/10/08/bash-and-the-one-true-path/)
- [More on paths - Wikipedia](http://en.wikipedia.org/wiki/Path_\(computing\))
- [The history of hidden files](https://plus.google.com/101960720994009339267/posts/R58WgWwN9jp)
