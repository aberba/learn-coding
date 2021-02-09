# Learn Coding: using D

> A mini book for learning computer programming completely from scratch using D programming language.

# Preface

This book is written to guide you to learn computer programming. I have put in effort to make it easy to understand for beginners. You will be taken through the basics and move to more advanced topics as you go further. You are encourage to follow along right from the start to understand more advanced concepts in this book.

# Chapter 1: Introduction

In this chapter, you will be introduced to the concept of computer programming, how it works and you will finally write your first code. The various sections of this chapter are outlined below:

* Introduction to computer programming
* Setting up your development environment
* Writing your first code

## Introduction to computer programming

A computer is an electronic device, which takes instructions and carries them out. A computer program contains the instructions which tell the computer what to do. By writing the right program, you can tell a computer to do anything, _as long as it is capable_. A computer only understand **0s** and **1s**. It uses a combination of 0s and 1s to represent a specific instruction. These combinations of 0s and 1s are difficult to write or understand.

To solve this problem, `computer programming languages` were invented. Programming languages are much easy to write or understand. A compiler is a program to convert a programming language into **machine code** which a computer can understand. The process of writing code in a programming language is known as _coding_ and converting it to machine code is known as **compilation** : the word **"compile"** is the verb for compilation.

There are so many different programming languages today. They all server the same purpose: to instruct a computer to perform a certain action. These languages vary in their design. Some are general purpose languages whilst other are designed for special purposes. Each programming language has its own special compiler for converting it into machine code.

