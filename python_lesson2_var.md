* TOC
{:toc}

# Variables

In the previous we lesson we did a few examples with variables. For example: 

``` python
~$ python
Python 3.8.5 (default, Jul 28 2020, 12:59:40) 
[GCC 9.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 
>>> 
>>> x = 40
>>> y = 2
>>> name = "python"
>>> sum = x + y
>>> sum
42
>>> print(sum)
42

```



We learnt about two types of variables which is an integer and a string. 

Now let us look at our excel dataset again:

![image](https://user-images.githubusercontent.com/29664888/146556128-70b3602d-93f4-4d89-a054-0de85692a6c5.png)

The first thing we wanted to do was get some statistics on the age column, like the minimum, maximum, average, and standard deviation metrics.

Now there are two ways of doing this. The better approach is just to import this excel file into Python and then find the metrics. The second way and longer way is to input the data ourselves. We will be doing the latter in order to understand the Python principles of variables and data types. 

Just like in excel where we are storing numbers in cells we can also store numbers in Python as variables. So for example we have at cell B2 is equal to 30, cell B3 is equal to 40, and so on. We can do the same in Python:

```python
>>>
>>> B1 = 30
>>> B2 = 40
>>> B3 = 30
>>> B4 = 49
>>> B1
30
>>> print(B2)
40
>>>
```

But this is a bit tedious to define a new variable for each new variable especially if we want to get some statistics from it. So let us rather use a variable that can store multiple values. There are many of these in Python, for now we are going to use one called a `list`. And a list is defined by [] brackets with the values inside the square brackets. We can also give a `list` a unique name. Let us call it `age` to match the excel dataset and do it as follows:

```python
>>> age = [30,40,30,49,22,35,22,46,29,25,39]
>>> print(age)
[30, 40, 30, 49, 22, 35, 22, 46, 29, 25, 39]
>>> age[0]
30
>>> age[1]
40
>>> age[10]
39
>>> age[11]
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
IndexError: list index out of range
>>>
```

This looks a lot better. We can store all those values of age in a `list` data type called `age`. Take note that to access any of the values all we need to do is use `age[index]`. Where `index` refers to the location in the `list` datatype. Note, the first value is stored at index 0 not 1. The second value is stored at index 1 and so on. The last value is stored at index 10. If you try to access the index at 11 you will get the error `list index out of range`. See the excel data set again and look at column A called `index` to see how the values are stored. 

Now we use some built in Python functions to get the same statistics we got in excel as shown below:

```python
>>> min(age)
22
>>> max(age)
49
>>> len(age)
11
>>> sum(age)
367
>>> average = sum(age)/len(age)
>>> average
33.36363636363637
>>>

```

So the cool thing is we can use the built in functions `min`, `max`, `len`, and `sum` to get the minimum and maximum number, the length of the list, and the sum of all the numbers. Thereafter, we can easily get the average. We will look at more of a manual approach later instead of using these functions. However, you will need to learn a little more do that. We will look at getting standard deviation a little later as well.

Let us now record all the information in other columns in lists too. So in the excel data set we have column C that holds Gender values for M (male) and F (female). Like before we can store the variables individually based on the cells:

```python
>>>
>>> C2 = M
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'M' is not defined
>>> C3 = M
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'M' is not defined
>>> C4 = F
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'F' is not defined
>>>
```

But wait! Its giving us errors. Why is that? Any letters, words, group of words fall under the category of a `string` data type. Therefore we need to add `"` to the beginning and end like so:

```python
>>> C2 = "M"
>>> C3 = "M"
>>> C4 = "F"
>>> C2
'M'
>>> C3
'M'
>>> C4
'F'
>>>
```

Again this is a tedious task so let us create a list for gender:

```python
>>> gender = ["M","M","F","M","F","F","F","M","M","F","M"]
>>> gender[0]
'M'
>>> gender[-1]
'M'
>>>
```

Same as before we can access individual values starting with index = 0 for the first value. A nice feature of Python is that you can access the last value in the list by setting the index = -1.

Lastly, we can do the same for country column and just make a list. Note, country is string as its words or groups of words:

```python
>>> country = ["South Africa","Botswana","South Africa","South Africa","Kenya","Mozambique","Lesotho","Kenya","Kenya","Egypt","Sudan"]
>>> country
['South Africa', 'Botswana', 'South Africa', 'South Africa', 'Kenya', 'Mozambique', 'Lesotho', 'Kenya', 'Kenya', 'Egypt', 'Sudan']
>>> country[0]
'South Africa'
>>> country[5]
'Mozambique'
>>>
```
## Different Data Types

We always need to understand what kind of data do we want to store. Well in previous example we know we are dealing with age which is a number. Python distinguishes between to types of numbers. The first first is called an `int` or integer which is any non-decimal number like 5, 2021, or -256. The other data type is called a `float` or floating point number which is any decimal number like 0.5, -34.56, and 3.1451245. You saw when we worked out the average for `age` we got a number with decimals which means Python will store it as a `float`.

In Python we don’t need to declare variable types, like in most other programming languages. They can change their type as well through casting. Let us first check what type of variable `x` is by entering the following: 

``` python
>>> print(type(x))
<class 'int'>
>>>

```
You get back `<class ‘int’>` which tells us this variable is an integer. Let us now change that variable to a float by entering the following:

``` python
>>> x = 40.2
>>> print(type(x))
<class 'float'>
>>> 
```

Now the type of the variable has changed to a float. 

Another piece of information you should take note of is that with strings the text that you want to store in a variable should be enclosed by either a single or double quote. 
If we want to print string variables using the `print()` function it would look like this:

``` python
>>> course = "Python was creating in the 1980s"
>>> 
>>> print("When was Python created?  " + course)
When was Python created? Python was creating in the 1980s
>>> 
```

You can do the same with numbers:
``` python
>>> 
>>> year_created = 1980
>>> 
>>> print("Year created is in: " + year_created )
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: can only concatenate str (not "int") to str
>>> 

```

Oh no, it seems we ran into an error! It is telling us that `year_created` is of type `int` or integer and it needs to be a type `str` or string. So now all we need to do is cast the variable into a string as shown:

``` python
>>> print("Year created is in: " + str(year_created))
Year created is in: 1980
>>> 
```

If we want to cast to an integer we use `int()`, for a float we use `float()` and for a string we use `str()`. 
The one last data type is a Boolean type. This type of variables holds either a True or False value.

As we saw in the previous section, you can change the type of a variable, by using type casting. That is, we can make a string into an integer and an integer into a string! Using the functions `int()`, `float()`, and `str()`.
For example, enter the following:
 
``` python
>>> 
>>> x = int(42)
>>> x
42
>>> y = str(42)
>>> y
'42'
>>> z = float(42)
>>> z
42.0
>>> a = int(42.0)
>>> a
42
>>> print(type(y))
<class 'str'>
>>>
```

Now when we made `y = str(42)`  we took an integer type and made it into a string type. You can see this when we said `print(type(y))`. 

# Global vs Local Variables
Variables have scope, that means they can be accessed globally or locally. Globally means the variables can be accessed anywhere in the code. Locally means it can only be accessed in certain parts of your code, for example in a function, loop or condition. Here is an example below.

```python
total = 0; # This is global variable.
# Function definition is here
def sum( arg1, arg2 ):
   # Add both the parameters and return them."
   total = arg1 + arg2; # Here total is local variable.
   print "Inside the function local total : ", total
   return total;
# Now you can call sum function
sum( 10, 20 );
print "Outside the function global total : ", total
```

We will go into functions more later.

# Summary

This brings us to the end of the second lesson where we covered variables and data types. In the next lesson we will be lists and dictionaries.



