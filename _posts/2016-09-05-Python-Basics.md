---
layout: post
title: "Python Basics"
date: 2016-09-5
---


- no comma or semi-comma at the end of each line of code!
- This course focus on Python 3.x.
- ';' is to place 2 commands on the same line
- 




### comments
use #

### print results and calculations

```sh
print(100*(1.1**7)-5)
```

### variables and types

types decide the operations' action

```sh
3 + 4
"ab" + "cd"
"a"* 4
```

#### strings

-  "" and '' can both be used in strings

```sh
input_1 = raw_input('test_to_show_: ') % input is string
len()
```

loop through a string, don't need to set an index and increase it every time by 1

```sh
for letter in str_1: 
    print letter
```

count the number of some letter

```sh
for letter in str_1:
    if letter == "o":
        count = count + 1
```

logical operation, return true/ false :

```sh
'a' in str_name
```

find specific letter in string
find specific letter after position 1 (parsing text)

```sh
position_1 = str_1.find("na")
position_2 = str_1.find("str_2", position_1) 
```

replace all the str_1 with str_2 in the string:

```sh
str.replace("str_1","str_2")
```

what functions can this string embed
```sh
dir(str_name)
```

stripping whitespace;

```sh
str_1.lstrip()
str_1.rstrip()
str_1.strip()
```

judge whether the first word in string is sth:

```sh
str_1.startswith("str")
```


- Basic types in Python: int, float, str, bool, 
- Compounded types: list,
- Conversion of types: the following commands change other types of variables into the type of the name of the commands.

```sh
str()
int()
float()
bool()
```

```sh
print(type(vari_name))
```

### Lists

- Different types of variables can be in one list. separated by ','
- A list can contain lists as well

```sh
list_1 = [a, b, "hi", 1, True]
[[1, 2, 3], [4, 5, 7]]
house = [["hallway", hall],
         ["kitchen", kit],
         ["living room", liv],
         ["bedroom",  bed],
         ["bathroom", bath]]
```

Subletting lists
- use the brackets [].
- Index starts from 0.
- Negative index: from back to front, starts from -1. The last one is -1, and so on

slicing and dicing

- [start: end], end index is not included in the output


```sh
list_1[0]
list_1[-1]
list_1[1:2]
list_1[:4]
list_1[5:]
subset_list_result = list_1[1] + list_1[2]
list_1[2][-1]
list_1[-1][1]
```

Tips:

```sh
the first m elements: list_1[:m]
the last n elements: list_1[-n:]
```

#### Notice: 

The list names are actually pointers!!! The first line below actually are 2 same pointers; while the second line below makes sure that two lists will not effect each other!

```sh
list_2_copy = list_2
list_2_copy = list_2[:]
```


Manipulating Lists:
- replace the elements 
- add and remove elements


```sh
replace: list_1[i] = 2
add: list_extended = list_1 + ["hi", 5]
remove: del(list_1[-4])
```

### Functions and Packages

show the documentation of a function: 

```sh
help(func_name)
?func_name
?func_name()
```

```sh
length of a list/string: len(var_name)
```

### Methods: functions that depending on types

you can use help() to find all the methods of a certain type/function

list methods:

```sh
not change the list:
list_name.index(some_element)
list_name.count(some_element)
change the list:
list_name.append(appended_element) % append one element each time
list_name.remove()
list_name.reverse()
```

String methods

```sh
string_name.capitalize()
string_name.replace()
string_name.upper()
```

### Packages

- packages need to be installed before use. use pip
- 
Useful packages for data science:
- Numpy
- Matplotlib
- Scikit-learn

import package

```sh
import numpy % import the entire package
import numpy as np % rename to make it easier
selective import:
from numpy import array % import function, if so, no need to specify which array() use are using from, so no need to use numpy.array()
from ... import ... as ...
```

### Numpy

- element-wise calculations
- arrays: contain only one type
- can use [] to get the elements

```sh
list(list>23) % only elements larger than 23 was kept
np_array_name = np.array(list_name) % convert list to array
np_2d[][] == np_2d[ , ]
np_2d.shape
np.mean()
np.median()
np.std()
mp.corrcoef(first, second)
sum(), sort(),...
np.random.normal() % generate random numbers
```

### Data visualization: Matplotlib

 Line plot:

```sh
import package.subpackage as local_name
import matplotlib.pyplot as plt
plt.plot(x,y)
plt.show()
```

Scatter plot:

```sh
plt.scatter(x,y)
plt.xscale('log') % put x-axis on a log scale
plt.show()
plt.scatter(x,y,s = [], c = [], alpha = 0.8) % specify the size/color of each data point shown in circles, alpha is the transparant level from 0 to 1
```
Histograms:

```sh
plt.hist(list_name, bin = 3)
plt.show()
plt.clf() % clear the plot
```

Customize the plots:

```sh
plt.xlabel('x_axis's name')
plt.ylabel('y_axis's label')
plt.title('title')
plt.yticks([value_1, value_2,...],['name_1','name_2',...])
plt.fill_between() % the area under the graph is colored
tick_val = [1000,10000,100000]
tick_lab = ['1k','10k','100k']
plt.xticks(tick_val, tick_lab)
plt.grid(True) % place grid
plt.text(x,y,'text')
```

### Control Flow and Pandas

```sh
if condition :
    expression
elif condition :
    expression
else :
    expression
```

For loops:

```sh
for i in range(int_1, int_2):
    do_sth
```



Pandas: A great package to deal with the tabular data with different types of data.

```sh
import pandas as pd
cars = pd.readcsv('cars.csv') % default row label is from 0 ..
cars = pd.readcsv('cars.csv', index_col = 0) % specify the first column to be the row label
print(cars)

cars['col_name'] % read a column as a Pandas Series
cars[['col_name']] % read a column as a Pandas DataFrame

cars.loc['col_name'] % return the row that this col_name lies in Pandas Series
cars.loc[['col_name']] % return the row that this col_name lies in Pandas DataFrame
cars.loc[['col_name1','col_name2']] % return 2 entire rows

select a certain elements by specifying the row and column
cars.loc['row_name','col_name']
select sub_DataFrame
cars.loc[['row_1','row_2'],['col_1','col_2']]

```
### good codes

reverse a string/list

```sh
str_1[::-1]
```

find a single number in a list where all others are in two

```sh
res = 0
for num in nums:
    res ^= num
print res
```

```sh
^= can be seen as not-binary XOR.  
x ^ x = 0
```



