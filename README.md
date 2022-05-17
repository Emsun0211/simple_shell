# Simple_Shell Project
This project is a collaboration between Samuel Ifada and Israel Adenuga, actual students of Software Engineering at Alx School. It consists of developing and making our own UNIX command interpreter (Shell).
The "Simple_shell" is a program that can be compiled and launched from the command line, where its main function is to execute commands read from the standard input.  It contains some of the basic features and functions found in the various shell programs like Kernel commands and builtin commands.
# Quick Start
1. Git clone this respository to your local directory.
>https://github.com/adexino0606/Simple_Shell.git
2. Compile the program.
>$ gcc -Wall -Werror -Wextra -pedantic *.c -o hsh
3. Now execute the shell.
>$ ./hsh
# Builtin Commands
This shell supports the next builtin commands:
>cd - change directory
>env - list the current environment variables
>exit - exit the shell
>help - show help for a builtin command
>pwd - Print the absolute pathname of the current working directory
>unsetenv - Remove an environment variable
# Delimit and comment commands
>; -  The semicolon. command separator that allows to run a command on a single line placing the semicolon between
> each command.
># - The command number. Allows a word beginning with # and all remaining characters on that line to be ignored.
# Manual
To see the manual run:
>$ man ./man_1_simple_shell
Example:
>man(1)           Manual page for Simple_Shell  man(1)
>NAME
>          Simple_Shell - Command language interpreter
>SYNOPSIS
>            ./hsh
>DESCRIPTION
>            Command language interpreter that executes commands read from the standard input or from a file.
>INVOCATION
           An  interactive  shell is one started without non-option arguments, just running ./hsh. 
Otherwise, when is started non-interactively, to run a shell script, for example, the 
shell reads and execute the next command echo "pwd" | ./hsh.         .  .  .
# Files
Brief description of every file in this repository.
Files and Description as follows;
1. _atoi.c -function that gets sign and numbers of string.
2. _calloc.c -function that allocates memory for an array.
3. _change.c -functions that change the OLDPWD and PWD environment variables.
4. _display_help.c -functions that reads all builtins text files and prints it to POSIX stdout.
5. _envir.c -functions to print the environment variables and create a copy of env.
6. _errors.c -functions with the error message for each builtin.
7. _forky.c -program that creates process and execute.
8. _gethome.c -funtion to get the environment variable HOME.
9. _getline.c -functions to read what the user writes.
10. _iscd.c -functions to change the current directory of the process.
11. _isexit.c -functions that finds if line input is exit therefore process termination.
12. _ishelp.c -functions to print the help of each builtin.
13. _noargv.c -function to give shell form without filename as input.
14. _realloc.c -function to change the size and copy the content.
15. _realloc2.c -function to change the size and copy the content special case.
16. _signal.c -function to handle SIGINT signal.
17. _str_concat.c -function to create an array using malloc.
18. _strlen.c -function that returns the length of a string.
19. _unsetenv.c -functions to remove an environment variable.
20. _strtoky.c -functions to cut a string into tokens depending of the delimit.
21. _writerr.c -functions to print the error for each builtin.
22. _yesargv.c -function to give shell form with filename as input.
23. checkbin.c -functions to check if commands exist in the path.
24. free_grid.c -function to free a matrix.
25. man_1_simple_shell -manual of simple_shell.
26. parsing.c -functions that create an array of pointers depending of the delimit characters.
27. shell.h -header file with all thr function prototypes.
28.startshell.c -main function that stars the shell (shell skeleton).
# Examples
Some examples for builtins after execute ./hsh

cd:

#cisfun$ pwd
/home/vagrant/simple_shell
#cisfun$ cd
#cisfun$ pwd
/home/vagrant
#cisfun$
cd error:

#cisfun$ cd hola
./hsh: 1: cd: can't cd to hola
#cisfun$
exit:

#cisfun$ exit 123
vagrant@vagrant-ubuntu-trusty-64:~/simple_shell$ echo $?
123
exit error:

#cisfun$ exit hola
./hsh: 2: exit: Illegal number: hola
#cisfun$
help:

#cisfun$ help exit
exit: exit [n]
	Exit the shell.

	Exits the shell with a status of N.  If N is omitted, the exit status
	is that of the last command executed.
#cisfun$
help error:

#cisfun$ help hola
./hsh: 4: help: no help topics match 'hola'. Try 'help help' or 'man -k 'hola' or info 'hola'
#cisfun$
# Authors
Akinnukawe Gbenga @Emsun0211
Victoria Ekpenyong @V1que
