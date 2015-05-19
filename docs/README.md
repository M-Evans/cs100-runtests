#CS100 Runtests

##Table of Contents
1.[What is cs100-runtests?] (#What is cs100-runtests?)
2.[Installation] (#Installation)
3.[How do I use it?] (#How do I use it?)
  3a.[The Vim Pane] (#The Vim Pane)
  3b.[The Shell Pane](#The Shell Pane)
  3c.[The Runtests Controller Pane] (#The Runtests Controller Pane)
4.[An Example Walkthrough] (#An Example Walkthrough)
5.[Features](#Features)

##What is cs100-runtests?
``cs100-runtests`` is a script developed to assist testing of student-made bash shells.
(Specifically, "rshells" developed by UCR CS-100 students)

##Installation

##How do I use it?
Once you have installed ``cs100-runtests``, run it with the command:
```
cs100-runtests <shell> <testcasefile>
```
where ``<shell>`` is the shell you want to test (e.g. ``bin/rshell``, ``sh``, ``bash``, etc.) and <testcasefile> is the path to the file containing all of the test cases you would like to use on your shell.
These parameters are optional, as runtests will default to ``bin/rshell`` if no shell is entered, and it is possible to load a test case file within the program after the script has been run.

Three panes are created when ``cs100-runtests`` is started.
The left pane is the [Vim pane](#The Vim Pane), which contains an open grade file that is created in the current directory. 
The upper right pane is the [Shell pane](#The Shell Pane), where the user-input <shell> (or default ``bin/rshell``) is started.
The lower right pane is the [Runtests Controller Pane](#The Runtests Controller Pane), which awaits further commands.

###The Vim Pane

###The Shell Pane
The Shell pane is controlled with the following commands:
* ``n`` or ``next`` runs the next test case loaded from the test case file.
* ``p``, ``previous``, ``b``, or ``back`` runs the previous test case loaded from the test case file.
  * Note: Pressing enter following a ``next`` or ``previous`` command will repeat it.
* ``l <testcasefile>`` or ``load <testcasefile>`` loads <testcasefile> into rshell, discarding previously loaded test cases.

###The Runtests Controller Pane

##An Example Walkthrough

##Features
