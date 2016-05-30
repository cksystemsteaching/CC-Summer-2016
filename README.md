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

* must be implemented in C\* in the selfie.c file,
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

Implement in mipster the four logical bitwise shift instructions of MIPS called `sll`, `srl`, `sllv`, and `srlv` according to the <a href="https://en.wikipedia.org/wiki/MIPS_instruction_set">MIPS</a> standard. In your implementation use the selfie library functions for bitwise shifting and the selfie interface functions for decoding. Also, make sure that the selfie disassembler and debugger produce proper output for these instructions.

Assignment 2: Bitwise Shift Operators (Scanning, Parsing)
---------------------------------------------------------

__Deadline__: April 7, 10am (hard, no extensions)

Implement in starc scanning and parsing of the two bitwise shift operators of C written `<<` and `>>`. Extend the scanner and parser of starc accordingly. In particular, invent unique tokens for the new symbols and make sure that the scanner properly distinguishes `<` from `<<` and `>` from `>>`. Then, add a new production rule for the new symbols to the C\* grammar (in the grammar.md file) such that their precedence is between `+` and `<` as specified for <a href="https://en.wikipedia.org/wiki/Operators_in_C_and_C%2B%2B">C operators</a>. Finally, add a procedure for parsing the new symbols to starc according to the new production rule (hint: use a copy of the procedure for parsing simple expressions as template). Test your implementation on syntactically correct as well as syntactically incorrect C\* programs using the two shift operators.

Assignment 3: Bitwise Shift Operators (Code Generation, Self-Compilation)
-------------------------------------------------------------------------

__Deadline__: April 14, 10am (hard, no extensions)

Implement in starc code generation for the shift operators `<<` and `>>` of Assignment 2 using the logical bitwise shift instructions of Assignment 1. The semantics of both operators should be logical bitwise shift meaning that zeros are shifted in on either end (even for `>>` of negative numbers). Change the implementation of the leftShift and rightShift procedures using `<<` and `>>` instead of `*` and `/` such that the original semantics of both procedures is preserved. Avoid calling the twoToThePowerOf procedure in your solution. Finally, demonstrate that self-compilation of selfie still works and check which procedures are now the most called procedures during self-compilation.

Assignment 4: Constant Folding
------------------------------

__Deadline__: April 28, 10am (hard, no extensions)

Implement constant folding in arithmetic expressions. For this purpose introduce a grammar attribute that represents the value of an expression if available. Use the attribute to evaluate constant expressions at compile time and delay code generation for arithmetic expressions accordingly. Represent the attribute by a call-by-reference parameter to the involved parsing procedures. The parameter needs to carry the value and a flag that indicates if a value is available. Use exactly one instance of the parameter for parsing an arithmetic expression. Test your code by including code snippets in `main` that are subject to constant folding. Also, make sure that self-compilation of selfie still works.

Assignment 5: Arrays
--------------------

__Deadline__: May 6, 10am (hard, no extensions)

Implement one-dimensional arrays with support of constant folding in size and index expressions. As usual, extend the C\* grammar first and then implement parsing and code generation. Focus on global array variables first. Then implement local array variables and finally array parameters. To test your code modify selfie such that the `SYMBOLS` variable is declared and accessed as array of integers `int SYMBOLS[28]`.

Assignment 6: Two-Dimensional Arrays
------------------------------------

__Deadline__: May 12, 10am (hard, no extensions)

Extend your implementation of one-dimensional arrays to two-dimensional arrays. To test your code modify selfie such that the `SYMBOLS` variable is declared and accessed as two-dimensional array of integers `int SYMBOLS[28][2]`. For each `symbol` store the symbol's string in `SYMBOLS[symbol][0]` and count the number of its occurrences in the parsed input in `SYMBOLS[symbol][1]`. After compilation output `SYMBOL[symbol][1]` on the console for each `symbol`.

Assignment 7: Struct Declarations
---------------------------------

__Deadline__: May 19, 10am (hard, no extensions)

Implement global and local pointer-to-struct declarations as well as pointer-to-struct parameters but leave struct access to the next assignment. As with arrays implement global declarations first, then local declarations, and finally parameters. To test your code declare a `struct` for symbol table entries in selfie but do not actually use the `struct`.

Assignment 8: Struct Access
---------------------------

__Deadline__: May 27, 10am (hard, no extensions)

Implement `struct` access. To test your code complete the port of the symbol table in selfie to structs and demonstrate self-compilation.

Assignment 9: Boolean Operators (Individual)
--------------------------------------------

__Deadline__: June 9, 10am (hard, no extensions)

Implement the Boolean operators `&&`, `||`, and `!` with lazy evaluation. Occurrences of `&&` and `||` in the same expression are not required to work. However, occurrences of `!` and `&&` as well as `!` and `||` in the same expression must work. To test your code replace the `isCharacterDigit` function by an adequate Boolean expression and demonstrate self-compilation.

Assignment 10: Boolean Operators (Algebra)
------------------------------------------

__Deadline__: June 16, 10am (hard, no extensions)

Complete your implementation of the Boolean operators `&&`, `||`, and `!` such that any occurrences of the operators in the same expression are supported. To test your code replace the `isCharacterLetter` function by an adequate Boolean expression and demonstrate self-compilation.