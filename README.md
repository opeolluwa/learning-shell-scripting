# Learning Shell Scripting

## What is a Shell?

Shell is a special user prgram that provides an interface to the user to use
operating system services.

Essentially the Shell accepts human-readable commands from input sources such as
keyboard-entry or file(shell scripts) and pass this to the Kernel

## What is Shell Scripting?

Shells are interactive, accepting commands from the user, typically through the
keyboard. For routine tasks, this becomes a very difficult thing to do, thus the
scripts are saved in files and passed to the Command Line Interpreter. This is
Shell scripting.

## Table of Content

- [What is a Shell](#what-is-a-shell)
- [What is Shell Scripting](#what-is-shell-scripting)
- [Beginning Shell Scripting](#beginning-shell-scripting)
- [Hello World](#10-hello-world)
- [Working with Inputs, Parameter and Variables](#20-working-with-inputs-parameter-and-variables)
- [More on Variables](#30-more-on-variables)

## Beginning Shell Scripting

A Shell script is typically appended with `.sh` or `-sh` extension, none of this
in needed, a script can be just the shell name, typically, scripts are placed in
`bin` or in `scripts` folder of larger/parent programs

```sh
mkdir bin
touch bin/hw
echo "echo Hello, World!" > bin/hw
```

## 1.0 Hello World

A Shell script must begin with the interpreter, typically, this is usually
`#!/bin/bash`, this can also be `#!/bin/zsh`, `#!/bin/csh`, etc.

The script must contain the following fields,

- Title - A brief description of the Script
- Date - Date the shell was written/last modified
- Author - Name of the Authors
- Version - Versioning using [SemVer](https://semver.org)
- Description - Deatiled infiormation about what the script is expected to do
- Options - the parameter which may be passed to the shell

Note that these values are provided for human readers/ future maintainers. An
example implementation would look like this.

```bash
#!/bin/bash 

#: Title          : Learning Shell scripting 
#: Date           : 2024-04-22 (last modified)
#: Author         : Adeoye Adefemi <adefemiadeoye@yahooo.com>
#: Version        : 1.0.1 
#: Description    : A quick start guide on learning Shell Scripting with BASH
#: Options        : Not applicable
```

See [bin/hw](./bin/hw) for an updated Hello World program

## 2.0 Working with Inputs, Parameter and Variables

Parameter and variables can be one of

1. Positional Argument, refrenced by index 1, 2, 3 .... as passed to the script. 
2. Special characters, special token `$#` return the last index of the positional argument. `$@` or `$*` can be used to 
3. Variables, these are named variables, eg `$HOME`, `$DIR`, this can also be
   written as ${HOME}, ${DIR}

The Bourne Shell can only read up to 9 positional arguments, using $<index> to
access higher positions use ${<position>}

Also, BASH provides the `read` utility to read data from the input device,
typically the keyboard. see [bin/io](./bin/io) for examples

## 3.0 More on Variables

In BASH, variables may start with a letter, or and underscore. Variable names
may only contain letters, numbers and underscore. Single letter variables like
`i`, `n`, `j`, e.t.c should be avoided even in loops.

