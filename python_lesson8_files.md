* TOC
{:toc}

# Input function

```python
print('Enter your name:')
x = input()
print('Hello, ' + x) 

>>> print("Rand to Dollar: " +  str(float(input("Enter Rand to Dollar: "))*0.068))
Enter Rand to Dollar: 100
Rand to Dollar: 6.800000000000001
>>> 
```

# Date & Time

For the date and time we need the following libraries shown in the code below. To access certain values we use list slicing.

```python
>>> from datetime import datetime
>>> from datetime import *
>>> 
>>> from time import *
>>> 
>>> print(str(datetime.now())[:])
2021-08-01 09:49:34.791152
>>> print(str(datetime.now())[10:19])
 09:49:41
```

# View PC Memory & CPU Usage:

## Overview
This is a simple program that outputs the PC memory and CPU usage and is useful for system monitoring. We will be using two libraries that is `psutil` and `time`. 
- `psutil`: _Cross-platform lib for process and system monitoring in Python._
- `time`: _Conversion of given time input into proper format._

Output:

```
PC Memory & CPU Usage

0: PC Memory: 89.3, CPU Usage: 59.7
1: PC Memory: 89.6, CPU Usage: 56.2
2: PC Memory: 89.7, CPU Usage: 54.7
3: PC Memory: 89.8, CPU Usage: 52.3
4: PC Memory: 89.8, CPU Usage: 60.8
5: PC Memory: 89.8, CPU Usage: 60.9
6: PC Memory: 89.9, CPU Usage: 64.9
7: PC Memory: 89.9, CPU Usage: 58.1
8: PC Memory: 89.9, CPU Usage: 53.1
9: PC Memory: 89.9, CPU Usage: 72.1
[Finished in 12.2s]

```

## Code

The code below shows the output described in the previous section. We are importing `psutil` and `time` first. Then we are just printing
out header information in the form of _"PC Memory & CPU Usage"_. Then we create a `for` loop that runs 10 times using the `range` function.
In the `for` loop we use the `psutil` libraries and use two of its methods: `psutil.virtual_memory()` and `psutil.cpu_percent(interval=1)` to store the instance of those values and then print them out. The method `time.sleep(0.1)` is just used to add 100ms delay in the `for` loop. 

```python
import psutil
import time

print("PC Memory & CPU Usage\n")

for i in range(10):
	mem = psutil.virtual_memory()
	
	usage = psutil.cpu_percent(interval=1)
	print(str(i) + ": PC Memory: "+str(mem[2]) + ", CPU Usage: " +str(usage))

	time.sleep(0.1)
```

# Read Excel file

country.xlsx

```
Country,Continent
Afghanistan,Asia
Albania,Europe
Algeria,Africa
Andorra,Europe
Angola,Africa
Argentina,South America
Armenia,Asia
```

```python
>>> import openpyxl
>>> wb = openpyxl.load_workbook('country.xlsx')
>>> wb.sheetnames # The workbook's sheets' names.
['Sheet1', 'Sheet2', 'Sheet3']
>>> sheet = wb['Sheet1'] # Get a sheet from the workbook.
>>> sheet
<Worksheet "Sheet1">
>>> type(sheet)
<class 'openpyxl.worksheet.worksheet.Worksheet'>
>>> sheet.title # Get the sheet's title as a string.
'Sheet1'
>>> sheet['A1'].value # Get the value from the cell.
Country
>>> sheet.cell(row=1, column=1).value
Country

>>> for i in range(1, 3, 1): # Go through every other row:
...     print(i, sheet.cell(row=i, column=1).value)
1 Country
2 Afghanistan
3 Albania
>>> sheet['A1'] = 'South Africa' # Edit the cell's value.
>>> sheet['A1'].value # Get the value from the cell.
South Africa
```

# Read CSV file

country.csv

```
Country,Continent
Afghanistan,Asia
Albania,Europe
Algeria,Africa
Andorra,Europe
Angola,Africa
Argentina,South America
Armenia,Asia
```

```python
with open('country.csv') as csvfile:
 reader = csv.DictReader(csvfile)
 for row in reader:
  p = Country(country=row['Country'], continent=row['Continent'])
  p.save()
```

# Read PDF File with Tables

```python
import tabula

file = "data.pdf"
file2 = "data3.pdf"

table1 = tabula.read_pdf(file,pages=1)
table2 = tabula.read_pdf(file,pages=2)

print(table1[0])
print(type(table2[0]))

# Has multiple tables

tables = tabula.read_pdf(file2,pages=1,multiple_tables=True)

print(tables[0])

print(tables[1])
```
