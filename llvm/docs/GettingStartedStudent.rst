=============================================================================
Getting Started with the LLVM System: Students, Hobbyists and Other Beginners
=============================================================================

.. contents::
   :local:

Audience
========

This version of the getting started guide is for those who want to build a
compiler from source and have a degree of technical knowledge.  For example
you might be:

* an undergraduate studying compilers who wants to understand more about a
  real world compiler;
* a hobbyist who wants to know more about how compilers work;
* a professional software engineer who needs to understand more about modern
  compiler technology; or
* a MSc or PhD student considering using Clang/LLVM in your project.
Welcome to the LLVM project! In order to get started, you first need to know
some basic information.

Assumptions
===========

This guide assumes you are familiar with *git*, the command line, compiling C/C++
programs and (if you are using Microsoft Windows) *Visual Studio*.

Prequisites
===========

You should ensure you have the following installed:

- a standard C/C++ compiler
- *cmake*
- *git*
- *Visual Studio* (if you are using Microsoft Windows)

Basic Building Instructions
===========================

This will build a native C/C++ compiler that will generate
executable code that you can run on your own machine.

Short Version
-------------

   ::

   git clone https://github.com/llvm/llvm-project.git
   mkdir bd
   cd bd
   cmake ../llvm-project/llvm
   make clang

Detailed version
----------------

#. Check out the Clang/LLVM source tree.  On Linux the following command would
   be appropriate::

   git clone https://github.com/llvm/llvm-project.git

   While on Windows, you would need the following::

   git clone --config core.autocrlf=false https://github.com/llvm/llvm-project.git

   **Note.** In the past Clang, the front end language processor,
   and LLVM, the back end code generator, had separate source trees, and this
   step was more complex.

#. Clang/LLVM is built "out-of-tree" so the built compiler is kept separate
   from the source tree.  Create a build tree alongside your checked out
   sources.  On Linux you could use the following::

   mkdir bd

#. Configure the compiler ready for building.  Change to the build directory
   and configure to build using standard makefiles.  On Linux use the
   following::

   cmake -G "Unix Makefiles" ../llvm-project/llvm

#. Build the compiler.  On Linux use the following::

   make clang

#. Take your favourite "Hello World" program in C, compile and run it.  On
   Linux use the following::

   ./bin/clang -o hello hello.c
   ./hello

#. Congratulations!  You have successfully compiled and run your first program
   using the Clang/LLVM compiler build from source.

