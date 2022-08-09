* TOC
{:toc}

# Lists

![image](https://user-images.githubusercontent.com/29664888/146557310-bc6f8f6e-88c9-443c-b6e0-f0dcfec8e062.png)

For now, we will be focusing on more features regarding the list data type as it will teach you the most important principles about storing multiple variables. A few more built in functions of lists are shown below. The first being `count` which count how many times that value is in the list: 

```python
>>> age.count(49)
1
>>> age.count(2)
0
>>> age.count(30)
2
>>>
3

```

Then we can reverse the items in a list, copy a list, and add lists together as shown below:

```python
>>> age.reverse()
>>> age
[39, 25, 29, 46, 22, 35, 22, 49, 30, 40, 30]
>>> age.reverse()
>>> age
[30, 40, 30, 49, 22, 35, 22, 46, 29, 25, 39]
>>> age_new = age.copy()
>>> age_new
[30, 40, 30, 49, 22, 35, 22, 46, 29, 25, 39]
>>> age_new.clear()
>>> age_new
[]
>>> age_new = age.copy()
>>> add_list = age + age_new
>>> add_list
[30, 40, 30, 49, 22, 35, 22, 46, 29, 25, 39, 30, 40, 30, 49, 22, 35, 22, 46, 29, 25, 39]
>>>
```

Lastly, we can also sort values in a list
```python
>>> age.sort()
>>> age
[22, 22, 25, 29, 30, 30, 35, 39, 40, 46, 49]
>>>
>>> age.sort(reverse=True)
>>> age
[49, 46, 40, 39, 35, 30, 30, 29, 25, 22, 22]
>>>
>>> def lenSort(item):
...  return len(item)
...
>>> country.sort(key=lenSort)
>>> country
['Kenya', 'Kenya', 'Kenya', 'Egypt', 'Sudan', 'Lesotho', 'Botswana', 'Mozambique', 'South Africa', 'South Africa', 'South Africa']
>>> country.sort(key=lenSort,reverse=True)
>>> country
['South Africa', 'South Africa', 'South Africa', 'Mozambique', 'Botswana', 'Lesotho', 'Kenya', 'Kenya', 'Kenya', 'Egypt', 'Sudan']
>>>
```

A list can also contain all kinds of data types:
```python
>>> my_list = [42, -2021, 6.283, "tau", "python"]
>>> print(my_list )
[42, -2021, 6.283, 'tau', 'python']
>>> 

```

Now we can access any item in this list based on their index. The first index is “[0]“ and the second is “[1]“ etc, as shown below:
```python
>>> my_list = [42, -2021, 6.283, "tau", "python"]
>>> print(my_list)
[42, -2021, 6.283, 'tau', 'python']
>>> 
>>> 
>>> print(my_list[0])
42
>>> print(my_list[1])
-2021
>>> print(my_list[5])
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
IndexError: list index out of range
>>> print(my_list[4])
python
```


So we saw here that we can access and thus print the first value of the list by accessing its index at “[0]“. You will see that I got an error with “my_list[5]“. This is because we do have 5 items in the list but since we start with the first value being “index[0]“, the last one will be “index[4]“ as shown.
We can also print all the items in the list using “[:]“, we can add items using “append()“, remove an item from the list using the “remove()“ function, and we can also check how many variables are in the list using the “len()“ tool as shown below:

```python
>>> my_list= [42, -2021, 6.283, "tau", "python"]
>>> 
>>> print(my_list[:])
[42, -2021, 6.283, 'tau', 'python']
>>> 
>>> my_list.append("pi")
42, -2021, 6.283, 'tau', 'python', 'pi']
>>> my_list.remove("pi")
>>> my_list.remove("tau")
>>> print(my_list)
[42, -2021, 6.283, 'python']
>>> 
>>> print(len(my_list))
4
>>> my_list.insert(1,"new1") 
```

Furthermore, you can view a certain range of items as well:
```python
>>> print(my_list[0:3])
[42, -2021, 6.283]
```

Another way of add elements is to insert it directly into a list:
```python
>>> my_list.insert(1,"new1") 
```
This is known as list slicing.
We can do a lot of cool things with lists like sorting, joining, and one of the coolest features of Python lists is - list comprehension. Please note, like with any tool, this data type has its limitations. You will learn over time to use the best data type for the right task. 

## Grouping Lists

```python
>>> group_lists = [age,gender,country]
>>> group_lists
[[30, 40, 30, 49, 22, 35, 22, 46, 29, 25, 39], ['M', 'M', 'F', 'M', 'F', 'F', 'F', 'M', 'M', 'F', 'M'], ['South Africa', 'Botswana', 'South Africa', 'South Africa', 'Kenya', 'Mozambique', 'Lesotho', 'Kenya', 'Kenya', 'Egypt', 'Sudan']]
>>> group_lists[0]
[30, 40, 30, 49, 22, 35, 22, 46, 29, 25, 39]
>>> group_lists[1]
['M', 'M', 'F', 'M', 'F', 'F', 'F', 'M', 'M', 'F', 'M']
>>> group_lists[2]
['South Africa', 'Botswana', 'South Africa', 'South Africa', 'Kenya', 'Mozambique', 'Lesotho', 'Kenya', 'Kenya', 'Egypt', 'Sudan']
>>> group_lists[0][0]
30
>>> group_lists[0][1]
40
>>> group_lists[1][0]
'M'
>>> group_lists[1][:]
['M', 'M', 'F', 'M', 'F', 'F', 'F', 'M', 'M', 'F', 'M']
>>>
```


Group lists with print function
```python
>>> listDetails = [
... ['name','job','DOB'],
... ['john','jack','jone'],
... ['doctor','engineer','CA'],
... [1973,1984,2000]
... ]
>>>
>>> print("My list:" + str(listDetails[0]))
My list:['name', 'job', 'DOB']
>>> print("My list:" + str(listDetails[0][1]))
My list:job
>>> print("My list:" + str(listDetails[1]))
My list:['john', 'jack', 'jone']
>>> print("My list:" + str(listDetails[1][:]))
My list:['john', 'jack', 'jone']
>>> print("My list:" + str(listDetails[2]))
My list:['doctor', 'engineer', 'CA']
>>> print("My list:" + str(listDetails[3]))
My list:[1973, 1984, 2000]
>>>
>>> listDetails[3].sort(reverse=True)
>>> print("My list:" + str(listDetails[3]))
My list:[2000, 1984, 1973]
>>>
>>> listDetails[0].sort(key=str.lower)
>>> print("My list:" + str(listDetails[0]))
My list:['DOB', 'job', 'name']
>>>
>>> print(dir(listDetails))
['__add__', '__class__', '__contains__', '__delattr__', '__delitem__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__gt__', '__hash__', '__iadd__', '__imul__', '__init__', '__init_subclass__', '__iter__', '__le__', '__len__', '__lt__', '__mul__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__reversed__', '__rmul__', '__setattr__', '__setitem__', '__sizeof__', '__str__', '__subclasshook__', 'append', 'clear', 'copy', 'count', 'extend', 'index', 'insert', 'pop', 'remove', 'reverse', 'sort']
>>>

```

# Dictionaries
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
