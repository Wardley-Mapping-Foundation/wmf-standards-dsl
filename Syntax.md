A map description in WMDL consists of a sequence of declarative expressions, each of which itself consists of a defined sequence of tokens.

		title Tea Shop
		anchor Business [0.95, 0.63]
		component Cup of Tea [0.79, 0.61] label [19, -4]
		component Cup [0.73, 0.78]
		Business->Cup of Tea
		Cup of Tea->Cup

# Expression
 An Expression is always a single line. The tokens forming an expression and their order within an expression is well-defined. Expressions do not have to follow a specific order. However, dependencies through references between expressions are an exception, where a certain order must be adhered to.   
e.g:

	component Cup [0.73, 0.78]

# Token
A token is a part of an expression. A token represents a symbol of the grammar where each symbol is of a given type, e.g. _[Identifier](Identifier.md)  

The above expression consists of three Tokens:
* component
* Cup
* [0.73, 0.78]

