# Strings

## What are strings

Strings is how we represent text in Python (and most other programming languages).

To create a string, use `"` or `'` like this:

```python
some_string = "This is a string"
```

String is also the default type when using input:

```python
my_input = input("Write something: ")
# my_input will always be a string, even if the user writes only numbers
```

## Converting strings into other types

Some times you want to convert strings into other types. The most common use case is when you've used `input()` to get a value from the user.

If you want to do math with the input, you can use `int()` (natural numbers, also known as integers) or `float()` (decimal numbers, also known as "floating point").
 
```python
my_input = input("Write a number: ")
# let's imagine that the user wrote 5
nat_num = int(my_input) # 5
dec_num = float(my_input) # 5.0
```

See the separate guides for numbers to learn more about doing math in python.

### Tasks

* Make a function that reads a number from the user (using `input()`) and returns the number multiplied by two
* Make a function that reads a number from the user (using `input()`) and returns the number multiplied by pi (using 3.14 or Math.pi, that's up to you)
	* Can you still use `int()`? Why or why not?

## Strings as lists

Strings can behave as lists. This is very useful when manipulating text. 

### Examples

```python
text = "Python can be kind of fun"
for character in text:
	print(character)
# Will print one character per line:
# P
# y
# t
# h
# …
```

We can also access characters like we access a specific element in a list:

```python
text = "Hello"
print(text[1])
# e
```

If we want to know how many characters are in a string, we can use the function `len()`:

```python
text = "Hello"
length = len(text)
print(length) # 5
```

### Tasks

* Make a function that prints the number of characters in the string the user wrote.
* Make a function that prints the number of characters in a file
	* See the file handling guide for how you read files
	* Remember that you will need to add together the sum  of the number of characters on each line

## Formatting strings

String formatting is a comprehensive topic. Instead of covering everything in detail here, I'll reffer you to [this guide](https://www.digitalocean.com/community/tutorials/how-to-use-string-formatters-in-python-3) by DigitalOcean. Most python 3 books also has a section on string formatting.

### Tasks

```python
a = 3.14159265358
b = 4.2
c = 123.456
```

Using the above variables, print a string that formats each value with two decimal points. The result should be:

```sh
a is 3.14, b is 4.20, c is 123.45
```
