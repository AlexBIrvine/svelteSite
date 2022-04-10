---
date: '2022-4-9'
title: 'Procedural Day 0: Inventory and Setup'
excerpt: Defining the project goals, taking inventory of language & paradigm, and setting up the dev environment
categories:
  - 'Programming Paradigms'
  - 'Learning Journal'
  - 'Programming'
  - 'Procedural'
  - 'C Language'
# updated:
---

# Project Requirements

The goal of this project is to create a cross platform GUI application using the SDL2 library that will be used to retrieve a quote from the QuotableIO API (https://api.quotable.io/random) and display it in a window.  The user will then have the option to save that quote to their device as a txt file, or open other saved quotes and display them in this application.  The application must be able to run on Linux, Windows, and Android without needing to be compiled from source.  

# Technologies Used

The project will be using the C programming language and the SDL library (possibly others too) in order to better learn how application development is done with a procedural programming paradigm.  

# Inventory of C

C is a language without a lot of features compared other more commonly used languages out there today.  It does not support any object oriented programming, higher order functions, or a packaging system similar to Javascript's NPM or Python's PIP.  All libraries are installed on the development machine and linked to when compiling the program into an executable.  Unlike Java and C#, C does not compile down into bytecode that will be interpreted by a virtual machine.  The executable created by C code is machine dependant.  

# Starting Steps in the Project

## 1. Installing dependencies

I'm working off of a Thinkpad T480 running Manjaro Linux.  Since this distro is arch based, I'm able to install the SDL2 library with the following command: 

`pacman -S sdl2`

Running that command showed me that the library is already installed on my system and ready to go.  

## 2. Creating the Test Program - HelloWorld

Here is the program, each step explained below: 

```c
#include <stdio.h>
int main(void) {
   printf ("Hello world!\n");
   return 0;
}
```

The first line `#include <stdio.h>` is how we link our standard I/O library to our program.  This is necessary for writing to the console.  If you are wondering why this basic output isn't included in all C programs by default, it's because C is used in so many different applications that it's not an assumed need.  For embedded engineers writing firmware drivers to motor controllers, there is no display and therefore no output needed.  It would be a waste to I/O support in that application, so C makes you include what you need per project.  

The next line `int main (void)` is the declaration of our main function.  The `int` is the return type.  Being that this is the main method, the return int is consumed by the OS that calls the executable.  A return code of 0 means that the program worked properly, and a return code of 1 means that an error ocurred in the program.  `(void)` means we will not be passing in any arguments and the main function accepts no parameters.  

Inside the block, as indicated by the curly braces, is the call to the `printf` function.  This is short for "print formatted" and returns the string "Hello World" to the standard output.  The `\n` at the end of the string is an escape character, in particular the new line characters.  This sends the equivalent of the enter key at the end of the string and will start the next outputted text on a new line.  

The final statement `return 0;` returns the integer 0.  If the program is able to execute this line, that means that it successfully ran without error, hence the return code of 0. 

## 3. Compiling and Running

I will be using the GCC (GNU C Compiler) for this project.  The first step was to ensure this was installed on my machine by checking for it's version using `gcc -v`.  This informed me that my machine is currently running version 11.2.0.  From there I directed my terminal to the folder the .c file is stored in and ran `gcc Hello.c -o Hello` in order to compile it.  This produced a file called `Hello`, which is the compiled output of `Hello.c`.  In order to run this on my machine, I had to change the file's privileges and allow it to be executed.  The linux command for this is `chmod +x Hello`.  From there, it's simply a matter of calling the file from the current folder with `./Hello`.  This produced the desired output to STDOUT!

# Lessons Learned

Not too much for me.  This was a refresher since I've taken a basic C programming course during my first attempt at university back in 2009.  