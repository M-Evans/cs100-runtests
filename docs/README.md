#CS100 Runtests

##Table of Contents
1.[What is cs100-runtests?] (#what-is-cs100-runtests?)

2.[Installation] (#installation)

3.[How do I use it?] (#how-do-i-use-it?)

  3a.[The Vim Pane] (#the-vim-pane)

  3b.[The Shell Pane](#the-shell-pane)

  3c.[The Runtests Controller Pane] (#the-runtests-controller-pane)

4.[An Example Walkthrough] (#an-example-walkthrough)

5.[Features](#features)

##What is cs100-runtests?
``cs100-runtests`` is a script developed to assist testing of student-made bash shells.
(Specifically, "rshells" developed by UCR CS-100 students)

##Installation
Installing ``cs100-runtests`` is as simple as cloning this repository. For those unfamiliar with how, enter the following in your terminal:
```
git clone https://github.com/M-Evans/runtests
```

##How do I use it?
Once you have installed ``cs100-runtests``, run it with the command:
```
cs100-runtests <shell> <testcasefile>
```
where ``<shell>`` is the shell you want to test (e.g. ``bin/rshell``, ``sh``, ``bash``, etc.) and <testcasefile> is the path to the file containing all of the test cases you would like to use on your shell.
These parameters are optional, as runtests will default to ``bin/rshell`` if no shell is entered, and it is possible to load a test case file within the program after the script has been run.

Three panes are created when ``cs100-runtests`` is started.
The left pane is the [Vim pane](#the-vim-pane), which contains an open grade file that is created in the current directory. 
The upper right pane is the [Shell pane](#the-shell-pane), where the user-input <shell> (or default ``bin/rshell``) is started.
The lower right pane is the [Runtests Controller Pane](#the-runtests-controller-pane). All commands for ``cs100-runtests`` are entered here.

###The Vim Pane
The Vim Pane is controlled with the following commands:
* ``g <line> <amount>`` or ``grade <line> <amount>`` places the amount entered as a grade on the line entered.
* ``f <line>`` places a full score on the entered line. 
  * Nothing happens when these commands are entered if ``<line>`` is not a properly-formatted grade line.
* ``zero`` makes all grades 0.
* ``full`` makes all grades maximum.

###The Shell Pane
The Shell Pane is controlled with the following commands:
* ``n`` or ``next`` runs the next test case loaded from the test case file.
* ``p``, ``previous``, ``b``, or ``back`` runs the previous test case loaded from the test case file.
  * Note: Pressing enter following a ``next`` or ``previous`` command will repeat it.
* ``l <testcasefile>`` or ``load <testcasefile>`` loads <testcasefile> into rshell, discarding previously loaded test cases.

###The Runtests Controller Pane
The Runtests Controller Pane is controlled with the following commands:
* ``c`` or ``clear`` clears the controller screen.
* ``e``, ``exit``, ``q``, or ``quit`` ends the program.
* ``h`` or ``help`` prints a small help message detailing the controls for ``cs100-runtests``.
  * ``h?``, ``?h``, ``?``, and ``??`` also print the help message.

##An Example Walkthrough

##Features
