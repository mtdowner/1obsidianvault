Running a Bash script

There are two ways to run a Bash script. The first way is to execute it as a parameter of a direct call to the `bash` executable binary, like so:
```

$ bash myscript
Hello from Bash
WHERE the content of the file myscript is as follows:
echo "Hello from Bash"
myscript
The second way to use the chmod command to change the permissions of the bash script to make it a standalone 
executable, like so:
$ chmod +x ./myscript
$ ./myscript
chmod
bash
Bash commands
Cheat sheet
A Bash script is a text file that contains programming statements that execute commands that are part of the host 
computer’s operating system. Typically system administrators and programmers use Bash scripts to avoid having to 
repetitively execute tasks manually in a terminal.
A typical use case for a Bash script is to do set up tasks for a newly provisioned computer. Thus, in addition to being 
a tool for system administrators and programmers, a Bash script can also be used by system provisioning software.
(The $ symbol that proceeds commands in the examples represents the command line prompt.)
Unlike a binary executable file which knows how to interact with the computer’s operating system directly, a Bash 
script, which is always text based, requires another program to run its commands. This other program is called an 
interpreter. The interpreter that runs a Bash script is, as the name implies, bash. However, in other cases, a bash script 
can be run by another interpreter that’s installed on the host computer. An example of another interpreter is sh .
The way a Bash script lets the operating system know which interpreter to use is according to a declaration made at 
the first line of the script. This first line declaration is called a script header. It is also called a shebang. A shebang starts 
with the characters #!
An example of a shebang is as follows:
bash
sh
#!

BE CAREFUL to make sure there is no space on either side of the = symbol when declaring a variable. The following 
will not work: MYVARIABLE = foo.
=
MYVARIABLE = foo
developers.redhat.com redhat-developer @rhdevelopers
And the statement ${MSG,,} turns all uppercase characters in the variable MSG to lowercase, like so: ${MSG,,} MSG
MSG="aBcDeFg"
echo ${MSG,,}
#returns abcdef
Parameter expansion a technique to get the value from the referenced entity such as a variable in a Linux script or an 
environment variable according to a piece of processing logic. A variable is processed by enclosing the variable name 
within the ${ } characters. The processing logic is defined by characters that follow the variable name. For example 
the variable named MSG, the statement ${MSG^^} turns all lowercase characters in the variable MSG to uppercase, 
like so:
String manipulation using parameter expansion
${ }
MSG ${MSG^^} MSG
MSG="aBcDeFg"
echo ${MSG^^}
#returns ABCDEFG
Examples:
The following examples demonstrate various ways to use parameter expansion on Linux variables.
Word replacement
MSG="Say hi to Chris and Sidney"
echo ${MSG//Chris/Billy}
#returns Say hi to Billy and Sidney
Character replacement using regular expressions
MSG="I need 10"
echo ${MSG//[a-zA-Z]/X}
#returns X XXXX 10
Replace all alphabetic characters with the character X but leave the numerals alone X