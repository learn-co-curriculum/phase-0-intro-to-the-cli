# CLI Essentials: Basic Commands in Bash

## Learning Goals

* Identify differences between command-line interface, terminal emulator, and shell
* Demonstrate how to navigate with Bash
* Demonstrate manipulating files in the command line

## Introduction

Have you ever noticed in movies or TV shows that when the "awesome computer
hacker person" needs to do something _really important_, you see them typing
a lot of text on a screen and _viol&agrave;_ something seemingly magical happens?

Like this...

< insert gif from Mr. Robot >

or this....

< insert gif from something else..>

You might have wondered what's going on there. These computer heroes are often
using a way of working with the computer called the "command-line interface" or
"CLI." The CLI asks the user for a command; the user types it in; and then the
computer runs the "sentence" that was typed in and returns output or makes changes.

For example, you can ask, through the CLI, which files are located on the
`Desktop`. You can create a new folder or delete it. But on top of
file-management kinds of activities, you can also find out how busy your CPU
is, how full your hard drive is, and whether your computer can find a network
path to `flatironschool.com`. On top of this you don't have to click through
several menus to get there! We'll give more examples of in the lesson.

Experienced developers would say "the CLI gives you more control" or that it's
"more powerful."

Developers love the command line and, as a result, write most developer tools
for other users of the command line. As a result, tools you will need to be a
developer will require you to use them through the command-line interface.

Lots of people worry that using the CLI will get them in trouble - like they'll
break their computer. We'd encourage you to think about the CLI like a good
sharp kitchen knife: if you pay attention when you use it, you're going to have
a valuable ally on your side. Take your time and if you have a question, ask.

## Identify Differences Between Command-Line Interface, Terminal Emulator, and Shell

When you want to use the CLI, you launch a program called a "terminal" program.
That's short for "terminal emulator." A long time ago, people only had keyboards
and monitors (no mouse or graphic interface!) that were tied to a computer that
they all shared. This monitor + keyboard device was called a "terminal." It looked
like this:

< pic of terminal >

< graphic of terminal cabled to a shared computer >

Nowadays, the "terminal" is "emulated" in software. It's "virtual." You launch
the "emulator" by opening a program called `Terminal` on OSX or something
similar on Linux or Windows. Instead of being connected to a remote computer by
a cable, your "terminal emulator" talks to the computer you're actually typing
on.

< graphic of terminal cabled to itself >

When you launch the "terminal emulator" program, it will immediately start a
program called a _shell_ program. The _shell_ program is what actually prompts
you for input and returns the output. The shell most computers default to
using is known as `bash`.

To help keep these terms straight, here's a table

< insert table derived from style guide >

## Conclusion

## Resources

- [Lifehacker on the Command Line](http://lifehacker.com/5633909/who-needs-a-mouse-learn-to-use-the-command-line-for-almost-anything)
- [Environment Variables](http://cbednarski.com/articles/understanding-environment-variables-and-the-unix-path/)
- [Built-in Shell Commands](https://www.gnu.org/software/bash/manual/html_node/Bash-Builtins.html) *Very useful*
- [15 Useful Bash Commands](http://www.thegeekstuff.com/2010/08/bash-shell-builtin-commands/)
- [The One True Path](http://blog.seldomatt.com/blog/2012/10/08/bash-and-the-one-true-path/)
- [More on paths - Wikipedia](http://en.wikipedia.org/wiki/Path_\(computing\))
- [The history of hidden files](https://plus.google.com/101960720994009339267/posts/R58WgWwN9jp)