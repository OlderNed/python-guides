# Working with numbers in python

## Integers and floats

Numbers in Python are divided into integers (`int`) and floating point (`float`) numbers. To separate between them, floating point numbers are always shown with decimals when printed:

```
float(5) # 5.0
```

When working with numbers, you can combine `int` and `float` in your math operation. The general rule is that `int` + `int` stays `int`, while any operation containing at least one `float` value will become `float`. This is useful to know if you're doing math with data from the user. If you want the precision of decimal numbers, you can define one of your numbers as float to ensure you get a decimal number as the answer:

```
my_value = eval(input("Write a number: "))
result = my_value / float(3)
print(result) # Result will be a floating point, even if the input is 9 (it would be shown as 9.0).
```

## Math

Math in python is quite straight forward: As long as your variables are numbers, you can do math. All the common operators are present:

```
1 + 1 # 2
3 - 2 # 1
2 * 2 # 4
6 / 3 # 2
```

Be aware that shorthand math annotation is not available:

```
a = 2
b = 3
print(ab) # NameError: name 'ab' is not defined
```

This is because you can have multi-character variable names, so python cannot know if you mean `a * b` when writing `ab`.


There are also some more special operators:

```
3 ** 3 # 27 - ** is the exponent operator. Some other languages and math notation often use ^ for this.
5 % 2 # 1 - % is the modulus operator (see section below)
```

You can combine operators like you would in any calculator, and you can use parentheses `(` and `)` as you normally would:

```
3 * (2 + 2) # 12
```

### Modulus

The `%` is an operator that may not seem familiar. Modulus is used in "Modular arithmetic" ("Modulær aritmetikk"), which is maths that is performed with only natural numbers (integers). Using `%` will give you the number left over when performing divison with natural numbers.

```
5 % 2 # 1

# This is the same as:
a = 5 / 2 # 2
b = 5.0 / 2.0 # 2.5
c = b - a # 0.5
c * 2 # 1
```