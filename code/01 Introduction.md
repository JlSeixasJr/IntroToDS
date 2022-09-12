---
jupyter:
  kernelspec:
    display_name: Python 3 (ipykernel)
    language: python
    name: python3
  language_info:
    codemirror_mode:
      name: ipython
      version: 3
    file_extension: .py
    mimetype: text/x-python
    name: python
    nbconvert_exporter: python
    pygments_lexer: ipython3
    version: 3.7.12
  latex_envs:
    autoclose: false
    autocomplete: true
    bibliofile: biblio.bib
    cite_by: apalike
    current_citInitial: 1
    eqLabelWithNumbers: true
    eqNumInitial: 1
    hotkeys:
      equation: Ctrl-E
      itemize: Ctrl-I
    labels_anchors: false
    LaTeX_envs_menu_present: true
    latex_user_defs: false
    report_style_numbering: false
    user_envs_cfg: false
  nbformat: 4
  nbformat_minor: 4
---

::: {.cell .markdown}
# Introduction
:::

::: {.cell .markdown}
## Comments
:::

::: {.cell .markdown}
To write something
:::

::: {.cell .code execution_count="4"}
``` {.python}
#my comments
print("Hello World!")
```

::: {.output .stream .stdout}
    Hello World!
:::
:::

::: {.cell .code execution_count="5"}
``` {.python}
print("Hello World!") #Some comment
```

::: {.output .stream .stdout}
    Hello World!
:::
:::

::: {.cell .code}
``` {.python}
"""
Multiple lines comments.
"""

# crtl + /
# cmd + /

# I
# want 
# to 
# comment
```
:::

::: {.cell .markdown}
## Variables
:::

::: {.cell .code execution_count="6"}
``` {.python}
x = 5
y = "string"

print(x, y)
```

::: {.output .stream .stdout}
    5 string
:::
:::

::: {.cell .code execution_count="7"}
``` {.python}
x = 10
x = "another"

print(x, y)
```

::: {.output .stream .stdout}
    another string
:::
:::

::: {.cell .markdown}
### Rules for Variables
:::

::: {.cell .code execution_count="9"}
``` {.python}
myVar = 1
my_var = 1
myvar2 = 1
_myvar = 1
MyVar = 1

MyVar
```

::: {.output .execute_result execution_count="9"}
    1
:::
:::

::: {.cell .code execution_count="10"}
``` {.python}
2myvar = 1
```

::: {.output .error ename="SyntaxError" evalue="invalid syntax (<ipython-input-10-29075fb64ebe>, line 1)"}
      File "<ipython-input-10-29075fb64ebe>", line 1
        2myvar = 1
             ^
    SyntaxError: invalid syntax
:::
:::

::: {.cell .code execution_count="11"}
``` {.python}
x, y, z = 100, "type", True

print(x, y, z)
```

::: {.output .stream .stdout}
    100 type True
:::
:::

::: {.cell .code execution_count="13"}
``` {.python}
x = 5

def myfunc():
    global x
    print("Value of x is ", x)
    x = 1
    
myfunc()
myfunc()
```

::: {.output .stream .stdout}
    Value of x is  5
    Value of x is  1
:::
:::

::: {.cell .markdown}
## Printing
:::

::: {.cell .code execution_count="14"}
``` {.python}
myVar = "something"

myVar
```

::: {.output .execute_result execution_count="14"}
    'something'
:::
:::

::: {.cell .code execution_count="15"}
``` {.python}
print(myVar)
```

::: {.output .stream .stdout}
    something
:::
:::

::: {.cell .code execution_count="17"}
``` {.python}
name = "Jose"
age = 33

print("My name is {var1} and I am {var2} years old.".format(var1=name, var2=age))
print("My name is {} and I am {} years old.".format(name, age))
```

::: {.output .stream .stdout}
    My name is Jose and I am 33 years old.
    My name is Jose and I am 33 years old.
:::
:::

::: {.cell .markdown}
## Data Types
:::

::: {.cell .code execution_count="22"}
``` {.python}
z = 2/3
type(z)
```

::: {.output .execute_result execution_count="22"}
    float
:::
:::

::: {.cell .code execution_count="21"}
``` {.python}
x = False
type(x)
```

::: {.output .execute_result execution_count="21"}
    bool
:::
:::

::: {.cell .code execution_count="23"}
``` {.python}
type(x)==type(z)
```

::: {.output .execute_result execution_count="23"}
    False
:::
:::

::: {.cell .code execution_count="26"}
``` {.python}
x = int(z)

print(x, type(x))
```

