makefile-tutorial
=================

A tutorial on Makefiles (Based on tutorial written [here](http://www.cs.colby.edu/maxwell/courses/tutorials/maketutor/))

## Let's Demystify Makefiles!

This tutorial explains what Makefiles are, how they are useful and shows how to write your own from scratch.  To see how Makefiles work "in action," clone the source code on the master branch and compile the simple C project. There are different versions of the same Makefile with varying degrees of complexity.  To compile each, run the following commands:

```
make build-v1
make
```

To run the simple C program, do:

```
./hellomake
```

To run a different version of the Makefile, do:

```
make clean
make build-v2
make
```

Substitute `build-v2` with either `build-v1`, `build-v3` or `build-v4` to run make with each of the other corresponding Makefile versions.


### What is a makefile?

A makefile is a special file that lists a set of rules for compiling a project.
These rules include *targets*, which can be an action `make` needs to take (eg. "clean" or "build") or the files/objects `make` will need to build (eg. .o files or an executable), and the commands that need to be run in order to build that target.  When you call the program `make`, it runs through each of these targets in your Makefile and executes them.

Rules usually take the form of:

```
target: dependencies
       steps to build target with dependencies
```


### What is the syntax of a Makefile?

Makefiles incorporate bash scripting with its own special syntax to indicate targets and variables.

You can run bash commands like

```
all:
    echo Hello
```

Makefiles also have special macros for indicating variables:


`CC`          --> Tells `make` which C compiler to use

`CFLAGS`      --> Specifies command line flags to pass to compiler

`DEPS`        --> File dependencies



You can also introduce your own macros like:

`TARGETS`     --> Indicates a list of targets to build


### Resources

The ultimate `make` and Makefile resource: [GNU make docs](http://www.gnu.org/software/make/manual/make.html)

The tutorial upon which this one is based: [cs.colby.edu](http://www.cs.colby.edu/maxwell/courses/tutorials/maketutor/)
