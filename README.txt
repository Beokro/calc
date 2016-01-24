Xujia Cao
01/24/2016
cs160 calc 

      I first rewrite the garmar in LL1 format and found the FIrst and second set. Then it is pretty straight forward to finish the parsing.

      About making calculator actually work. I first try make a local variable current variable in Expr, Term and Facotr function but I found it is not a very good way to do it. Instead I add a stack<int> in parse class. Everytime in function Factor it reads a number, I will push a number to the stack. When I encounter a operator, I will wait for it evalue the second part of equation(it could be a number of a expression) and then I will get and pop the top 2 number from the stack and evalue them based on the operator and then push it back to the stack. I will print the result when I am suppose to eat . and . is next token.
