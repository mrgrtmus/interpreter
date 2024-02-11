# python-interpreter
The following defines a simple language, in which a program consists of assignments and each variable is assumed to be of the integer type. 
(1) detect syntax errors; 
(2) report uninitialized variables; 
(3) perform the assignments if there is no error and print out the values of all the variables after all the assignments are done.

Program:
	Assignment*

Assignment:
	Identifier = Exp;

Exp: 
	Exp + Term | Exp - Term | Term

Term:
	Term * Fact  | Fact

Fact:
	( Exp ) | - Fact | + Fact | Literal | Identifier

Identifier:
     	Letter [Letter | Digit]*

Letter:
	a|...|z|A|...|Z|_

Literal:
	0 | NonZeroDigit Digit*
		
NonZeroDigit:
	1|...|9

Digit:
	0|1|...|9
