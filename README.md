## MathParser Swift ##


----------
A fast and lightweight math parser built in Swift.
It parse a mathematical infix expression like:
``` 
10 ^ 2 + (7 * 8) + cos(x) 
```
First of all, the parser tokenize the expression with regex and retrieve the tokens:

```
Type: (, 		Range: {0, 1}, 	String: (, 	 Value: nil
Type: Number, 	Range: {1, 2}, 	String: 10,  Value: Optional(10.0)
Type: Operator, Range: {4, 1}, 	String: ^, 	 Value: nil
Type: Number, 	Range: {6, 1}, 	String: 2, 	 Value: Optional(2.0)
Type: Operator, Range: {8, 1}, 	String: +, 	 Value: nil
Type: (, 		Range: {10, 1}, String: (, 	 Value: nil
Type: Number, 	Range: {11, 1},	String: 7, 	 Value: Optional(7.0)
Type: Operator, Range: {13, 1} 	String: *, 	 Value: nil
Type: Number, 	Range: {15, 1}, String: 8, 	 Value: Optional(8.0)
Type: ), 		Range: {16, 1}, String: ), 	 Value: nil
Type: Operator, Range: {18, 1}, String: +, 	 Value: nil
Type: Operator, Range: {20, 3}, String: cos, Value: nil
Type: (, 		Range: {23, 1}, String: (, 	 Value: nil
Type: Unknown, 	Range: {24, 1}, String: x, 	 Value: nil
Type: ), 		Range: {25, 1}, String: ), 	 Value: nil
Type: ), 		Range: {26, 1}, String: ),   Value: nil
```

Once the expression has been tokenized,
