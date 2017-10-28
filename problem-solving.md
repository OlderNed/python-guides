# Problem solving with Python

Knowing how to handle strings, loops, lists and more, is all needed to write python programs. But it is also important to know when you use each tool, and where to start when confronted with a programming task.

## To loop or not to loop

Loops are very useful, and most programs will use loops at some point. You will most likely need a loop if you're going to do one of the following:

* Read a file with multiple lines
* Do the same calculation on multiple values
* The input to your [function or method](functions.md) is a list
* Handle a string as a list of characters

### The kinds of loops

There are two main kinds of loops to remember: `for` and `while`. The general rule is that you use `for` when you have a list or know how many times you need to do something, while you use `while` when you need to do something until a condition changes (like for example a value reaches a threshold, or the user inputs something).

They are written like this:

```python
for value in [0, 1, 2, 3]:
  # Do something for each value, like
  print(value)


from random import randint
my_number = 0
while my_number < 20:
	my_number = randint(0, 50)
	print(my_number)
```

## Strings and numbers

A good rule of thumb is that numbers is for math, string is for everything else. You can convert between them using `int()` (make a natural number), `float()` (make a decimal number), and `str()` (make a text).

It can be confusing to work with these if you're used to working with only numbers. It's a good idea to remember that you can use `type()` to check what type you're dealing with.

```python
type(5) # int
type(5.5) # float
type("text") # str
```

Refer to the separate guides for strings and numbers for more details.

### Common mistakes

If you ever see 1+1 become 11, you're probably dealing with strings.

```python
a = "1"
a + a # 11
int(a) + int(a) # 2
```

## What if

The `if` statement is what we call a conditional expression. It is intended to read like English:

> If (something is true): Do something.

Or in code:

```python
if my_fact == True:
  print("It's true!")
```

When you write `if` statements, it is helpful to think about it like a English sentence. The `:` can be read as "run the following code", or just "do this":

```python
if a > 5:
  print(a)
# Reads as: If the value of variable a is more than 5, print variable a.

if a == b:
  print("They're equal!")
# Reads as: If a is equal to b, print "They're equal!".
```

*Note that comparing values in python is done by using two equal signs (`==`). This is to differentiate between assignment and comparisons. See [basics](basics.md) for more details.*

### Common mistakes

If an `if` statement is not evaluated to True or False, it will assume you want to check if a value exists or not.

```python
a = None
b = "Something"

if a:
  print("a")

if b:
  print("b")

# This program would print `b`.
```

## Scoping - Where to put what when

Scoping indicates where a variable is accessible. Let's look at an example:

```python
a = 1

def some_fun():
  b = 2

  for c in range(b):
    d = 3
    print(a, b, c, d)
```

In the python code above, there are three *scopes*.

`a` is in what's called the *global scope*. This means that this variable is available in the entire file. While this can be useful, it is generally advicable not to declare variables in the global scope. There are many reasons for this, for example it can be difficult to avoid issues where multiple functions overwrites the same value.

`b` is in the scope of `some_fun()`. This means that only code inside `some_fun()` can write to and read this variable. This is a good place for variables that will be read or manipulated throughout the function. You might also want to place variables that will be returned at the end of the function here, especially if the value is agregated (like a counter or a list that will be filled).

`c` is *implicitly* in the scope of the for loop, by the fact that it's a part of the loop statement. Here it will contain each value of `range(b)` for each iteration of the loop (`0` for the first iteration and so on).

`d` is also in the scope of the for loop. This means that it is only available inside the loop. It also means that it will be redefined for each iteration of the loop.

Notice how the indentation (space on the left) indicates which scope each variable is in.

### Scoping rules of thumb

* Scoping is indicated by indentation
* Avoid using the global scope if possible
* Write your variables in the narrowest scope possible (to avoid accidental redifinitions of the same names)
* If you update the value or add to a list throughout a function, write it in the function scope at the top
* Outside of scoping, you also need to remember that a variable must be defined before it's used