::: {.output .stream .stdout}
    0 <class 'int'>
:::
:::

::: {.cell .markdown}
## Strings
:::

::: {.cell .code execution_count="27"}
``` {.python}
'single'
```

::: {.output .execute_result execution_count="27"}
    'single'
:::
:::

::: {.cell .code execution_count="28"}
``` {.python}
"double"
```

::: {.output .execute_result execution_count="28"}
    'double'
:::
:::

::: {.cell .code execution_count="31"}
``` {.python}
phrase = "My name is "

print(phrase+name)
print(phrase, age)
```

::: {.output .stream .stdout}
    My name is Jose
    My name is  33
:::
:::

::: {.cell .code execution_count="32"}
``` {.python}
words = "You're students."
words
```

::: {.output .execute_result execution_count="32"}
    "You're students."
:::
:::

::: {.cell .markdown}
## Lists
:::

::: {.cell .code execution_count="33"}
``` {.python}
['a','b','c','d']
```

::: {.output .execute_result execution_count="33"}
    ['a', 'b', 'c', 'd']
:::
:::

::: {.cell .code execution_count="35"}
``` {.python}
myList = [10, 6.5, 'z', ["You", "Me"], False]
myList
```

::: {.output .execute_result execution_count="35"}
    [10, 6.5, 'z', ['You', 'Me'], False]
:::
:::

::: {.cell .code execution_count="38"}
``` {.python}
myList[-1]
```

::: {.output .execute_result execution_count="38"}
    False
:::
:::

::: {.cell .code execution_count="39"}
``` {.python}
myList[1:4]
```

::: {.output .execute_result execution_count="39"}
    [6.5, 'z', ['You', 'Me']]
:::
:::

::: {.cell .code execution_count="40"}
``` {.python}
b = True
myList.append(b)
myList
```

::: {.output .execute_result execution_count="40"}
    [10, 6.5, 'z', ['You', 'Me'], False, True]
:::
:::

::: {.cell .code execution_count="42"}
``` {.python}
myList = myList[0:3]
myList
```

::: {.output .execute_result execution_count="42"}
    [6.5, 'z', ['You', 'Me']]
:::
:::

::: {.cell .code execution_count="45"}
``` {.python}
myList[:1]
```

::: {.output .execute_result execution_count="45"}
    [6.5]
:::
:::

::: {.cell .code execution_count="46"}
``` {.python}
#Length
len(myList)
```

::: {.output .execute_result execution_count="46"}
    3
:::
:::

::: {.cell .code execution_count="47"}
``` {.python}
myList.insert(1, 'y')
myList
```

::: {.output .execute_result execution_count="47"}
    [6.5, 'y', 'z', ['You', 'Me']]
:::
:::

::: {.cell .code execution_count="48"}
``` {.python}
myList.remove(['You', 'Me'])
myList
```

::: {.output .execute_result execution_count="48"}
    [6.5, 'y', 'z']
:::
:::

::: {.cell .code execution_count="49"}
``` {.python}
myList.pop(-1)
myList
```

::: {.output .execute_result execution_count="49"}
    [6.5, 'y']
:::
:::

::: {.cell .code execution_count="50"}
``` {.python}
del myList[0]
myList
```

::: {.output .execute_result execution_count="50"}
    ['y']
:::
:::

::: {.cell .code execution_count="51"}
``` {.python}
mySecList = [1,2,3]
list3 = myList + mySecList
list3
```

::: {.output .execute_result execution_count="51"}
    ['y', 1, 2, 3]
:::
:::

::: {.cell .code}
``` {.python}
```
:::

::: {.cell .markdown}
## Dictionaries
:::

::: {.cell .code execution_count="52"}
``` {.python}
ids = {
    1:{ #Index
        "name":"Jose", #key : #item
        "age":33,
        "height":187,
        "year":2019
    },
    2:{
        "name":"Ana",
        "age":35,
        "height":167,
        "year":2017
    }
}

ids
```

::: {.output .execute_result execution_count="52"}
    {1: {'name': 'Jose', 'age': 33, 'height': 187, 'year': 2019},
     2: {'name': 'Ana', 'age': 35, 'height': 167, 'year': 2017}}
:::
:::

::: {.cell .code execution_count="53"}
``` {.python}
myName = ids[1]
othrName = ids.get(2)

print(myName)
print(othrName)
```

::: {.output .stream .stdout}
    {'name': 'Jose', 'age': 33, 'height': 187, 'year': 2019}
    {'name': 'Ana', 'age': 35, 'height': 167, 'year': 2017}
