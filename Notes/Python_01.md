# I) Basic Grammar of Python

## a) the first python program
```python
print("Hello, world!")
```
------
## b) identifier

the first charater has to be a alphabet letter or underline
the other parts can be letters, numbers, Chinese characters or underline
case sensitive

cannot be the same name as any key word's, such as 'False', 'None', 'True', 'and', 'as', 'assert', 'break', 'class', 'continue', 'def'

## c) indentation
no need using curly brackets, instead we use different indentation
for example

```python
if True:
    print ("Answer")
    print ("True")
else:
    print ("Answer")
  print ("False")    # if the indentation is mistyped, it will bring different output


```
------
## d) multiple-line-sentence

a sentence is written in a line, but if the sentence is too long we can use backslash

```python
total = item_one + \
        item_two + \
        item_three
```

if in the [], {}, or () we don't need to use backslash

```python
total = ['item_one', 'item_two', 'item_three',
        'item_four', 'item_five']



```

------

the brackets can automatically detect multiple lines

## e) Number types

int (integer)
bool (boolean)： True False # the first letter is uppercase
float: 1.23、3E-2

complex: 1 + 2j

## f) data type of String

in Python, single quotation mark ' is identical to double quotation mark "
escape character: \
but if we use r we can make the backslash not act as the escape charater

```python
r"this is a line with \n" #although we wrote \n, it will not create a new line
```

automatic linking strings: "this " "is " "string" will be automatically converted to "this is string"
fyi,"r" here refers to raw string.

we use + to link strings or link strings and whatever can be shown

```python
print("my name is " + myName)  # sample output: my name is Shuo
print("my height is " + myHeight*100) # sample output: my height is 172
```



*(star character) is used to repeat strings

```python
print("yesmola " * 3) # sample output: yesmola yesmola yesmola
```


 strings in python, once assigned values to, cannot be changed

there is no such data type as char(character) in Python
but a character is a string whose length is 1

#### assess strings

 index starts from 0

```python
str = '123456789'
print(str[0])              # output: 1
print(str[0:-1])           # output: 12345678
print(str[0:5])            # output: 12345
print(str[2:-2])           # output: 34567
print(str[2:])             # output: 3456789
print(str[1:5:2])          # output:24
print(str[1:5:1])          # output:2345

```

*Test yourself*
Can you generalise a summary after you have tried the code above?

------
## g) input
``` python
input("Please type your name here:" )
```
when the user presses the enter key, the program will automatically exit

to its essence, input() is a function via which we can get the input from user
so, we can assign the value of input() to a variable, here comes the example:

``` python
a = input("Please enter your age: ")
print(a)
```



*for Java learners*
unlike Java, we do not need to declare the variable's name and type as in the code example above
you can assume that the first assginment of value makes the decalration in the meanwhile
and the data type of variables can be certained in the first assginment

------
## h) multiple sentences and code group
As you can notice, in some programming languages we need a semicolon ";" to mark the end of the line
However in Python we don't need that, a separate line without a ";" can be read by compliers
but if you are to use the semicolon to separate the sentences, here comes an example:
```python
import sys; x = 'runoob'; print(x)
```
------
## i) output using print()
Let's rerun the example given in g), have you noticed that when print() is executed, it automatically starts a new underline
*(for java learners)* it's like python writes a System.out.println() after print() by default
if you don't want to create a new line, you have to attach a end="" at the end of brackets inside

```python
x = "i"
y = 6
# output with a new line
print(x)
print(y)
print('------')
# output without creating a new line
print(x, end = "")
print(y, end = "")
```
*Test yourself*
How many lines will the output of the Python code below consist of(including blank lines)? What kind of sentence can function as a new line creater? Run it to see if you answer it right. And you can also see the answer at the Appendix part.
```Python
name = input("Please enter your name: )
c = "Hey " + name # Strings can be linked using plus sign(+)
s = "I'm Li Shuoshuo. "
print("\n")
print(c, end = "");print("")
print(s)
print(r"Can you answer it right? \n")
print()
```

------
## j) Comments
#### Single-line comments: start with a hash(#)
single-line sentence:
```python
# This is a comment
print("Hello, World!")
```
single-line and attached to a sentence
```python
print("Hello, World!") # This is a comment
```
#### Multiple-line comments: using quotation marks
it's like a multiple-line string:
```Python
"""
this is a comment
"""
print("using single or double quotation marks is okay")
'''
this is also a comment
'''
```
------
## Appendix
#### Answers
f)summary: string[頭下標：尾下標:step]

g) 8

print()
print("")
print(whatever)
Above are equivalent to pressing the enter key one time, i.e. creating a new line.

explanation = "find me"
