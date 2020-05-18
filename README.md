# Compiler-Design-Valid-if-statements
Design of lexical and parser phase to check for valid if statements
The cd2.l contains the lex part of the program and cd2.y contains the yacc part of the program.
The repositor also contains an input file.
EXPLANATION OF THE CODE
                         The lex part of the code specifies the Lex command specification file that defines the lexical analysis rules.The file contains include statements for standard input and output  as well as for the y.tab.h file. Variables k, i, o, s and ln are declared for counting the number of keywords, identifiers, operators, separators and new lines respectively.When the file containing the problem statement is given as input to the program, the rules in lex recognizes  keywords, identifiers, operators, separators and newlines and respective tokens are generated to pass on to yacc program.The variables declared above are incremented as an action for a rule.The y.tab.h file contains definitions for the tokens that the parser program uses. 
        The yacc part of the code specifies the yacc command grammar file that defines the parsing rules, and calls the yylex subroutine created by the lex command to provide input.



The file contains the following sections:
•	Declaration section
      This section   contains entries that:
	->Includes standard I/O header file
	->Declarations for any variables or constants used in other parts of the grammar file
•	Rule section
    The rule section defines the rules that parse the input stream .
->%token-Lists the tokens which comes from lex tool with their type
•	Program section
       The program section contains the following subroutines:
->	main : The required main program that calls the yyparse subroutines to start the program
->	yyerror(str) : The error-handling subroutine only prints a syntax error message.It uses the variable ln to print the line number where the error has occurred.
->File *yyin : Input file for lex program and defaults to stdin
If the input statement is as per the defined productions then the program prints “Program compiled successfully “ message with the number of keywords, identifiers, separators and operators.If the given input is syntactically incorrect, the program prints “Error at line (the line number where the error has occurred)” along with the message “syntax error”.


