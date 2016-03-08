Workflow
--------

* Step 0: form a team of 2-3 members
* Step 1: give your team a name
* Step 2: get a github account for each member
* Step 3: one person per team forks the [CC-Summer-2016](https://github.com/cksystemsteaching/CC-Summer-2016/fork) repository
* Step 4: add the other team members to __your__ fork as collaborators
* Step 5: each team member clones that fork
* Step 6: check out the branch [selfie-master](https://github.com/cksystemsteaching/CC-Summer-2016/tree/selfie-master)
* Step 7: add a new file called TEAM to this branch
* Step 8: list the name of your team as well as your names in the TEAM file
* Step 9: implement solutions of assignments in this branch as well (see below)
* Step 10: commit regularly and push your changes to your fork
* Step 11: to submit solutions send pull requests from your fork via github.com to [selfie-master](https://github.com/cksystemsteaching/CC-Summer-2016/tree/selfie-master)

General Requirements
--------------------

All homework solutions:

* must be implemented in C* in the selfie.c file,
* must compile without warnings with starc and execute with mipster,
* must not break any existing selfie functionality, and
* must be ready for presentation on your machine in class.

Assignment 0: Your Team!
------------------------

__Deadline__: March 10, 10am (hard, no extensions)

Suppose your team name is *TheCompilables*. Change selfie such that it prints "This is TheCompilables Selfie" in a separate line on the console before doing anything else. All other functionality should be unaffected.

Assignment 1: Bitwise Shift Instructions
----------------------------------------

__Deadline__: March 17, 10am (hard, no extensions)

Implement in mipster the four logical bitwise shift instructions of MIPS called sll, srl, sllv, and srlv according to the <a href="https://en.wikipedia.org/wiki/MIPS_instruction_set">MIPS</a> standard. In your implementation use the selfie library functions for bitwise shifting and the selfie interface functions for decoding. Also, make sure that the selfie disassembler and debugger produce proper output for these instructions.