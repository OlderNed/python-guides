# Overview

Operators are "tools" that you use while writing code. For a larger overview, see [this guide](https://www.tutorialspoint.com/python/python_basic_operators.htm).

# Basic operators

The most basic iterator in Python is `=`. It does not mean quite the same as in maths. Instead, it is used for what we call `assignment`, in the sense that it's used to assign a value to a variable.

```python
a = 2
```

We have now assigned the value 2 to the variable a. This means that unless we assign a new value to `a`, it now represents the value 2:

```python
print(a) # 2
a + 2 # 4
```

## Assignment operators

The first operator we looked at, `=`, is an assignment operator. There are also more assignment operators, used for more special cases. The most useful ones are the math assignment operators:

* `+=` adds a value to the axisting value
* `-=` subtracts a value from the existing value
* `*=` multiplies the existing value by a given value
* `/=` divide the existing value by a given value

There are more, like `**=` and `%=`. You can imagine what they do based on the info in [the math section of the numbers guide](numbers.md#math)`

Here are some examples of how to use them:

```python
a = 2
a += 1 # 3
a -= 1 # 2
a *= 2 # 4
a /= 2 # 2
```

## Comparison operators

Comparison operators work mostly like in maths, but there are some important distinctions.

Because `=` is already taken as an assignment operator, we cannot use the same to compare two values. That's why the basic equality operator is `==`.

```
2 + 2 == 4 # True
```

Comparison operators always return a True or False value. We don't always see that, but it's good to keep it in mind when imagining what a piece of code does.

For example, these two statements are equal:

```python
if True:
    print("This is true")

if 1 == 1:
    print("This is true")
```

To emphasize this further, we could also write the latter like this:

```python
if (1 == 1) == True:
    print("This is true")
```

Other useful comparison operators are:

* `!=` Not equals - the opposite of `==`
* `<` and `>` Less than and greater than
* `<=` and `>=` Less or equal than and Greater or equal than

Usage:

```python
3 < 4 # True
3 < 2 # False
3 > 3 # False
3 >= 3 # True
3 == 3 # True
3 != 3 # False
3 != 4 # True
```

## Logical operators

Some times you want to check more than one comparison at a time. You can use logical operators to do this. In python, the most common logical operators are `and`, `or` and `not`. They can be used like in English:

```python
True and True # True
True and False # False
True or False # True
False or False # False
not True # False
not False # True
```

In usage:

```python
a = 2
b = 4

if a > 1 and b > 1:
    print("Both values are more than 1")

if a > 3 and b > 3:
    print("This won't print, because only b is above 3")

if a > 3 or b > 3:
    print("At least one of the values are above 3")

if a > 5 or a > 5:
    print("This won't print, since none of the values are above 5")
```

You can combine multiple logical operators as well. It's a good idea to use parentheses to indicate what you really mean.

```python
a = 1
b = 2
if a != b and (a < b or b > 5):
    print("This will print, because a isn't equal to b, and a is less than b. The last check doesn't matter since it was that *or* the previous one")
```
