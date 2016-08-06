# Polish-Notation
Sessional Project of Data Structure course of B.Sc. in CSE

### Introduction
Polish notation is normally known as prefix notation. It is also known as reverse polish notation or reverse notation. It is a combination of operands and constants. We can use this for logical, arithmetical or in algebra equations. It can contain also parenthesis. The Polish logician Jan Łukasiewicz invented this notation around 1920 in order to simplify sentential logic. While no longer much used in logic, it has since found a place in computer science.

### Problem Definition
Infix notation is popular in many ways. It can represent arithmetic and logical formula notation. But here we use only arithmetic notation.

Computer can evaluate any equation by using translator program. But here we will take an infix expression like 2 + 2 or 3 * 4 /5 etc. But may programming language can not determine the value directly. It transform this like 2 2 + or 3 4 5 / * this form. In infix notation, unlike in prefix or postfix notations, parentheses surrounding groups of operands and operators are necessary to indicate the intended order in which operations are to be performed. In the absence of parentheses, certain precedence rules determine the order of operations.

For this we will use a postfix conversion program to transform this. Then we will create a new function, which will evaluate the value of that postfix expressions.

