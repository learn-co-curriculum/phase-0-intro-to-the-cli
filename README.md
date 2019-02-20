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

## Identify Differences Between Command-Line Interface, Terminal Wmulator, and Shell

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

## Demonstrate How to Navigate With `bash`

To sum up: `bash` is a text-based interpreter that provides a _command-line
interface_ for controlling your computer (or operating system).

> **ASIDE**: Bash is actually an acronym which stands for **B**ourne-**A**gain
> **SH**ell. As the word "again" suggests, there are _other_ shells, some of
> which came before `bash`. There are also shells that have come along _since_
> `bash`. Nevertheless most programmers use `bash` or something very similar.

### Identify My Logged-In Username

Let's start simply. Let's ask the computer who I am logged in as:

```bash
$ whoami
```

 < probably need screen shot>

The `whoami` command lets you see which user account you're logged in to from a
terminal window. This might seem obvious, especially if you're logged in on your
personal computer, but it's not always clear which account you're you're working
in the command line.

In a strange circumstance where `whoami` isn't installed, there is another command
you can use that can tell you your current username. Try:

```bash
$ id -un
```

### Identifying the "Present Working Directory" With `pwd`

With your Terminal program open, type in `pwd` and hit return/enter.

```bash
$ pwd
```

You should see some output describing the directory you are currently within.
The `pwd` command stands for "**p**rint **w**orking **d**irectory".
You'll see that the operating system created a directory under the "User"
directory that was named the same as your `whoami` result

`/Users/[your user name]`

We would call this directory your "home" directory.

That output is describing a location on your computer.

`/User/kellyegreene` means that I am currently working within a directory `/Users`
on the root of my machine, and then within that directory, a directory named
`kellyegreene`. You might wonder what directory `Users` is in. Read on to
learn more about the `root` directory which contains all directories....

<something like that>

That's my home directory.

Because it's so common to read files from, or move things into our home
directories, `bash` lets us type `~` as a shortcut. We'll be working with this
shortcut later on.

Try this:

**Note:** *Any time you see the* `$` *character, you shouldn't type it in.
This is just a standard way to represent a bash prompt. Yours may or may not
be a* `$`.

```bash
$ cd ..
$ pwd
```

You should now see that you are one directory above where you were, in you're
in a new terminal, you might see:

`/Users`

You should be able to make a guess about what `cd` does, but we'll explain it
right now!

### Change Directories Using `cd`

The `cd` command stands for "**c**hange **d**irectory".
The `..` is a placeholder meaning the directory above the working directory.

Try this:

```bash
$ cd .
$ pwd
```

You can see you are still in the same directory.

The `.` is a placeholder meaning the current directory.

So here are three default placeholders for your file system:

- `~` Your **home** directory
- `.` The **current** directory
- `..` The directory in which your current directory is contained—referred to
as the "**parent**" directory.

You can supply any path to the `cd` command to nkellyegreenegate to that location.

## Demonstrate Manipulating Files in the Command Line

### Paths in Shell

The path supplied to the `cd` command, for example `/Users/kellyegreene`, is
known as an absolute path.

Systems can use either *absolute* or *relative* paths.

An absolute path is a path that points to the same location on the file system
regardless of the working directory. They start with `/` ("forward slash") because
that is the root of your file system.

This is an absolute path: `/Users/kellyegreene`.

A relative path is a path **relative** to the working directory of the user or
application, so the full absolute path will not have to be given. They start with
the name of a directory or a file.

This is a relative path: `kellyegreene/Documents`.

Paths use `/` to denote levels.

How many levels are within the following path?

`/Users/kellyegreene/Development/code/flatiron-school/mixtape-app`

If you said 6 levels to the question above you are right! Knowing where you
are in your terminal is very important.

### Use `ls` to List Files in Shell

In a new terminal, try this:

```bash
$ ls
```

You should see a list of all the files within your working directory.

The command `ls` stands for "**l**i**s**t".

We can use flags on most unix commands to give more specific instructions. Most
programs also accept flags, or options for execution.

A flag is denotated by a `-` ("dash"). **Note:** *In some programs, options are
passed directly to the command and not via flags.*

A common flag that nearly all programs and commands accept is a standalone `h`,
for "**h**elp".

```bash
$ ls -h
```

