# Variables

Variables are used to store information that can vary. A basic variable can be written like this:

```python
a = 5
```

Variables are useful because they can change:

```python
a = 5
print("a is", a) # a is 5
a = 4
print("a is", a) # a is 4
```

This may not seem that useful yet, but it will become more apparent as we start working with more complex examples later on.

# Functions

Functions, in some cases also called functions (we won't get into why, just remember that both terms can appear), are named pieces of code. You can use functions provided by the language, or *libraries*, or you can write your own.

A function can be recognized by the ending parentheses: `len()`. Functions may sometimes expect variables as input. For example `len()`, which calculates the length of a list or a string, needs a list or a string as input:

```python
len("test") # 4
```

You can assign the result of a function to a variable:

```python
a = "test"
b = len(a)
print(a, "is", b, "characters long") # test is 4 characters long
```


# Types

Variables can have different types. These types have different properties. The most basic types are [numbers](numbers.md) (divided into integers (shortened to `int`) and floating point numbers (shortened to `float`)), and [strings](strings.md) (shortened to `str`), which represent text.

You can read more about the types themselves in the linked documents above.

To check what type a variable is, use the `type()` function:

```python
a = "test"
type(a) # str
b = 1
type(b) # int
c = 2.5
type(c) # float
```

# Math

You can do math with numbers. They can either be directly written numbers (like `1`) or variables that are numbers.

```python
a = 1 + 1 # 2
b = a * 2 # 4
```

You can read more about math in the [numbers document](numbers.md#math).

# Printing

We've used the print function in some of the examples above, but it's worth mentioning it more speicifically too. `print()` is a helpful function that prints whatever it receives to the console. It can be used both as useful output (for command line based programs) and as *debug* information when writing a program.

`print()` is special in that it can work with any type and any number of inputs:

```
print(5) # 5
print(42, "is everything") # 42 is everything
```