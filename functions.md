## Writing a function

In python, you "define" functions like this:

```python
def my_function():
    print("This s a function that prints this text")
```

A function can have one or more parameters (sometimes called arguments or just inputs). These are listed in the parentheses:

```python
def add_numbers(first, second):
    return first + second

a = add_numbers(1, 2)
print(a) # 3
```

The `return` in the previous example indicates what result is given to the caller of the function, and is the reason why the result of first + second is available in `a`.

## Functions and methods

Functions and methods, are named pieces of code. You can use functions and methods provided by the language or *libraries*, or you can write your own.

There are differences between functions and methods, but those are mostly academic in nature. In this guide you'll mostly find functions, and the only thing to keep in mind is that many people use these terms interchangeably. 

If you really want to know the difference (warning, requires more knowledge than this guide provides), you can find a good explanation [here](https://www.quora.com/Whats-the-difference-between-a-method-and-function-in-Python-I-have-Googled-and-found-contradicting-views-Some-seem-to-use-them-interchangeably-Can-you-give-an-example-in-code-to-clarify/answer/Jim-Dennis-1?srid=3yos).