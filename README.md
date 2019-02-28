# Basic Commands in Bash

## Learning Goals

* List directory files in the shell with `ls`
* Move or rename files and directories with `mv`
* Copy Files with `cp`
* Create empty files with `touch`
* Make new directories with `mkdir`
* Remove files with `rm`

## Introduction

In the previous lesson we learned how to "navigate" the directory structure
of our file system. But our file systems (and lives) would be so boring
without _files_. Copying files, moving files, reading the contents of
files, feeding files to the `ruby` program, cat .gifs. We looooooove files.

This lesson will show you how to work with your files. In time, you might
stop using Finder and other tools because it's so much faster (and fun!)
to use the CLI.

## List Directory Files in the Shell with `ls`

In a new terminal, which automatically puts you in your _home directory_, try this:

```bash
$ ls
```

The command `ls` stands for "**l**i**s**t". After you run it, you should then see a list of all the files within your working directory.

### Using Flags with Commands

We can use flags on most Unix commands to give more specific instructions. Most
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

## Move or Rename Files and Directories with `mv`

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

## Copy Files with `cp`

If you think about it, move is really "copy, but delete the original."
Well, `cp` does that, but doesn't delete the original. It's therefore a "copy."

It uses the same snytax as `mv`:

```bash
cp letter_to_mom.txt letter_to_mom-2019-02-15.txt
```

If you want to copy a directory and its file contents, you need to use the `-r` 
flag.

```bash
cp -r february_cat_gifs ~/Desktop/vital_media_files
```

> **NOTE**: Look how we're using the `~` shortcut! This expands into
> `/Users/username/Desktop/vital_media_files`

## Create Empty Files with `touch`

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

## Make New Directories with `mkdir`

We can make directories with the `mkdir` command:

```bash
$ mkdir name_of_directory
```
Now if you enter `ls` you should see the empty directory you just created in the working
directory.

## Remove Files with `rm`

To delete a file, we can enter `rm` at a shell prompt.
**Note:** Deleting a file with rm is *permanent*. This action cannot be undone.

```bash
$ rm hello_world.rb
```

Much like `cp`, if you want to delete a directory, you need to provide the `-r` flag

```bash
$ rm -r ~/Desktop/pokemon_fan_fiction
```

There additional options to `rm`:

* -i (interactive) — Prompts you to confirm the deletion. This option can stop you from
deleting a file by mistake.
* -f (force) — Overrides interactive mode and removes the file(s) without prompting.
Use this with caution. This action cannot be undone!
* -v (verbose) — Shows the progress of the files as they are being removed.

## Conclusion

There are a variety of commands you can use to manipulate files via the command line. If this list seems overwhelming at first, remember that it takes all programmers a little time to practice their CLI workflows. Refer back to these resources as you need to, and it will get easier as you go along.

## Resources

- [Lifehacker on the Command Line](http://lifehacker.com/5633909/who-needs-a-mouse-learn-to-use-the-command-line-for-almost-anything)
- [Environment Variables](http://cbednarski.com/articles/understanding-environment-variables-and-the-unix-path/)
- [Built-in Shell Commands](https://www.gnu.org/software/bash/manual/html_node/Bash-Builtins.html) *Very useful*
- [15 Useful Bash Commands](http://www.thegeekstuff.com/2010/08/bash-shell-builtin-commands/)
- [The One True Path](http://blog.seldomatt.com/blog/2012/10/08/bash-and-the-one-true-path/)
- [More on paths - Wikipedia](http://en.wikipedia.org/wiki/Path_\(computing\))
- [The history of hidden files](https://plus.google.com/101960720994009339267/posts/R58WgWwN9jp)
