# Python loops intro

## for loops
For loops runs the same code for each value in a list.

A python list looks like this:

```python
[1, 5, 6, 9]
```

Be aware that the list might not be just numbers, but for simplicity we'll use numbers in this example.

A for loop looks like this:

```python
my_list = [1, 5, 6, 9]
for number in my_list:
  print(number)
# 1
# 5
# 6
# 9
```

### Range

`range()` is very useful when working with loop.

It is most useful when you need both the [_index_](lists.md#list-indexes) and the _value_ of a list.

For example, if you want to list out a chapter list, you can do it like this:

```python
chapters = ["The beginning", "The middle", "The end"]

count = len(chapters)

for index in range(count):
  print("chapter {}: {}".format(index, chapters[index]))
```

### Tasks

Using this list:

```python
my_list = [1, 2, 3, 4]
```

* Make a loop that prints each number in the list
* Make a loop that prints the number times two (2, 4, etc)
* (bonus): Make a loop that only prints numbers that can be divided by 2


## while loops

While loops continue running until something changes.

## Stopping a loop before it's done

You can stop any loop before it's normally done by calling `break`.

```python
while True:
	my_var = input("Write y to continue: ")
	if my_var != "y":
		break
```

### Tasks

* Using a while loop, keep adding together numbers written by the user until the user writes "stop"
* Make sure the program doesn't crash if the user writes something else that is not a number
	* Hint: Use `type`