Single-character options can typically be combined with each other. For example,
in the `ls` command, `h` is a suffix on the `l` flag meaning "**h**uman readable
formats." They can be combined with `a` meaning "**a**ll information including.
Try these three together:

We can use the `ls -al` flag with ls so that we can see all of the files including
hidden files in "long form".

```bash
$ ls -lah
```
And also:

```bash
$ ls -l -a -h
```
Both are valid input options.

When you've entered `$ ls -lah` above, you should have a received a list of files
including some that you hadn't seen from entering just `$ ls` before:

```bash
drwxr-xr-x   6 kellyegreene  staff   204B Jun  2 11:21 .
drwxr-xr-x   5 kellyegreene  staff   170B May 28 15:52 ..
-rw-r--r--@  1 kellyegreene  staff   6.0K May 28 15:52 .DS_Store
drwxr-xr-x  13 kellyegreene  staff   442B Jun  2 11:02 .git
-rw-r--r--   1 kellyegreene  staff    66B May 28 15:49 .learn
-rw-r--r--   1 kellyegreene  staff    11K Jun  2 11:21 README.md
```

Notice that at the top of the file output there are a bunch of files that start with
a `.`, like `.DS_Store`

Files like `.DS_Store` are not listed. That's because files that start with a `.`
are _hidden_ files. Your `.bash_profile` is a hidden file in your home directory.
If you want to see the hidden files you can add the `a` flag to `ls` by typing `$ ls -a`.

**Note:** *Combining flags is only valid for single-letter options. A "long option"
such as* `--force` *is defined with more than one character and must be entered with
its own flag.*

### Use `mv` to Move or Rename Files and Directories

Move, or `mv` is a command that moves one or more files or directories from one place
to another.  To move a file from the current directory to another location, enter a
path as the third word on the command line.

```bash
$ mv filename /dir1/
```

We can also rename file or directory using the `mv` command. To rename a file with
`mv`, the third word on the command line must end in the new filename.

```bash
$ mv original_program.rb renamed_program.rb
```

### Create Empty Files With `touch`

We can use the `touch` command to create empty files in the current directory. Try:

```bash
$ touch hello_world.rb
```

Now try:

```bash
$ ls
```

You should see the file you just created, `hello_world.rb`, in the working directory.
Note that this is an empty file and has nothing inside of it, because you just created it.

### Making New Directiries Using `mkdir`

We can make directories with the `mkdir` command:

```bash
$ mkdir name_of_directory
```
Now if you enter `ls` you should see the empty directory you just created in the working
directory.

### Removing Files With `rm`

To delete a file, we can enter `rm` at a shell prompt.
**Note:** Deleting a file with rm is *permanent*. This action cannot be undone.

```bash
$ rm hello_world.rb
```

There additional options to `rm`:

* -i (interactive) — Prompts you to confirm the deletion. This option can stop you from
deleting a file by mistake.
* -f (force) — Overrides interactive mode and removes the file(s) without prompting.
Use this with caution. This action cannot be undone!
* -v (verbose) — Shows the progress of the files as they are being removed.
* -r (recursive) — Deletes a directory and all files and subdirectories it contains.

You can also delete directories using `rm` or `rmdir`.

## Conclusion

As we keep exploring and working with the command line, we will start to unlock and
understand its full potential! Adopting the terminal for command-related interactions
can allow us to become more productive users-—we work on multiple projects, tasks, and
easily switch contexts and folders. It's also the root of all computing systems. While
syntax might vary between operating systems, the functions that we are given through
terminal applications are the same.

## Resources

- [Lifehacker on the Command Line](http://lifehacker.com/5633909/who-needs-a-mouse-learn-to-use-the-command-line-for-almost-anything)
- [Environment Variables](http://cbednarski.com/articles/understanding-environment-variables-and-the-unix-path/)
- [Built-in Shell Commands](https://www.gnu.org/software/bash/manual/html_node/Bash-Builtins.html) *Very useful*
- [15 Useful Bash Commands](http://www.thegeekstuff.com/2010/08/bash-shell-builtin-commands/)
- [The One True Path](http://blog.seldomatt.com/blog/2012/10/08/bash-and-the-one-true-path/)
- [More on paths - Wikipedia](http://en.wikipedia.org/wiki/Path_\(computing\))
- [The history of hidden files](https://plus.google.com/101960720994009339267/posts/R58WgWwN9jp)