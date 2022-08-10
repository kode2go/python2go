* TOC
{:toc}

# Variables

In the previous we lesson we did a few examples with variables. We learnt about two types of variables which is an integer and a string. And integer or `int` refers to whole numbers that are either positive or negative for example 5, 2021, or -256. A string refers to any text. That can be a single character, word, or groups of words.

There is one more type that we will use often which is a float or a variable number that has decimals. The `float` or floating point number is any decimal number like 0.5, -34.56, and 3.1451245. 

We can determine what types of variables we have using the built-in `type()` function. Let us first check what type of variable x is by running the file below:

<iframe src="https://trinket.io/embed/python3/263d9d4024" width="100%" height="356" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

You get back `<class 'int'>` which tells us this variable is an integer, `<class 'float'>` for the number that has decimals and then `<class 'str'>` for the variables that had text.

# Changing Between Variable Data Types

Many types you would want to change the data type. For example if you are reading in data from an excel, csv, or text file it a number may be stored as text. So we can convert that to an integer or float if we want to do some calculations or statistics with it. We do that using the built-in Python functions:

- `int()` converts to an intger
- `float()` converts to a float
- `str()` converts to a string 

This conversion process is called casting. Let us look at an example below:

<iframe src="https://trinket.io/embed/python3/2bd71b33e7" width="100%" height="356" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

One useful feature of casting is when you want to use numbers with the `print` function. Usually, the `print` functions converts everything inside the brackets to a string. However, if you want output some text with an integer variable you will need to use the `F-format` feature. If you use the `f` letter inside the `print` function you can use variable numbers with text where the variables are inside curly brackets `{}`. Run the example below:

<iframe src="https://trinket.io/embed/python3/832a501a2a" width="100%" height="356" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

# The Excel Dataset

Now let us look at our excel dataset again:

![image](https://user-images.githubusercontent.com/29664888/146556128-70b3602d-93f4-4d89-a054-0de85692a6c5.png)

The first thing we wanted to do was get some statistics on the age column, like the minimum, maximum, average, and standard deviation metrics.

Now there are two ways of doing this. The better approach is just to import this excel file into Python and then find the metrics. The second way and longer way is to input the data ourselves. We will be doing the latter in order to understand the Python principles of variables and data types. 

Just like in excel where we are storing numbers in cells we can also store numbers in Python as variables. So for example we have at cell B2 is equal to 30, cell B3 is equal to 40, and so on. Run the code below:


<iframe src="https://trinket.io/embed/python3/48fd30238b" width="100%" height="356" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

Try storing the rest of the variables that we got from the excel dataset in column B and print them out too.

Now to store each value in a separate variable is a tedious process especially if we want to get some statistics from it. So let us rather use a variable that can store multiple values. There are many of these in Python, for now we are going to use one called a `list`. And a `list` is defined by square `[]` brackets with the values inside the square brackets separated by commas. We can also give a `list` a unique name. Let us call it `age` to match the excel column B dataset and do it as follows:

<iframe src="https://trinket.io/embed/python3/4e75b484fa" width="100%" height="356" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

This looks a lot better. We can store all those values of age in a `list` data type called `age`:

```python
age = [30,40,30,49,22,35,22,46,29,25,39]
```

Take note that to access any of the values all we need to do is use `age[index]`. Where `index` refers to the location in the `list` datatype. Note, the first value is stored at index 0 not 1. The second value is stored at index 1 and so on. The last value is stored at index 10:

![image](https://user-images.githubusercontent.com/29664888/183818288-4c43ae67-47f8-462f-b11e-d6683acbd41c.png)

If you try to access the index at 11 you will get the error `list index out of range`. See the excel data set again and look at column A called `index` to see how the values are stored. 

Now we use some built in Python functions to get the same statistics we got in excel as shown below. Run the code below:


<iframe src="https://trinket.io/embed/python3/59f4ac2759" width="100%" height="356" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

So the cool thing is we can use the built in functions `min`, `max`, `len`, and `sum` to get the minimum and maximum number, the length of the list, and the sum of all the numbers. Thereafter, we can easily get the average. We will look at more of a manual approach later instead of using these functions. However, you will need to learn a little more do that. We will look at getting standard deviation a little later as well.

Let us now record all the information in other columns in lists too. So in the excel data set we have column C that holds Gender values for M (male) and F (female). Like before we can store the variables individually based on the cells. Run the code below:


<iframe src="https://trinket.io/embed/python3/27e4b9f970" width="100%" height="356" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>


But wait! Its giving us an error `name 'M' is not defined` Why is that? Any letters, words, group of words fall under the category of a `string` data type. Therefore we need to add `"` to the beginning and end. Run the code below:


<iframe src="https://trinket.io/embed/python3/dcae186896" width="100%" height="356" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>


Again this is a tedious task so let us create a `list` for gender:

```python
gender = ["M","M","F","M","F","F","F","M","M","F","M"]
```

Run the code below:


<iframe src="https://trinket.io/embed/python3/8cc9438d33" width="100%" height="356" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>


This is the same as before. we can access individual values starting with index = 0 for the first value. A nice feature of Python is that you can access the last value in the list by setting the index = -1.

Lastly, we can do the same for the country column and just make a `list`. Note, country values are strings as its words or groups of words:

```python
country = ["South Africa","Botswana","South Africa","South Africa","Kenya","Mozambique","Lesotho","Kenya","Kenya","Egypt","Sudan"]
```

Run the code below:

<iframe src="https://trinket.io/embed/python3/9b983558e4" width="100%" height="356" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>


# Summary

This brings us to the end of the second lesson where we covered variables and data types. In the next lesson we will be lists and dictionaries.



