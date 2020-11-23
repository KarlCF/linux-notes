## I/O Redirection

### Notes

* Extra reading:
  * https://linuxcommand.org/lc3_lts0070.php
  * https://www.guru99.com/linux-redirection.html
  * https://superuser.com/questions/1003760/what-does-eof-do
  * https://www.geeksforgeeks.org/piping-in-unix-or-linux/#:~:text=A%20pipe%20is%20a%20form,program%2Fprocess%20for%20further%20processing.&text=You%20can%20make%20it%20do,the%20pipe%20character%20%27%7C%27.
* EOF: End of File

### Redirections

* \> Redirects standard output (stdout), overwrites content
* \>> Redirects standard output and appends to the target file
* < Redirects standard input (stdin) (receives arguments until ctrl + d is pressed)
* << Redirects standard input 
* FD: File Descriptor
  * stdin - 0
  * stdout - 1
  * stder -:2
* 2> Redirects the standard error output(stderr)
* 2>> Redirects the standard error output(stderr)
* Example:
  * ls fogete opa.txt > saida.txt 2>&1 
    * 2>&1 is used to redirect the output from the standard FD (2 for error) to 1(which is output), so when running that commend, both the error and success are output in the same destination
  * ls fogete opa.txt > saida.txt 2> saida.txt offers the same output from the command shown before, but needs more interaction
* tee - read from standard input and write to standard output and files
  * tee --help | study this

## Linux Basic Operators

### Notes

* Extra reading:
  * https://www.tecmint.com/chaining-operators-in-linux-with-practical-examples/#:~:text=The%20AND%20Operator%20(%26%26)%20would,execution%20status%20of%20last%20command.

### Operators

* AND => && => Runs next command if the previous one succeeds
* OR => || => Runs until the command succeeds (keeps running while the commands fails)

## Getting Help

### Notable Commands

* man - an interface to the system reference manuals
  * use "/" to find patterns, example: /Richard to find the name Richard in the file
  * Whenever there are more than one entries for the same command (e.g.: crontab(1), crontab(5)) man opens on the first section, to specify the section, use man (section) (command). (e.g.: man 5 crontab)
  * To show available manuals, use man -k (command) or apropos (command), but apropos shows every reference to the command, which might be too much info. Use -e (e.g.: apropos -e ls)
* apropos - search the manual page names and descriptions
  * -w to enable wildcard on query
* whatis - display one-line manual page descriptions
* which - locate a command
