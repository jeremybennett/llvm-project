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

This guide assumes you are familiar with git, the command line, compiling C/C++
programs and (if you are using Microsoft Windows) Visual Studio.

Prequisites
===========

You should ensure you have the following installed
- a standard C/C++ compiler
- cmake
- git
- Visual Studio (if you are using Microsoft Windows)

Basic Building Instructions
===========================

This will build a native C/C++ compiler that will generate
executable code that you can run on your own machine.

#. Check out the Clang/LLVM sources.  Clang (the front end language processor)
   and LLVM (the back end code generator) have separate source trees (this
   will change in the future).
