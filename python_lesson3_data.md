* TOC
{:toc}

# Data Storage With Lists

Lists have many features. We will be covering some of them in this lesson. 

A list can also contain all kinds of data types:

<iframe src="https://trinket.io/embed/python3/51e9ca3fc4" width="100%" height="356" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

We can do many things with lists:
- print all the items in the `list` using `[:]`
- we can add items to the end of the `list` using `append()`
- add items at specific positions using `insert()`
- remove an item from the `list` using the `remove()` function
- check how many variables are in the `list` using the len()
- print a range of values using `[start:end]` – just like in excel! 

![image](https://user-images.githubusercontent.com/29664888/183845999-98b7e384-8aef-4803-bf2f-e07256474a0e.png)

Let us see some examples of this. Run the code below:

<iframe src="https://trinket.io/embed/python3/c9daf01a5f" width="100%" height="356" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

When we are getting only a certain range of values from a list we call this list slicing.
We can do a lot of cool things with lists like sorting, and joining. Please note, like with any tool, this data type has its
limitations. You will learn over time to use the best data type for the right task.

## Storing Data Into Lists From Excel

Now we will be continuing with the excel dataset that we used in the previous lessons: 

![image](https://user-images.githubusercontent.com/29664888/146557310-bc6f8f6e-88c9-443c-b6e0-f0dcfec8e062.png)

For now, we will be focusing on more features regarding the list data type as it will teach you the most important principles about storing multiple variables. A few more built in functions of lists are shown below. The first being `count` which count how many times that value is in the list: 

<iframe src="https://trinket.io/embed/python3/59e8303696" width="100%" height="356" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

> Exercise: Using the `count` function check how many times the number 22 is in the age list

We can also reverse the items in a list, copy a list, and add lists together as shown below:


<iframe src="https://trinket.io/embed/python3/b618adee97" width="100%" height="356" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

Lastly, we can also sort values in a list

<iframe src="https://trinket.io/embed/python3/9e9a7fbb6c" width="100%" height="356" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

## Grouping Lists

As I mentioned before a list can contain various kinds of types, even a list itself. What you see below is we are storing the lists `age`, `gender`, and `country` inside `group_lists`:


<iframe src="https://trinket.io/embed/python3/25dc43eae4" width="100%" height="356" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

> Exercise: From the variable `group_lists` display the last value in the third list.

# Data Storage With Dictionaries

A more involved data type is called a dictionary which we will only briefly cover. It has more features than a list and is especially useful for data science. For example, try out the following:

![image](https://user-images.githubusercontent.com/29664888/146557310-bc6f8f6e-88c9-443c-b6e0-f0dcfec8e062.png)

We can either type it out or just use the lists we generated earlier and put it in our dictionary:

```python
>>> dataset = {'age': age,'gender': gender,'country':country}
>>> dataset
{'age': [30, 40, 30, 49, 22, 35, 22, 46, 29, 25, 39], 'gender': ['M', 'M', 'F', 'M', 'F', 'F', 'F', 'M', 'M', 'F', 'M'], 'country': ['South Africa', 'Botswana', 'South Africa', 'South Africa', 'Kenya', 'Mozambique', 'Lesotho', 'Kenya', 'Kenya', 'Egypt', 'Sudan']}
>>> dataset['age']
[30, 40, 30, 49, 22, 35, 22, 46, 29, 25, 39]
>>> dataset['age'][0]
30
>>>>>>
>>> dataset['age'][0] = 50
>>> dataset['age'][0]
50
>>> print(dir(dataset))
['__class__', '__contains__', '__delattr__', '__delitem__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__iter__', '__le__', '__len__', '__lt__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__setattr__', '__setitem__', '__sizeof__', '__str__', '__subclasshook__', 'clear', 'copy', 'fromkeys', 'get', 'items', 'keys', 'pop', 'popitem', 'setdefault', 'update', 'values']
>>> dataset.keys()
dict_keys(['age', 'gender', 'country'])
>>> dataset.values()
dict_values([[30, 40, 30, 49, 22, 35, 22, 46, 29, 25, 39], ['M', 'M', 'F', 'M', 'F', 'F', 'F', 'M', 'M', 'F', 'M'], ['South Africa', 'Botswana', 'South Africa', 'South Africa', 'Kenya', 'Mozambique', 'Lesotho', 'Kenya', 'Kenya', 'Egypt', 'Sudan']])
>>> 50 in dataset
False
>>> 50 in dataset['age']
False
>>> 30 in dataset['age']
True
>>> dataset.pop('age')
[30, 40, 30, 49, 22, 35, 22, 46, 29, 25, 39]
>>> dataset
{'gender': ['M', 'M', 'F', 'M', 'F', 'F', 'F', 'M', 'M', 'F', 'M'], 'country': ['South Africa', 'Botswana', 'South Africa', 'South Africa', 'Kenya', 'Mozambique', 'Lesotho', 'Kenya', 'Kenya', 'Egypt', 'Sudan']}
>>> dataset['newage'] = age
>>> dataset
{'gender': ['M', 'M', 'F', 'M', 'F', 'F', 'F', 'M', 'M', 'F', 'M'], 'country': ['South Africa', 'Botswana', 'South Africa', 'South Africa', 'Kenya', 'Mozambique', 'Lesotho', 'Kenya', 'Kenya', 'Egypt', 'Sudan'], 'newage': [30, 40, 30, 49, 22, 35, 22, 46, 29, 25, 39]}
>>>
```

This assigns a dictionary to the dataset variable. This dictionary’s keys are 'age', 'gender', and 'country'. The values for these keys are several as you can see. You can access these values or keys as shown. Note, you can also created nested dictionaries. We instead of creating lists within the dictionary we could have created them as dictionaries. Note, we can also put dictionaries in lists as well!

## Dictionaries vs. Lists

Dictionary keys are unique

Unlike lists, items in dictionaries are unordered. The first item in a list named spam would be spam[0]. But there is no “first” item in a dictionary. While the order of items matters for determining whether two lists are the same, it does not matter in what order the key-value pairs are typed in a dictionary. Enter the following into the interactive shell:

As you model more complicated things, you may find you need dictionaries and lists that contain other dictionaries and lists. Lists are useful to contain an ordered series of values, and dictionaries are useful for associating keys with values.

Because dictionaries are not ordered, they can’t be sliced like lists.
Though dictionaries are not ordered, the fact that you can have arbitrary values for the keys allows you to organize your data in powerful ways. 

## Extra

Look at frequency of numbers in a list without knowing the numbers - loop

dir(mylist) very useful


>>> import builtins
>>> dir(builtins)


import types

builtin_function_names = [name for name, obj in vars(builtins).items() 
                          if isinstance(obj, types.BuiltinFunctionType)]
