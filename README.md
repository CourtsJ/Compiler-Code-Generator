# Compiler-Code-Generator
Compiler for a  small programming language
Based of a given template.

The compiler will accept programs with the following syntax:

Program = Statements
Statements = Statement (; Statement)*
Statement = If | While | Assignment

If = if Comparison then Statements end
While = while Comparison do Statements end
Assignment = identifier := Expression

Comparison = Expression Relation Expression
Relation = = | != | < | <= | > | >=

Expression = Term ((+ | -) Term)*
Term = Factor ((* | /) Factor)*
Factor = (Expression) | number | identifier

Identifiers contain only lower-case letters. Numbers are represented by non-negative integers in decimal notation. An example of a program using the above BNF extended by read and write statements is:

read n;
sum := 0;
while n > 0 do
  sum := sum + n;
  n := n - 1
end;
write sum
