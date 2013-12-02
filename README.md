makefile-tutorial
=================

A tutorial on learning Makefiles (Based on tutorial written [here](http://www.cs.colby.edu/maxwell/courses/tutorials/maketutor/))


### What is a makefile?

A makefile is a special file that lists a set of rules for compiling a project.
These rules are called *targets*.  When you call the program `make`, it runs through each of these targets in your Makefile and executes them.


### What is the syntax of a Makefile?

Makefiles incorporate bash scripting with its own special syntax to indicate targets and variables.

You can run bash commands like

all:
    echo Hello


Makefiles also have special macros for indicating variables:

CC          --> Tells `make` which C compiler to use
CFLAGS      --> Specifies command line flags to pass to compiler
DEPS        --> File dependencies

You can also introduce your own macros like:

TARGETS     --> Indicates a list of targets to build

