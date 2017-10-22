## Lists basics

Lists are very important, because you often work with a series of values at once.

A list can contain multiple values.

An empty list looks like this:

```python
a = []
```

A list of numbers can look like this:

```python
a = [1, 2, 3, 4]
```

A list of strings can look like this:

```python
a = ["a text", "another text", "a third text"]
```

## Working with lists

A very common use case for a list is to do the same operation on each value in a string. That's why this is a basic feature of Python, and it looks like this:

```python
a = [1, 2, 3]
for num in a:
    print(num * 2)
# 2
# 4
# 6
```

In short, this will run the `print` method (where it prints the value multiplied by 2) for each number in the list `a`.

You can get the length of a list using `len()`:

```python
a = [1, 2, 3]
b = len(a)
print(b) # 3
```

Adding value to an existing list is done like this:

```python
a = [1, 2, 3]
a.append(4)
# a == [1, 2, 3, 4]
```

You can access and modify values in a list by using square brackets. You use the index (an integer, starting from 0) of the value to reffer to it.

```python
a = [5, 3, 2, 3]

# Accessing values
a[0] # 5
a[1] # 3
a[2] # 2

# Modifying value
a[0] = 8 # a is now [8, 3, 2, 3]
a[1] = 4 # a is now [8, 4, 2, 3]
```

You can also access the list from the end, using negative indicies. Be aware that they start at `-1`, not `-0` (because -0 == 0, so you can't differentiate between them).

```python
a = [5, 4, 3, 2]
a[-1] # 2
a[-2] # 3

a[-1] = 8 # a is now [5, 4, 3, 8]
```

Lists can be combined using + (in the same way as strings):

```python
a = [1, 2, 3] + [4, 5, 6]
# a == [1, 2, 3, 4, 5, 6]
```

## Tasks

* Create a method that takes a list as an argument and adds a value to it
* Create a method that reverses a list
