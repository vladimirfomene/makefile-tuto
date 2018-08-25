
# Makefiles Are Awesome
This is an introduction to the GNU `make` utility. It was inspired by **Daphne's** [makefile tutorial](https://github.com/lifeissweetgood/makefile-tutorial) makefile tutorial. This repository will give you a brief introduction to Makefiles without getting too deep into its
complexity.
***

## Pre-Requisite
* Make sure you have a Bash shell.
* Make sure you have the GCC C compiler.
* Make sure you have the make utility installed on your system.

## What is Make Anyway?
* It is a command line tool that can help you automate a lot of command line tasks like building your software projects. Most projects are
made up of many source files and a change in any one of them will mean recompiling them before building the project. Imagine if your
project depends on millions of files, and you just made a change on a hundred of them. 


* Makefiles will save you from a lot of typing by helping you reduce long command line instructions into just a word and give you the power 
to provide a name for your binary executable file. The latter is helpful when you are compiling C programs and you do not want the compiler
to output a `a.out` file. 

* You can use make to build any kind of software project, it does not necessarily have to be a C or C++ project.

## How To Use This Tutorial
* Clone the repository using the following command: `git clone https://github.com/vladimirfomene/makefile-tuto.git`
* It is worth noting that when the make utility is ran on a directory, it executes the code in the `Makefile` of that directory.
* Each `Makefile-v#` has comments which explains the code in it.
* There are four make files in this repository, Makefile-v1 to Makefile-v4, they are arranged in order of complexity. To run each version, you have to execute the following commands in the order in which they appear: `make build-v1`, `make hello`, `make clean`. Run the same commands
for v2, v3 and v4.
* For each version, a binary executable program will be created after you run the `make hello` command. To see what this program does, run it by typing, `./hello`.


## What Happens When You Execute These Commands?
* Executing each `make build-v#` will copy `Makefile` into a temporary file and then copy the content of `Makefile-v#` into `Makefile`. This
is so that when you run, `make hello` you are executing the content within `Makefile-v#`.
* Executing `make hello` runs GCC (C compiler) to compile `hello.c` which depends on `greeting.c` and `greeting.h`.
* Executing `make clean` deletes every .o file and Makefile, then it moves the content in the temporary file back in the Makefile.


## Resources
Here is a list of resources that were helpful in making this tutorial and where you can go if you want to take your make skills to 
another level.
* [Youtube makefile tutorial](https://www.youtube.com/watch?v=Lyp36ku7D0A)
* [Webpage page tutorial](http://www.cs.colby.edu/maxwell/courses/tutorials/maketutor/)
* [Official GNU Make manual](https://www.gnu.org/software/make/manual/make.html)

