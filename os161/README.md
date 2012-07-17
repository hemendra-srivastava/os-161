# OS 161 source
##files: 

Makefile: top-level makefile; builds the OS/161 distribution, including all the provided utilities, but does not build the operating system kernel. 

configure: this is an autoconf-like script. It sets up things like `How to run the compiler.' You needn't understand this file, although we'll ask you to specify certain pathnames and options when you build your own tree. 

defs.mk: this file is generated when you run ./configure. You needn't do anything to this file. 

defs.mk.sample: this is a sample defs.mk file. Ideally, you won't be needing it either, but if configure fails, use the comments in this file to fix defs.mk. 

##directories: 

bin: this is where the source code lives for all the utilities that are typically found in /bin, e.g., cat, cp, ls, etc. The things in bin are considered "fundamental" utilities that the system needs to run. 

include: these are the include files that you would typically find in /usr/include (in our case, a subset of them). These are user level include files; not kernel include files. 

kern: here is where the kernel source code lives. 

lib: library code lives here. We have only two libraries: libc, the C standard library, and hostcompat, which is for recompiling OS/161 programs for the host UNIX system. There is also a crt0 directory, which contains the startup code for user programs. 

man: the OS/161 manual ("man pages") appear here. The man pages document (or specify) every program, every function in the C library, and every system call. You will use the system call man pages for reference in the course of assignment 2. The man pages are HTML and can be read with any browser. 

mk: this directory contains pieces of makefile that are used for building the system. You don't need to worry about these, although in the long run we do recommend that anyone working on large software systems learn to use make effectively. 

sbin: this is the source code for the utilities typically found in /sbin on a typical UNIX installation. In our case, there are some utilities that let you halt the machine, power it off and reboot it, among other things. 

testbin: these are pieces of test code.