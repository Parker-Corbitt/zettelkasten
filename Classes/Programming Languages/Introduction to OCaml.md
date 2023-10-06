***
### Language Basics: Chapter 1/2
##### Expressions, Values, and Basic Functions
- *Expressions*: something which still can be computed
- *Values*: An expression on which no more computation can be performed
	- All values are expressions, but not vice versa
- Here are some examples of values that are also expressions
```
42 (* an integer value *)
3.14 (* a floating-point value *)
"hello" (* a string value *)
true (* a boolean value *)
```

- Here is an example of both a conditional expression, and an expression using a function call
```
let x = 5 in
if x > 0 then x + 1 else x - 1

let square x = x * x in
square 5
```

- Here, let is being used to define both a variable and a function
	- The general formula for functions is shown below
```
let name (parameters) = expression in
body
```

- Say I wanted to test this function for proper output.  I could do something like this
```
let square x = x * x in
assert (square 5 = 25)
```

- If the assertion passes, the code continues as normal
- If the assertion fails, the program stops and an exception is raised

##### Recursion
Recursion is a topic that is very crucial to not only take full advantage of what OCaml offers, but to take full advantage of what any functional language can do.

- Here is an example of a factorial function
```
let rec factorial n =
  if n = 0 then 1
  else n * factorial (n - 1)
```
- In any recursive function, you always need a base case which will stop the recursive call

##### Tail Recursion
Tail recursion is a technique used to avoid overflowing the stack. By using this method, stack space is actually made constant, rather than growing with each call. It's possible because the recursive call is the last operation done within a function, and the result is immediately returned. No previous state of any variable needs to be remembered, so the same space in the stack can be constantly reused.

- Here is an example of a tail recursive function to compute the nth number of *n*th number of the Fibonacci sequence
```
let fib n =
  let rec fib_helper n acc1 acc2 =
    if n = 0 then acc1
    else fib_helper (n-1) acc2 (acc1+acc2)
  in fib_helper n 0 1
```

#####  Documentation
- Comments are structured as such
```
(**This is a comment*)
(**@author Parker Corbitt)
```