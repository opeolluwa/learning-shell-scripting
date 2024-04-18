# Learning Shell Scripting

## What is a Shell?

Shell is a special user prgram that provides an interface to the user to use operating system services.

Essentially the Shell accepts human-readable commands from input sources such as keyboard-entry or file(shell scripts) and pass this to the Kernel

## What is Shell Scripting?

Usually Shells are interactive, accepting commands from the user, typically through the keyboard. For routine tasks, this becomes a very difficult thing to do, thus the scripts are saved in files and passed to the Command Line Interpreter. This is Shell scripting.

## Table of Content

- [What is a Shell](#what-is-a-shell)
- [What is Shell Scripting](#what-is-shell-scripting)
- [Beginning Shell Scripting](#beginning-shell-scripting)
- [Hello, World](#hello-world)

## Beginning Shell Scripting

A Shell script is typically appended with `.sh` or `-sh` extension, none of this in needed, a script can be just the shell name, typically, scripts are placed in `bin` or in `scripts` folder of larger program

```sh
mkdir bin
touch bin/hw
echo "echo Hello, World!" > bin/hw
```

# 1.0 Hello World

A Shell script must begin with the interpreter, typically, this is usually `#!/bin/bash`, this can also be `#!/bin/zsh`, ``#!/bin/csh`, etc.

The script must contain the following fields,

- Title
- Date - Date the shell was written/last modified
- Author - Name of the Authors
- Version - Versioning
- Options - the parameter which may be passed to the shell

Note that this are provided for human readers/ future maintainers 


See [bin/hw](./bin/hw) for an updated Hello World program 
