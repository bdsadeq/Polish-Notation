# Polish-Notation
Sessional Project of Data Structure course of B.Sc. in CSE

### Introduction
Polish notation is normally known as prefix notation. It is also known as reverse polish notation or reverse notation. It is a combination of operands and constants. We can use this for logical, arithmetical or in algebra equations. It can contain also parenthesis. The Polish logician Jan Łukasiewicz invented this notation around 1920 in order to simplify sentential logic. While no longer much used in logic, it has since found a place in computer science.

### Problem Definition
Infix notation is popular in many ways. It can represent arithmetic and logical formula notation. But here we use only arithmetic notation.

Computer can evaluate any equation by using translator program. But here we will take an infix expression like 2 + 2 or 3 * 4 /5 etc. But may programming language can not determine the value directly. It transform this like 2 2 + or 3 4 5 / * this form. In infix notation, unlike in prefix or postfix notations, parentheses surrounding groups of operands and operators are necessary to indicate the intended order in which operations are to be performed. In the absence of parentheses, certain precedence rules determine the order of operations.

For this we will use a postfix conversion program to transform this. Then we will create a new function, which will evaluate the value of that postfix expressions.

### Solution
There are two steps to solve a polish notation. Input will be an expression in infix form.

 - Step 1 : First convert this infix expression to postfix or reverse notation.
 - Step 2 : Evaluate the value of postfix notation.

### Algorithm
Algorithm for transforming  infix expressions into postfix expressions.

Algorithm Polish(Q,P)

//Suppose Q is an arithmetic expression written in infix notation. This algorithm finds the equivalent postfix expression P.

 - 1. Push “(“ onto STACK, and add “)” to the end of Q.
 - 2. Scan Q from left to right and repeat steps 3 to 6 for each element of Q until the STACK is empty.
 - 3. If an operand is encountered, add it to P.
 - 4. If a left parenthesis is encountered, push it onto STACK.
 - 5. If an operator (X) is encountered, then
 - a. Repeatedly pop from STACK and add to P each operator (on the top of STACK) which has the same precedence as or higher precedence than (X).
 - b. Add (X) to STACK.
 - 6. If a right parenthesis is encountered, then
 - a. Repeatedly pop from STACK and add to P each operator (on the top of STACK) until a left parenthesis is encountered.
 - b. Remove the left parenthesis. (Do not add the left parenthesis to P).
 - 7. Exit.

Algorithm for evaluation of a postfix expression.

Algorithm Evaluation (Postfix expression)

//This algorithm finds the value of an arithmetic expression P written in postfix notation.

 - 1. Add a right parenthesis “)” at the end of P. (This acts as a sentinel).
 - 2. Scan P from left to right and repeat steps 3 and 4 for each elements of
 - P until the sentinel “)” is encountered.
 - 3. If an operand is encountered, put it on STACK.
 - 4. If an operator (X) is encountered, then
 - a. Remove the two top elements of STACK, where A is the top element and B is the next to top element.
 - b. Evaluate B(X)A.
 - c. Place the result of (b) back on STACK.
 - 5. Set value equal to the top element on STACK.
 - 6. Exit.
 
### Program Development
In postfix notation the operators follow their operands; for instance, to add three and four one would write "3 4 +" rather than "3 + 4". If there are multiple operations, the operator is given immediately after its second operand; so the expression written "3 − 4 + 5" in conventional infix notation would be written "3 4 − 5 +" in RPN: first subtract 4 from 3, then add 5 to that. An advantage of RPN is that it obviates the need for parentheses that are required by infix. While "3 − 4 * 5" can also be written "3 − (4 * 5)", that means something quite different from "(3 − 4) * 5", and only the parentheses disambiguate the two meanings. In postfix, the former would be written "3 4 5 * −", which unambiguously means "3 (4 5 *) −".

This program is stack base program. Operands are pushed onto a stack, but when an operation is performed, operands will be popped from that stack and result will be pushed again.

 - 1.	Build a stack.
 - 2.	Transform infix to postfix.
 - 3.	Evaluate that postfix value.
 
### Result
Using this idea and algorithms we build a program to convert an infix expressions to postfix expressions and evaluate the value of that postfix expressions.

### Example
Let, an infix expression is 1 + ( 2 * 3 – ( 4 / 5 ^ 6 ) * 7 ) * 8

Procedure into postfix

![Preview Loading ...](http://image.sadequr.com/github/polish_notation/procedure_into_postfix.jpg)

Let, an postfix expression is 7 6 9 + * 12 4 / -

Procedure to evaluate the value

![Preview Loading ...](http://image.sadequr.com/github/polish_notation/procedure_to_evaluate_the_value.jpg)

### Limitations



