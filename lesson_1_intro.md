---
layout: default
---

* TOC
{:toc}

# Introduction

Welcome to this Python programming tutorial. In this tutorial we will be focusing on an introduction to Python programming. We assume that you have no background in Python programming so this course will cover the fundamental principles. 

Note The first few pages is a tutorial on using python for the first time.

Note this code was developed in the following environment:
- OS: Windows 10, 
- Python Version: 3.8.5
- IDE: CoCalc & Sublime 3.2.2

# What is programming?

Programming is just a process of using instructions that tells a computer how to perform a task. We use the programming language of Python to create these instructions. Other programming languages also exist like C, C++, and Java. We will be using Python as it is quite versatile, easy to use, and quick to learn.

# Python Overview

Python can be used to create pretty much any type of application, from data processing to web applications to running embedded systems. Like a Swiss Army Knife, Python may not be the best language for every specific application, but there’s a good chance it’s the second-best language for almost anything. 

## What can you do with it:

![uses1](https://user-images.githubusercontent.com/63326895/107113352-1fd67280-6867-11eb-8fad-4543693c1524.png)

## How does it compare to other programming languages (2019):

![comparison](https://user-images.githubusercontent.com/63326895/107113415-7b086500-6867-11eb-8e87-b737a42948d2.png)


# Python as a tool for data Science

Let us start with an example of data you have loaded in excel as shown below:

![image](https://user-images.githubusercontent.com/29664888/146556128-70b3602d-93f4-4d89-a054-0de85692a6c5.png)

This is quite a simple data set that has age, gender, and country for 11 people. Imagine we want to extract some useful information from this table of data. Maybe let us also get some statistics on the age column, like the minimum, maximum, average, and standard deviation metrics:

![image](https://user-images.githubusercontent.com/29664888/146557310-bc6f8f6e-88c9-443c-b6e0-f0dcfec8e062.png)

For example we only want to see people above the age of 30, who are male and are from South Africa. This is quite straight forward to do in excel by using the filter tab for example:

![image](https://user-images.githubusercontent.com/29664888/146557001-46f31b86-a0ef-4305-aa6c-10c8bc689bce.png)

Finally, let us draw a graph of age distribution:

![image](https://user-images.githubusercontent.com/29664888/146557483-5f446a0e-2e5a-424a-bd81-51629514ad94.png)

So these were simple tasks that were performed on this dataset and could be similar to what you would have to do. Now we will be using Python to do the exact same thing...and more! Python is just another tool that you can use to analyse and process your data. So you will be learning the necessary tools to be able to achieve what we did in excel.

# Let’s get started

So firstly we need to setup the Python environment we going to use to analyse this simple dataset. There are many ways to this and various applications and it is all up to your own preference. If you are use to using Matlab then using something like Spyder would seem very familiar to you:

If you want a more a involved coding environment then you can choose PyCharm:

![image](https://user-images.githubusercontent.com/29664888/146560123-911ff622-3489-4fbd-8f0d-bccfefbc65df.png)

or VS Code:

![image](https://user-images.githubusercontent.com/29664888/146560264-1be64c00-0821-4c88-938c-e288acd14f07.png)

Or can also use simple text editors like Sublime to run Python:

![image](https://user-images.githubusercontent.com/29664888/146560408-047d4730-776a-42d9-90eb-6e74ccd60f2e.png)

Or if you like using the terminal then go ahead and just install Python from it website:

![image](https://user-images.githubusercontent.com/29664888/146560506-d4ad6407-f6f0-4683-8a8f-346c7cb827b2.png)


For For the first few lessons we are going to be using a terminal using CoCal. Go to the link: https://cocalc.com/ and click on "Run CoCalc Now", then click on the "New" tab and select the "Linux terminal" option. You should then be presented with a linux terminal showing the "~$" prompt. 

In the terminal you can check what version of Python you are running with:

```
~$ 
~$ python --version
Python 3.8.10
~$ 
```

You can also use any other Linux terminal used in Windows, Linux, or MacOS. If you want to a full installation of Python on your computer follow this link: https://github.com/kode2go/python/wiki/A.1-Setup-Python-Environment

## Step 1:
Enter the following command in the Linux terminal: `python`. This will open up a Python interpreter. You will see the next line saying “Python 3.8.5 …“ which just tells us the Python version we are using. And the last line shows the `>>>` prompt which indicates that you have just started a new python environment called a Python interpreter. With these notes, make sure you only type out or copy any commands that are after the `>>>` prompt.

![image](https://user-images.githubusercontent.com/63326895/107113430-8fe4f880-6867-11eb-90cf-40f3708d5026.png)

## Step 2:
Let us start off with some simple math commands. Note the Python convention for math operations below.

| Math Operator  | Example |
| ------------- | ------------- |
| Addition  | 10 + 20 |
| Subtraction  | 10 - 20 |
| Multiplication  | 10*20  |
| Division  | 10/20  |
| Assignment | x = 5  |

Type out the following commands in the Python interpreter and press the “Enter” key and you should see the follow responses from the Python interpreter: 

``` python
>>> 
>>> 40 + 2
42
>>> print(40+2)
42
>>> name = "python"
>>> print(name)
python
>>> x = 40
>>> y = 2
>>> x
40
>>> y
2
>>> 
```

Now let us do a simple sum by entering the following:

``` python
>>> 
>>> sum = x + y
>>> print(sum)
42
>>>

```

Let us take a step back and go through what we have done so far.
First off, we did some basic math by adding two numbers. These types of numbers are also known as integers. You should have seen the answer as `42` which is an integer. We can also print or display that answer as text,  with `print(40+2)`. We also made a variable called `name` which stores the text ` “wabbit” `. Note the two exclamation marks “ ”, makes sure the variable is stored as text, again also known as a string.
We then started assigning some variables like `x = 40` and `y = 2`. We can print out what those variables represent at any time if you just enter `x` and `y`. Then we made a sum as `sum = x + y` which we then printed out on the terminal using the `print` function: `print(sum)`.

# Python Print and Input Functions

We can do many things with the `print()` function, more than we have done so far. We can print multiple lines of text using `\n` like this:

```python
>>> print("this is line 1 \n this is line 2 \n")
this is line 1
 this is line 2
>>>
```

We can also print shapes:

```python
>>> print("*****\n*****\n*****\n*****\n")
*****
*****
*****
*****

>>>
```

We have seen now a few examples of how to output variables, values and text using the `print()` function. We can also do get data input as well using the `input()` function:

```
>>> answer = input("What is the best programming language?")
What is the best programming language?Python
>>> print(answer)
Python
>>>
```

We can also get values as well but as you will learn you will need to convert the type to a number like using `int()`:

```python

>>> answer = int(input("When was python invented?"))
When was python invented?1980
>>> diff = 2022 - answer
>>> print(diff)
42
>>>
```

If we did not use `int()` we would get an error.


# Python Interpreter

Note that Python reads your code sequentially from top to bottom.
For example this works:

```python
1. >>> 
2. >>> mysum= 40 + 2
3. >>> print(mysum)
4. 42
```

Python reads each line in order from line 1 to 4. However, this will not work:
```python
1. >>>
2. >>> print(mysum)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'mysum' is not defined
3. >>>
```

Since there is no variable that was declared before called mysum. You must declare or define it before you use it.

Well done! That’s it! You have been doing basic Python programming. 

# Good Programming Habits

1. Add comments to each line of code explaining what it does. Also, any time you code a variable it is stored in memory. It is a good practice for beginners to write that out as a comment the line of code that declared the variable. 
```python
1. >>> 
2. >>> mysum= 40 + 2
3. >>> #store the sum of two values (40 and 2) in the variable called mysum, in memory mysum = 42
4. >>> print(mysum)
5. 42
6. >>> #print out the variable called mysum
```
This is more applicable for larger programs as you will see later.

# Summary

This is the end of this lesson on getting an overview of Python and how to set it up. In the next lesson we will be focusing on working through the excel data set!

# Extra Resources:

General Python Resources:
* https://www.python.org/
* https://www.w3schools.com/python/default.asp
* https://automatetheboringstuff.com/
* https://realpython.com/

Data Science:
* https://www.datacamp.com/courses/intro-to-python-for-data-science
* https://realpython.com/tutorials/data-science/
* https://towardsdatascience.com/tagged/python

Machine Learning:
* https://www.tensorflow.org/
* https://keras.io/
* https://scikit-learn.org/stable/

GUI Applications:
* https://wiki.python.org/moin/TkInter (This is where everyone starts)
* https://www.tutorialspoint.com/python/python_gui_programming.htm
* https://realpython.com/python-gui-tkinter/
* https://www.tutorialspoint.com/pyqt/pyqt_hello_world.htm

Web Development:
* https://www.djangoproject.com/
* https://flask.palletsprojects.com/en/1.1.x/

Mobile App Development
* https://kivy.org/#home

Other
* http://ode.org/ (simulating rigid body dynamics, pendulums, collision dynamics)
* https://micropython.org/ (micro-electronics, IoT)
* https://opencv.org/ (Image Processing, Computer Vision)




_yay_

[back](./)


