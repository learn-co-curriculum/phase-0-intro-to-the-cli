# CLI Essentials: Basic Commands in Bash

## Learning Goals

* Demonsrate how to navigate with Bash
* Demonstrate manipulating files in the command line

## Introduction

Bash is a text-based interpreter for controlling your computer (or operating system).
Bash is actually an acronym which stands for **B**ourne-**A**gain **SH**ell. It replaced
the Bourne shell and "bashed together" the unix programs sh, csh and ksh. From it you can
navigate the files on your computer and execute programs.

You can also connect to other computers and basically do everything you can do in your GUI
Operating System (like OS X or Windows).

When you open a terminal, you're basically within your file system, or in a directory, just
like you are when you open a Finder window or an Explorer window.

## Demonsrate How to Navigate With Bash

### Identifying the "Present Working Directory" With `pwd`

Open up command prompt or terminal. Type in: `pwd` and hit return.

```bash
$ pwd
```

You should see some output describing the directory you are currently within.

`/Users/[your user name]]`

That output is describing a location on your computer. You have a file system and within that
file system are directories and files.

The `pwd` command stands for "**p**rint **w**orking **d**irectory".

`/User/kellyegreene` means that I am currently working within a directory `/Users` on the root
of my machine, and then within that directory, a directory named `kellyegreene`.

That's my home directory. It belongs to the user I am currently logged in as. The placeholder for
a user's home directory is the `~` ("tilde") symbol.

Try this:

**Note:** *Any time you see the* `$` *character, you shouldn't type it in. This is just a standard
way to represent a bash prompt. Yours may or may not be a* `$`.

```bash
$ cd ..
$ pwd
```

You should now see that you are one directory above where you were, in you're in a new terminal,
you might see:

`/Users`

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
- `..` The directory in which your current directory is contained—referred to as the "**parent**"
directory.

You can supply any path to the `cd` command to nkellyegreenegate to that location.

## Demonstrate Manipulating Files in the Command Line

### Paths in Shell

The path supplied to the `cd` command, for example `/Users/kellyegreene`, is known as an absolute
path.

Systems can use either *absolute* or *relative* paths.

An absolute path is a path that points to the same location on the file system regardless of the
working directory. They start with `/` ("forward slash") because that is the root of your file system.

This is an absolute path: `/Users/kellyegreene`.

A relative path is a path **relative** to the working directory of the user or application, so the
full absolute path will not have to be given. They start with the name of a directory or a file.

This is a relative path: `kellyegreene/Documents`.

Paths use `/` to denote levels.

How many levels are within the following path?

`/Users/kellyegreene/Development/code/flatiron-school/mixtape-app`

- [The One True Path](http://blog.seldomatt.com/blog/2012/10/08/bash-and-the-one-true-path/)
- [More on paths - Wikipedia](http://en.wikipedia.org/wiki/Path_\(computing\))

If you said 6 levels to the question above you are right! Knowing where you are in your terminal -
what directory you are working in - is very important.

### Use `ls` to List Files in Shell

In a new terminal, try this:

```bash
$ ls
```

You should see a list of all the files within your working directory.

The command `ls` stands for "**l**i**s**t".

We can use flags on most unix commands to give more specific instructions. Most programs also accept
flags, or options for execution.

A flag is denotated by a `-` ("dash"). **Note:** *In some programs, options are passed directly to the
command and not via flags.*

A common flag that nearly all programs and commands accept is a standalone `h`, for "**h**elp" or
"**h**uman".

```bash
$ ls -h
```

Single-character options can typically be combined with each other. For example,  in the `ls` command,
`h` is a suffix on the `l` flag meaning "**h**uman readable formats." They can be combined with `a`
meaning "**a**ll information including permissions". Try these three together:

We can use the `ls -al` flag with ls so that we can see all of the files including hidden files in long
form 

```bash
$ ls -lah
```
And also:

```bash
$ ls -l -a -h
```
Both are valid input options.

When you entered `$ ls -lah` above, you should have a received a list of files including some that
you hadn't seen from entering just `$ ls` before:

```bash
drwxr-xr-x   6 kellyegreene  staff   204B Jun  2 11:21 .
drwxr-xr-x   5 kellyegreene  staff   170B May 28 15:52 ..
-rw-r--r--@  1 kellyegreene  staff   6.0K May 28 15:52 .DS_Store
drwxr-xr-x  13 kellyegreene  staff   442B Jun  2 11:02 .git
-rw-r--r--   1 kellyegreene  staff    66B May 28 15:49 .learn
-rw-r--r--   1 kellyegreene  staff    11K Jun  2 11:21 README.md
```

Notice that at the top of the file output there are a bunch of files that start with a `.`, like
`.DS_Store`

Files like `.DS_Store` are not listed. That's because files that start with a `.` are hidden files.
Your `.bash_profile` is a hidden file in your home directory.  If you want to see the hidden files you can add the `a` flag to `ls` by typing `$ ls -a`.

If you're interested in where this convention came from check out [The history of hidden files](https://plus.google.com/101960720994009339267/posts/R58WgWwN9jp) .


**Note:** *Combining flags is only valid for single-letter options. A "long option" such as*
`--force` *is defined with more than one character and must be entered with its own flag.*

### Use `mv` to Move or Rename Files and Directories

Move, or `mv` is a command that moves one or more files or directories from one place to another. 
To move a file from the current directory to another location, enter a path as the third word on the
command line.

```bash
$ mv filename /dir1/
```

We can also rename file or directory using the `mv` command. To rename a file with `mv`, the third word
on the command line must end in the new filename.

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

You should see the file you just created, `hello_world.rb`, in the working directory. Note that this is an
empty file and has nothing inside of it, because you just created it.

### Making New Directiries Using `mkdir`

We can make directories with the `mkdir` command:

```bash
$ mkdir name_of_directory
```

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

## Resources

- [Lifehacker on the Command Line](http://lifehacker.com/5633909/who-needs-a-mouse-learn-to-use-the-command-line-for-almost-anything)
- [Environment Variables](http://cbednarski.com/articles/understanding-environment-variables-and-the-unix-path/)
- [Built-in Shell Commands](https://www.gnu.org/software/bash/manual/html_node/Bash-Builtins.html) *Very useful*
- [15 Useful Bash Commands](http://www.thegeekstuff.com/2010/08/bash-shell-builtin-commands/)