:::
:::

::: {.cell .code execution_count="54"}
``` {.python}
age = othrName["age"]
age
```

::: {.output .execute_result execution_count="54"}
    35
:::
:::

::: {.cell .code execution_count="55"}
``` {.python}
othrName["year"] = 2021
othrName
```

::: {.output .execute_result execution_count="55"}
    {'name': 'Ana', 'age': 35, 'height': 167, 'year': 2021}
:::
:::

::: {.cell .markdown}
## Sets
:::

::: {.cell .code execution_count="56"}
``` {.python}
set1 = {"a", "b", "c"}
set2 = {1, 2, 3}

set3 = set1.union(set2)
set3
```

::: {.output .execute_result execution_count="56"}
    {1, 2, 3, 'a', 'b', 'c'}
:::
:::

::: {.cell .code execution_count="57"}
``` {.python}
set3.discard(3)
```
:::

::: {.cell .code execution_count="58"}
``` {.python}
set3.remove('a')
```
:::

::: {.cell .code execution_count="59"}
``` {.python}
set3.remove('d')
```

::: {.output .error ename="KeyError" evalue="'d'"}
    ---------------------------------------------------------------------------
    KeyError                                  Traceback (most recent call last)
    <ipython-input-59-9cfe27f2acf4> in <module>
    ----> 1 set3.remove('d')

    KeyError: 'd'
:::
:::

::: {.cell .code execution_count="60"}
``` {.python}
set3.discard('d')
```
:::

::: {.cell .code execution_count="61"}
``` {.python}
set3
```

::: {.output .execute_result execution_count="61"}
    {1, 2, 'b', 'c'}
:::
:::

::: {.cell .markdown}
## Operators
:::

::: {.cell .code execution_count="62"}
``` {.python}
x = 10
y = 20
```
:::

::: {.cell .code execution_count="63"}
``` {.python}
x > y
```

::: {.output .execute_result execution_count="63"}
    False
:::
:::

::: {.cell .code execution_count="64"}
``` {.python}
x < y
```

::: {.output .execute_result execution_count="64"}
    True
:::
:::

::: {.cell .code execution_count="65"}
``` {.python}
x == y # x != y
```

::: {.output .execute_result execution_count="65"}
    False
:::
:::

::: {.cell .code execution_count="66"}
``` {.python}
x >= y
```

::: {.output .execute_result execution_count="66"}
    False
:::
:::

::: {.cell .code execution_count="67"}
``` {.python}
x <= y
```

::: {.output .execute_result execution_count="67"}
    True
:::
:::

::: {.cell .code execution_count="68"}
``` {.python}
not(x == y)
```

::: {.output .execute_result execution_count="68"}
    True
:::
:::

::: {.cell .code execution_count="69"}
``` {.python}
x > 5 and x < 20 #or
```

::: {.output .execute_result execution_count="69"}
    True
:::
:::

::: {.cell .markdown}
## if statements
:::

::: {.cell .code execution_count="70"}
``` {.python}
if  x < y:
    print("is less")
```

::: {.output .stream .stdout}
    is less
:::
:::

::: {.cell .code execution_count="71"}
``` {.python}
x = 25
if  x < y:
    print("is less")
else: 
    print("is greater")
```

::: {.output .stream .stdout}
    is greater
:::
:::

::: {.cell .code execution_count="73"}
``` {.python}
x = 20
if  x < y:
    print("is less")
elif x > y:
    print("is greater")
else:
    print("is equal")
```

::: {.output .stream .stdout}
    is equal
:::
:::

::: {.cell .markdown}
## Loops
:::

::: {.cell .code execution_count="75"}
``` {.python}
newset = range(10)
print(newset)
```

::: {.output .stream .stdout}
    range(0, 10)
:::
:::

::: {.cell .code execution_count="78"}
``` {.python}
import random

for i in range(10): #0 1 2 3 4 5 6 7 8 9 range(lower, upper, step)
    n = random.randint(1, 50)
    print(n)
```

::: {.output .stream .stdout}
    14
    6
    17
    45
    35
    34
    43
    23
    42
    37
:::
:::

::: {.cell .code execution_count="79"}
``` {.python}
i = 0
while i < 25:
    print("Another")
    i = random.randint(1, 30)
    print(i)
```

::: {.output .stream .stdout}
    Another
    14
    Another
    11
    Another
    18
    Another
    11
    Another
    24
    Another
    28
:::
:::