[D](https://dlang.org) is one example of a general purpose programming language. It was designed to be used for doing so many things (web applications, games, desktop applications, operating systems, robotics, real-time communication systems, etc). Learning D is fairly straight forward even for beginners. In this book, you will learn how to begin computer programming using the D programming language.

## Setting up your development environment

To begin programming in D you need to have the following two (2) softwares:

1. **A Text Editor**: A text editor is a software used for writing code. One example of a text editor is Sublime which you can download at **[sublimetext.com](https://www.sublimetext.com/)**.
2. **D compiler**: We will use the D compiler to convert the code we will write to machine code. Download the D compiler at **[dlang.org/download](https://dlang.org/download)**. Make sure you select **DMD (the official D compiler)** and download the version for your Operating System (Windows, Linux, macOS, BSD, etc).

After downloading these two softwares, install all onto your computer. After completing this process, you are ready to begin programming! From this point onwards, we will be using the **command-line** (also know as Command Prompt or Terminal) to run DMD (the D compiler) to compile the code we will write to machine language. Instructions on how to launch the command-line for various Operating Systems is illustrated as follows:

#### Windows

If you are on Windows, open Start Menu and search for **D2 32-bit Command Prompt**. Open it to launch a command prompt on your desktop as shown in the screenshot below:

![D2 32-bit Command Prompt in Windows](images/commad-prompt.jpg)
D2 32-bit Command Prompt in Windows

Create a new folder named `code-demo` in your `C:\` drive. All the code we will write should be stored in this folder (`C:\code-demo`). Navigate to this folder in the command prompt you launched by entering the command `cd C:\code-demo` (press `Enter` on your keyboard to run command). Remember to _always_ make sure you navigate to `C:\code-demo` whenever you first launch **D2 32-bit Command Prompt**.

#### Linux and macOS

The command-line program for most Linux Operating Systems and macOS is called **Terminal**. Search for "Terminal" from the applications installed and launch.

![Terminal in Linux](images/linux-terminal.png)
Terminal in Ubuntu Linux

The code we will write should be stored in a newly created folder `code-demo` in your Home folder. Navigate to this folder by entering the command `cd ~/code-demo` in your command-line. Remember to _always_ make sure you navigate to `code-demo` whenever you first launch **Terminal**.

> #### Installing the D compiler other Operating Systems
>
> There are so many Operating Systems which do not have their installer on the [D language website](https://dlang.org/download). Some of them require building the compiler from its source code on your own. Approach for some of them are as follows:
>
> * **Slackware**: Slackware uses Slackbuild script to create packages. You can obtain the slackbuild script for the D compiler at https://slackbuilds.org/repository/14.2/development/dmd/
> *

## Writing your first code

To be begin, we will write a small piece of code that displays the text `"Hello, world"` to he screen. Open Sublime text editor and create a new file by clicking on `File > New File`. Save the file by clicking on `File > Save`. This will bring up a file dialog for you to select a location where your want to save the file. On Windows, save it at `C:\code-demo` folder. For Linux and macOS users, save it in the `code-demo` folder in Home. Make sure you save the file as `hello.d`.

> #### File Naming Conventions
>
> Any file containing D code _must_ have a name that ends with `".d"`. The `".d"` is the extension (format) of the file. File names _must only_ contain numbers, letters, or underscore (`"_"`) and names _should not_ contain a space. All letters must be in lower-case (small letters).

> Some invalid style of naming D files include `"d program.d"`, `"d program .d"` and "`dprogram"`.
>
> Valid styles include `"d_program.d"`, `"dprogram.d"` and `"d_program_01.d"`.
>
> **NOTE:** Although I stated you should save the file as `hello.d`, you are free to save it with any name you want as long as it conforms to the file naming conventions stated above.

After saving the new file, type the following code _exactly as it appears_ into it:

```d
import std.stdio;
void main()
{
    writeln("Hello, world!");
}
```

The code should look similar to the screenshot below when typed in Sublime:

![Code in Sublime text editor](images/sublime-code.jpg)

You can now save the code to the file by clicking `File > Save` or using the keyboard shortcut `Ctrl + S` in Sublime. Enter the following command in your command-line compile and run the code using DMD:

```sh
dmd -run hello.d
```

This command tells DMD to look for a file named `hello.d`, compile and run it. You may also choose to compile it to machine code first using:

```sh
dmd hello.d
```

This will generate a program called `hello.exe` on Windows or just `hello` on Linux and macOS. On Windows, enter with the command:

```sh
hello.exe
```

or on Linux and macOS, enter:

```sh
./hello
```

This should print `"Hello, world!"` in the command-line just like the previous command but this time, you also have the generated program at the location of the D source file.

> ### Terms
>
> * Any file which contains code in any programming language is called a **source file**. The whole code for a program which may be made up of several source files in known as the **source code**.

If you typed the code correctly, saved it into the new file and typed the command correctly, DMD should compile and run the code we wrote above. This should print the text `"Hello, world!"` in the command-line as shown in the screenshot below;

![Demo code in Terminal](images/hello.png)
Demo code in Terminal

Congratulations! You have written your first program in D.

> ### Getting all source code for examples in this book
>
> You can access all the code used in this book at https://github.com/aberba/learn-coding within the `examples` folder. The examples source code is organized placed into various folders in sequence depending on the **Chapter** in the book within which it was demonstrated.
> For example, the `hello.d` code we just wrote will be placed in the `chapter_01` folder in `examples` and the file will be named as `example_01_hello.d`. The next example in this chapter will be saved in a file with its name prefixed with `example_02_`. The same pattern applies to source code for all examples in this book.

In the next chapter, you will learn the basics of D, and the meaning of the various units in the code we just wrote above.

# Chapter 2: Learning the basics of D

Programming languages have certain **basic rules** (syntax) programmers need to follow to write code that a compiler can convert to machine code and makes the computer carries out the required action accurately. These rules form the basics of every programming language including D. In this chapter, you will learn the basic **syntax** of D and how to perform certain tasks and mathematical calculations.

> **Syntax**: The syntax of a programming language is how code must be ordered or arranged or formatted by following the basic rules of the programming.

## The entry point

Every D program is required to have a specific piece of code where the computer will start executing the program from. This piece of code is known as the **entry point**. As you saw in chapter one, the entry point of a D program has the following syntax.

```d
void main() {
    // All code goes here
}
```

As you can see, the entry point starts with a **function** called `main` within which all other code must be placed.

> A **function** is a piece of code with a _given_ name which performs a specific action when used. Every function is given a _unique_ name to be used to reference it.

In D, an entry point function must and only be named `main` which will contain all other code of the program. Every function, including `main`, must have a **return type** which indicates the type of output (data type) the function produces, if any. The entry point in the above example has a return type of `void` which indicates that an entry point returns no output. We shall discuss functions and data types into details later in this chapter.

With this knowledge in mind, lets write a simple program that prints the text `"I am a programmer"` to the screen just like we wrote in Chapter One.

```d
// ch_02_01.d

import std.stdio: writeln;
void main()
{
    writeln("I am a programmer.");
}
```

The code above this time starts with `import std.stdio: writeln;` placed above the entry point, `main`. This line of code imports one built-in function called `writeln` from `std.stdio` module of the D **standard library**.

> `import` is a built-in keyword for importing functions and utitlies for use in a program. You may use just `import std.stdio;` to import _all_ functions and utilities in `std.stdio`. However, we used `import std.stdio:writeln` in the example to only import `writeln` function since we only needed that in the program. Its appropriate to only import what you need.

> The `std` prefix in `std.stdio` represents the **standard library** which is a collections of functions and utitlities for performing common tasks in programming. These functions and utilities are grouped into collections known as **modules** depending on the task each one performs. These functions and utilities are made for programmers to use in their code without having to write them themselves.

> The `stdio` module (standard **Input and Output module**) contains functions and utitlies for reading inputs and writing outputs. There are other modules which will be discusssed later in this book.

The `writeln` functions above is for writing text to the screen and we used it to write the text `"I am a programmer"` within the main function of the program. You may also modify the code to print any other text you want.

## Variables

A variable is used to represent the certain value in a program. This value can be any data such as the number of days in a week (numeric data type), the name of a person (string data type), the weight of an object (decimal), or and anwser to a question such as true or false (boolean data type). The syntax for declaring a variable is as follows:

```d
// ch_02_02.d

int count = 10;
string fullName = "Samuel Adongo";
float weight = 12.5;
bool isEmpty = true;
```

Each variable begins with its **data type** which may be `int`, `string`, `float`, etc. The data type we use depends on the type of data the variable will represent. An `int` data type is used for whole numbers, `string` for words, phrases and sentences, etc (more data types are discusssed later). The data type of a variable is followed by its name which _must be unique_. The name of a variable _must begin with a letter_ (a-z) and can contain numbers or an underscore (`_`) within it's name after the first letter. The following are all valid names;

```d
// ch_02_03.d

int number_of_fruits = 3;
int numberOfFruits = 3;
int number2 = 3;
int number_2 = 3;
int numberTwo = 3;
int numberTWO = 3;
```

Since each variable must have a unique name, using the same name for more than one variable will caused an error in the compiler during compilation. This error will appear when you run the command to compile your code. The following code will cause and error since the same name is used for the two variables defined:

```d
// ch_02_04.d

import std.stdio: writeln;
void main()
{
    int name = 3;
    string name = "Samuel Adongo";
}
```

An error message similar to the following will be displayed by the compiler as a result of the mistake:

```sh
code-demo/ch_02_04.d(5): Error: declaration ch_02_04.main.name is already defined
```

> The compiler reports an error when a programmer makes a mistake in the syntax of his code. Reading an error message will provide you with an idea of what went wrong in the code. Double check your code to fix the error on the line number which is usally shown in the error message in parenthesis. For example, `ch_02_04.d(5)` tells you the error seem to be on line `5`.

Lets write an example program which prints the value of variables defined to the screen:

```d
// ch_02_05.d

import std.stdio: writeln;
void main()
{
    string name = "Samuel Adongo";
    writeln(name);

    int totalCount = 20;
    writeln(totalCount);
}
```

This will print:

```sh
Samuel Adongo
20
```

## Data Types

There are several types of data including whole numbers, decimals, etc. we use in everyday life for calculations, counting, and other forms of communitcation. D provides syntax for representing such different types data of data in code when programming. The type of a data in D is known as its **data type**.

The table below outline the various basic data types in D:

### Character data type

A single charcter of a word can be represented in D using the `char` data type as follows:

```d
// chapter_02/ch_02_06.d

import std.stdio: writeln;
void main()
{
    char letter = 'a';
    writeln(letter);
}
```

The value of a charcter _must_ be wrapper in single quotes (`'a'`).

### String data types

Any word, phrase or sentence is know as a string and is represented with the `string` data type.

```d
// chapter_02/ch_02_07.d

import std.stdio: writeln;
void main()
{
    string coolWord = "Awesome";
    string coolPhrase = "Awesome guy!";
    string coolSentence = "I am an awesome programmer.";

    writeln(coolWord);
    writeln(coolPhrase);
    writeln(coolSentence);
}
```

The value of a string _must_ be wrapper in double quotes (`""`).

### Numerical data Types

Thes are data types from representing numbers are illustrated in the table below:

#### Whole numbers

| Data Type | Description                                                                                             |
| --------- | ------------------------------------------------------------------------------------------------------- |
| byte      | Positive and negative whole numbers ranging from -128 to 127                                            |
| ubyte     | Only positive whole numbers ranging from 0 to 255                                                       |
| short     | Positive and negative whole numbers ranging from -32768 to 32767                                        |
| ushort    | Only positive whole numbers ranging from 0 to 65535                                                     |
| int       | Positive and negative whole numbers ranging from -2147483648 to 2147483647                              |
| uint      | Only positive whole numbers ranging from 0 to 4294967295                                                |
| long      | Very large positive and negative whole numbers ranging from -9223372036854775808 to 9223372036854775807 |
| ulong     | Very large only positive whole numbers ranging from 0 to 18446744073709551615                           |

#### Decimal numbers

| Data Type | Description                                                         |
| --------- | ------------------------------------------------------------------- |
| float     | Decimals or numbers with fraction that does not exceed 3.40282e+38  |
| double    | Decimals or numbers with fraction that does not exceed 1.79769e+308 |

...
