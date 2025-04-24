# cmpsc442-homework-4-solved



**<span style='color:red'>TO GET THIS SOLUTION VISIT:</span>** https://www.ankitcodinghub.com/product/cmpsc442-homework-4-solved-2/

1. Propositional Logic [65 points]

In this section, you will implement a collection of classes corresponding to logical expressions, a simple knowledge base, and algorithms for propositional logic inference via truth table enumeration and resolution. All expressions will be subclasses of the provided base Expr class. The fragment of logic we will be working with can be defined recursively as follows:

Atom: Atom(name) is an expression.

Negation: If $e$ is an expression, then Not($e$) is an expression.

Conjunction: If $e_1,e_2,\ldots,e_n$ are expressions, then And($e_1,e_2,\ldots,e_n$) is an expression.

Disjunction: If $e_1,e_2,\ldots,e_n$ are expressions, then Or($e_1,e_2,\ldots,e_n$) is an expression.

Implication: If $e_1$ and $e_2$ are expressions, then Implies($e_1$, $e_2$) is an expression. Biconditional: If $e_1$ and $e_2$ are expressions, then Iff($e_1$, $e_2$) is an expression.

You will find that a generic hash function has been defined for the Expr class, and that the initialization methods for each of its subclasses have been provided. These should not be altered. Combined with the methods for equality checking to be implemented below, this will ensure that expressions behave as expected when used as elements of sets.

1. [3 points] First read through and understand the provided __init__ methods for the Atom, Not, And, Or, Implies, and Iff expression subclasses, keeping in mind that expressions will be considered immutable for our purposes. In particular, review the *args syntax (link) and frozenset class (link) if needed. The former allows for convenient n-ary conjunctions and

disjunctions, and the latter is used to ensure immutability.

We use sets rather than lists for conjunctions and disjunctions to guarantee that, e.g., all 24 permutations of the conjuncts in the expression $A \land B \land C \land D$ will be equivalent. Moreover, you may find that certain set functions such as union and set difference will prove useful later on. As a first exercise, implement the __eq__(self, other) methods in each subclass, which will be called when expressions are compared using the == operator. You should check for syntactic equality only, in the sense that two expressions should be considered equal only if they are of the same class and have the same internal structure. No simplification should be performed. As a special case, Iff(a, b) should be equal to Iff(b, a). Hint: Each of these can be implemented in a single line.
