* TOC
{:toc}

# Interactive Area

Any code that is shown can be run here. Simply copy and paste it below and run it:

<iframe src="https://trinket.io/embed/python3/9554865385" width="100%" height="356" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

# String Indexing

Understanding strings and how to manipulate them is a crucial part to understanding Python programming. There are a lot of core principles that lead off from understanding and manipulating strings. There are also a lot of similarities between strings and lists!
Lets first look at a few important concepts. Strings in Python are either surrounded by single quotation marks or double quotation marks. And as we saw before, we can assign it to a variable:

```python
string_one = "Python Course"
print(string_one)
string_two = '1000'
print(string_two)
```

Run the code to see the output you get.

In other programming languages single characters like “b“ or “4“ are a unique data type on its own and often referred to as a char or character data type. In Python, it is still considered a string just of length 1. And just like we accessed items in a list through their index positions, we can also access single or multiple characters of a string using their associated index:

```python
print(string_two[0])
print(string_two[0])
print(string_one[:])
print(string_one[0:4])
print(string_one[-1])
```

Run the code to see the output you get.

This should all be familiar to you as you have seen it with lists. The second last command we have seen in lists where we only want a certain range of the string, this is known as string slicing. The only new way of accessing strings, which applies to lists too, is the last command where we used `[-1]`. This is a cool feature with Python where `[-1]` allows you to access the very last value of the string. One last feature is that to join or concatenate more than one strings. And we do this quite simply:

```python
string_three = string_one + string_two
string_two[0]
print(string_three)
string_three = string_one + " " + string_two
string_two[0]
print(string_three)
print(len(string_three))
```

We can also use the function `len()` to get the length of a string as well as seen above.

Run the code to see the output you get.

# String Filtering

How do we mine or filter certain data. Let us look at an example below:


```python
string_three = 'welcome, Python Course 101'
print(string_three)
# splits the string based on ","
print(string_three.split(","))
['welcome', ' Python Course 101']
split_string =
string_three.split(",")
print(split_string)
print(type(split_string))
```

We use the `split()` function and we specify that our criteria to split is based on a comma. Interestingly the split function outputs a list! 

Run the code to see the output you get.

# String Modifying

Here are a few examples of how we can modify strings:

```python
mystring = 'PyThoN'
# we can make all letters lower case:
print(mystring.lower())
# we can make all letters upper case:
print(mystring.upper())
# replace a string with another:
print(mystring.replace('P','Q'))
```

Run the code to see the output you get.

# Summary

This brings us to the end of the lesson. On to the next one.
