#How to use CS100 Runtests

This walkthrough will familiarize you with the basic features and usages of ``cs100-runtests``.

First, start cs100 runtests as such:
```
./cs100-runtests bin/rshell exampleFolder/exampleTestCaseFile
```

You will see the [Vim Pane](#the-vim-pane) to the left, the [Shell Pane](#the-shell-pane) to the upper right, and the [Runtests Controller Pane](#the-runtest-controller-pane) to the lower right. 
The controller will let you know if you test case file was successfully loaded, and print out the commands available.

(screenshot1 here)

First we will step through one test case. Type ``n`` or ``next`` and press Enter. 
The first test case should be run, and the result printed in the Shell Pane.

(screenshot2 here)

Step through another test case by just pressing ``Enter``. 
This utilizes the previous command repeating feature. 
If no commands are specified, pressing ``Enter`` will run the previously entered command.

(screenshot 3 here)

Now let's try running a previous case. 
Type in ``p`` or ``previous`` and hit ``Enter`` as many times as you would like. 
Notice that the controller prints an error message when you attempt to run more test cases commands after the first one has been executed.

(screenshot 4 here)

Let's step forward four times (``next``). Make sure to take advantage of the previous command repeating feature. 
Now step through one more test case and...

You'll notice that our ``bin/rshell`` has finished executing. 

(screenshot 5 here)

There is no need to quit and restart ``cs100-runtests`` when this is encountered. 
Simply run the next test case and ``cs100-runtests`` will restart ``bin/rshell``. 
You will also be notified that ``bin/rshell`` has been restarted.

(screenshot 6 here)

Step through the next test case. This one backgrounds the shell.
Fortunately, ``cs100-runtests`` is able to use job control to bring back the stopped process. Try the last case.

(Screenshot 7 here)

Now that we have run out of test cases, let's try to run more. 
Step forward as many times as you would like to. The controller prints out an error notifying you that you have run out of test cases.

(screenshot 8 here)

Now that we have finished testing the ``shell``, let's grade it. First, zero out all of the grades by entering ``zero`` in the controller pane. 

(screenshot 9 here)

Let's say the student earned full credit for the objectives on lines 5 and 7.
To enter their grades, type in:
```
f 5
f 7
```
Perhaps they received 4 points for the objective on line 6:
```
g 6 4
```
And received 11 points for the objectives on lines 8 and 9:
```
g 8 11
g 9 11
```
(screenshot 10 here)

If you wanted to give a full grade for every objective on every line, run ``full``.

(screenshot 11 here)

Now that we are done testing and grading ``bin/rshell``, type ``exit`` and hit ``Enter`` to stop running ``cs100-runtests``.

Congratulations. You now know the basic features of ``cs100-runtests``.


```
cs100-runtests <shell> <testcasefile>
```
where ``<shell>`` is the shell you want to test (e.g. ``bin/rshell``, ``sh``, ``bash``, etc.) and <testcasefile> is the path to the file containing all of the test cases you would like to use on your shell.
These parameters are optional, as runtests will default to ``bin/rshell`` if no shell is entered, and it is possible to load a test case file within the program after the script has been run.

Three panes are created when ``cs100-runtests`` is started.
The left pane is the [Vim Pane](#the-vim-pane), which contains an open grade file that is created in the current directory. 
The upper right pane is the [Shell Pane](#the-shell-pane), where the user-input <shell> (or default ``bin/rshell``) is started.
The lower right pane is the [Runtests Controller Pane](#the-runtests-controller-pane). All commands for ``cs100-runtests`` are entered here.

##The Vim Pane
The Vim Pane is controlled with the following commands:
* ``g <line> <amount>`` or ``grade <line> <amount>`` places the amount entered as a grade on the line entered.
* ``f <line>`` places a full score on the entered line. 
  * Nothing happens when these commands are entered if ``<line>`` is not a properly-formatted grade line.
* ``zero`` makes all grades 0.
* ``full`` makes all grades maximum.

##The Shell Pane
The Shell Pane is controlled with the following commands:
* ``n`` or ``next`` runs the next test case loaded from the test case file.
* ``p``, ``previous``, ``b``, or ``back`` runs the previous test case loaded from the test case file.
  * Note: Pressing enter following a ``next`` or ``previous`` command will repeat it.
* ``l <testcasefile>`` or ``load <testcasefile>`` loads <testcasefile> into rshell, discarding previously loaded test cases.

##The Runtests Controller Pane
The Runtests Controller Pane is controlled with the following commands:
* ``c`` or ``clear`` clears the controller screen.
* ``e``, ``exit``, ``q``, or ``quit`` ends the program.
* ``h`` or ``help`` prints a small help message detailing the controls for ``cs100-runtests``.
  * ``h?``, ``?h``, ``?``, and ``??`` also print the help message.

