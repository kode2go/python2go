* TOC
{:toc}

# Reading and Writing Files

File handling is one of the useful features of Python programming. To be able to read, edit, and create files are just some of the features that are available. Let us first start off with reading files using a Linux terminal. If you are using Windows, then just use the normal file creation method.
In CoCalc, let us first create a file with some text in it in the Linux terminal:
```python
~$ touch myfile.txt
~$ nano myfile.txt 
~$ cat myfile.txt 
Learning Python
Welcome!
~$ 
```
Now let us read and print the contents of the file in the Python interpreter:
```python
~$ python
Python 3.8.5 (default, Jul 28 2020, 12:59:40) 
[GCC 9.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> f = open("myfile.txt","r")
>>> print(f.read())
Learning Python
Welcome!
>>> 
>>> f.close()
```


We used the “open()” function to open the file “myfile.txt” in order to read it using “r”. Then we used the “read()” function to read all its contents. 
Now let us try that again but only read one line at a time:
```python
>>> f = open("myfile.txt","r")
>>> print(f.readline())
Learning Python

>>> print(f.readline())
Welcome!
>>> 
>>> f.close()
```





But we know now that any repetitive task should be automated! We can use a “for” loop to print all the lines one-by-one:

```python
>>> f = open("myfile.txt","r")
>>> for line in f:
...  print(line)
... 
Learning Python

Welcome!

>>> 
>>> f.close()
>>> 
```

Now let us write to a file. We have two options. Either we can append the text to the file or overwrite the entire file. In the “open()” function the letter “a” stands for append and the letter “w” stands for overwrite:
```python
>>> f = open("myfile.txt","a")
>>> f.write("A new line of text")
18
>>> f.close()
>>> 
>>> f = open("myfile.txt","r")
>>> print(f.read())
Learning Python
Welcome!
A new line of text
>>> 
```

# Directory Navigation:

```python
import os
# Get current working directory
os.getcwd()
# Set path of new directory here
path =  "C:\\...."
# changes the directory 
os.chdir(path) 
# list items in directory
os.listdir('.')
# make a directory:
os.mkdir('tempDir')

```

Lastly to delete a file or folder we need to import a very handy module called “os”and use one of its pre-defined functions. Let us first create a random file and folder in the Linux terminal:
```python
~$ 
~$ ls
 2021-02-03-165527.term  'Welcome to CoCalc.ipynb'
~$ 
~$ touch myfile.txt
~$ mkdir myfolder
~$ ls
 2021-02-03-165527.term  'Welcome to CoCalc.ipynb'   myfile.txt   myfolder
~$ 
```

Now in the Python interpreter let us see if we can first see this file and folder using the function “os.listdir()”:

```python
~$ python
Python 3.8.5 (default, Jul 28 2020, 12:59:40) 
[GCC 9.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import os
>>> os.listdir('/home/user')
['.local', '.ssh', '.bash_history', '.config', '.sage', '.jupyter-blobs-v0.db', 'myfile.txt', '.gitexcludes', '.gitconfig', 'myfolder', '2021-02-03-165527.term', '.Welcome to CoCalc.ipynb.sage-jupyter2', '.bash_profile', '.python_history', '.snapshots', 'Welcome to CoCalc.ipynb', '.2021-02-03-165527.term-0.term', '.smc', '.bashrc']
>>> 
```

Now we can delete these files:

```python
>>> os.remove("myfile.txt")
>>> os.rmdir("myfolder")
>>> 
>>> os.listdir('.')
['.local', '.ssh', '.bash_history', '.config', '.sage', '.jupyter-blobs-v0.db', '.gitexcludes', '.gitconfig', '2021-02-03-165527.term', '.Welcome to CoCalc.ipynb.sage-jupyter2', '.bash_profile', '.python_history', '.snapshots', 'Welcome to CoCalc.ipynb', '.2021-02-03-165527.term-0.term', '.smc', '.bashrc']
>>> 
>>> 
~$ ls
 2021-02-03-165527.term  'Welcome to CoCalc.ipynb'
~$ 
```

An different way of doing this is using a module called `tkinter` as shown in the code below:

```python
import os
import tkinter as tk
from tkinter import filedialog

file_dir = tk.filedialog.askopenfilename(title='Select text file')
print(file_dir)

with open(file_dir, 'r') as Text_file:
    for line in Text_file:
        print(line)
        fields = line.strip().split()
        print(fields)

Text_file.close()
head, tail = os.path.split(str(file_dir))
print("start of filename: " + head + " end of filename: " + tail)
```

Another way is to use `shutil` (or shell utilities) module. It has functions to let you copy, move, rename, and delete files in your Python programs. To use the shutil functions, you will first need to use `import shutil`.

```python
   >>> import shutil, os
   >>> from pathlib import Path
   >>> p = Path.home()
   >>> shutil.copy(p / 'spam.txt', p / 'some_folder')
   'C:\\Users\\Al\\some_folder\\spam.txt'
   >>> shutil.copy(p / 'eggs.txt', p / 'some_folder/eggs2.txt')
   WindowsPath('C:/Users/Al/some_folder/eggs2.txt')
```
