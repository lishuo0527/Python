# II. Basic Data Type
variables in Python do not need to be declared(their names and types)
Every variable have to be assigned value first before use, and then the variable can be created. (More specifically, the variable has a place created in RAM)
in Python, a variable is just a variable, which does not have a "type"(like in Java). The data types we referred to is the types of objects variables point to in RAM.

## a) assign value to multiple variables
Python allows you to assign value to multiple variables at the same time.
```python
a = b = c = 1 # the assignment sequence is from the last to the first
d, e, f = 1, 2.2, "LeeSek" # it's equivalent that d = 1; e = 2.2; f = "LeeSek"
```
## b) Standard data types (6 in total)

mutable 可變 (3)
- Number
- String 字符串
- Tuple 元組

immutable 不可變 (3)
- List 列表
- Set 集合
- Dictionary 字典

## c) Number
int, float, bool, complex(複數) are the four types of numbers.
*for java learners: for integers or float numbers there is only one type separately, which perform as long or double in Java*

####indicate the object types pointed to by variables
*question: why didn't I write "variable types? "*
using type(variable) we can check the types
```python
a, b, c, d = 20, 5.5, True, 4+3j
print(type(a), type(b), type(c), type(d))
```
the output is:
```
<class 'int'> <class 'float'> <class 'bool'> <class 'complex'>
```

and we also can use isinstance(variable, type)
```Python
a = 2001314
isinstance(a, int)
```
output:
```python
True
```

in Python 3, bool class is a *subclass** of int, essentially, True and False can calculate together(i.e. True==1、False==0)
*(Trivia: there is no bool type in Python 2, 0 is for False and 1 for True)*

*subclass is like a child from another class(parent)

we can use "is" to check the type.

```Python
0 is True
```

```Python
True
```

#### Delete references of variables
```Python
del variable
del var_a, var_b
```

## Calculation

>>> 2 / 4  # 正常除法，得到一个浮点数
0.5
>>> 2 // 4 # 地板除，得到一个整数（扔掉小數點後面）
0
>>> 17 % 3 # 取餘
2
>>> 2 ** 5 # 乘方
32

when an integer is calculated with a float, the integer will automatically be converted to a float to proceed.

## d) Strings
Python 没有单独的字符类型，一个字符就是长度为1的字符串。
*for java learners: there is no such thing as char in Python, when it comes to a charater, it is a string whose length is 1.

Strings are **immutable**! for example
```Python
m = "love"
m[1] = "i"
```
the output won't be **live** but it will show an error.

## e) List [列表] 方括號 square brackets
Lists are the most frequently used data types in Python.
The elements in lists can be numbers, strings and even other lists(it's called nesting).

## f) Tuple (元組) 圓括號 parentheses

Like the characteristics of strings we introduced in the chap I, lists can also be indexed and intercepted. You can refer to this picture and the relevant part in the chap I.
https://www.runoob.com/wp-content/uploads/2014/08/list_slicing1_new1.png
```python
tup1 = ()    # an empty/void tuple
tup2 = (20,) # when a tuple only contains one element, in the end we must add a comma to be distinguished from the operators that parentheses function as
```

although tuples' entries/elements are immutable, but tuples can include mutable object like lists.

tuples can also use + operator to be linked together.

Strings, to its essence, are special tuples because of their immutability.

Strings, lists and tuples are called sequences (序列)

## g) Set (集合) 花括號 curly brackets
A set is made up of one or several whole groups of different sizes. The things or objects that make up a set are called elements or members.

The basic function of sets is to **perform membership tests and to remove duplicate elements**.
Please have a careful test using the code below and pay attention to when we use {} or ().

```Python
name = {'S','h','u','o'}
name1 = set('Shuo')
voidSet = set()
```

#### create sentences: using curly brackets {} or set() function

```Python
sites = {'Lazada', 'Taobao', 'Shopee', 'JD', 'Pinduoduo', 'Pinduoduo'}

print(sites) # what is the output?
```
as we can see from the test above, duplicate members will be automatically removed.

#### member tests

```Python
sites = {'Lazada', 'Taobao', 'Shopee', 'JD', 'Pinduoduo', 'Pinduoduo'}
if 'Meituan' in sites: #do not forget the colon(:) in the end of the sentence
  print("Meituan is in shopping sites")
else:
  print("Meituan is not in shopping sites")
```
from the above test, we can conclude that **element** in **sequence** is a boolean expression

#### sets operation/calculation

```Python
a = set("LiShuo")
b = set("LeeSek")

print(a - b) # difference 差集
print(b - a) # be cautious what is to be deducted 注意誰減誰
print(a | b) # union 並集
print(a & b) # intersection 交集
print(a ^ b) # Not co-existing members 不同時存在的成員
```

## h) Dictionary (字典) 花括號 curly brackets 冒號 colons
Lists are ordered collections of objects and dictionaries are unordered collections of **鍵(key) : 值(value)**
keys must be immutable, and remain only in a same dictionary.

#### Take a look back at lists.
```Python
list1 = ['S', 2, 0, 0, 1, 3, 1, 4]
print(list1[2] + list1[4]) #what is the output?
````
as you can see, the indexes(**starting from 0**) are 0, 1, 2, 3, ..., and the elements are what is inside the square brackets.

#### back to our beloved dictionaries
the indexes of dictionaries are not just 0, 1, 2, 3, ..., and they do not follow a sequence (unordered), and the elements are what is inside the square brackets and behind the colons.

```Python

dict = {}  # create a void dictionary
dict['my name'] = "Li Shuo"
dict[1] = "True"

friend = {'Malaysian1' : 'Calvin', 'Chinese1' : 'YQZ', 'Chinese2' : 'Teoh Yee Bong'}

print (dict['my name'])       # output the value whose key is 'my name'输出键为 'my name' 的值
print (dict[1])           # output the value whose key is 1
print (friend)          # output the whole dictionary
print (friend.keys())   # output all keys
print (friend.values()) # output all values
```
Same as in sets, a function dict() can be used to create dictionaries

```python
dict1 = dict([('Calvin', 8), ('YQZ', 6), ('TeohYeeBong', 1)])  # do notice that there exist quotation marks enclosing the strings' content
dict2 = dict(Calvin= 8 , YQZ= 6 , TeohYeeBong = 1)
# do notice that for strings we do no need the quotation marks

print(dict1)
print(dict2)
```
*summary*
dict([(key1, value1), (key2, value2), ..., (key_, value_)])

dict(key1 = value1, key2 = value2, ..., key_ = value_)

#### 字典推導式
```Python
dict1 = {x: x**2 for x in (2, 4, 6)}
print(dict1)
```

```Python
{2: 4, 4: 16, 6: 36}
```

dict1 = [表达式 for 变量 in 列表 if 条件] # [out_exp_res for out_exp in input_list if condition]
"if condition" can be removed
