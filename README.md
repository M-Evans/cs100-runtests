# Runtests Features

## About
Runtests is tool that can be used to send test cases to terminal applications.

It's meant to be run on most Linux systems.
I've tested it in bash 4.2.53 with tmux 1.8 and bash 4.1.2 with tmux 1.6.
It can also be run by multiple users on the same system, but **not** by the same user multiple times on a given system.

## Advantages
* Test cases will be echoed to the terminal as if a user typed them (as opposed to redireciton that hides the input).
* Test cases can be played in order or reversed and replayed backwards. Runtests pauses after every newline.
* Control combinations can be sent (such as ``C-c`` and ``C-z``).

## Installation
Clone this project then copy ``runstests.sh`` into a folder indexed by your ``PATH`` (e.g. ``~/bin`` or ``/usr/local/bin``).
