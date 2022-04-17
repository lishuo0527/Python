# IV. Comprehension 推導式

pay attention to the **different brackets** wrapping the expressions

## List
[expression for variable in list]
[expression for variable in list if condition]
[表达式 for 变量 in 列表]
[表达式 for 变量 in 列表 if 条件]

*Calculate the integers within 30 that are divisible by 3:*
```Python
multiples = [i for i in range(30) if i % 3 == 0]  # range(30) consist 0 to 29 integers
print(multiples)
```

## Set

{expression for item in Sequence if condition}

*Calculate the squareroot of the three numbers: 9, 25, 181.*

```Python
set1 = {n ** 0.5 for n in [9, 25, 196]}
print(set1)
```

## Dictionary

{key_expr : value_expr for value in collection if condition}

*Create a dictionary using strings and their lengths: the value of each string in the list is the key and the length is the value, forming key-value pairs*

```Python
list1 = ['Shuo','Yiwen', 'Qingzi', 'Calvin']
dict1 = {s : len(s) for s in list1}  # len() is a function whose return value is the length of the string
print(dict1)
```

*Provide four numbers to create a dictionary with positive numbers as keys and the square of the positive numbers as values.*

```Python
num = [2,-3, 7,8]
dict2 = {n : n ** 2 for n in num if n > 0}
print(dict2)
```



## Tuple

(expression for item in sequence if condition)

*Generate a tuple containing the cube of numbers 1 to 9*

```Python
tuple1 = (n ** 3 for n in range(1,10))
print(tuple1)  # return a generator object
print(tuple(tuple1))  # this is how we print the content of a tuple
```
