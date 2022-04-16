# III. Data Type Conversion

Sometimes we need to convert the types built into the data. Normally we just need to write the data type as a function name.
There are 2 categories of conversions:
    **Implicit**: automatically done
    **Explicit**- using conversing functions

## Implicit Conversions (automatic)

The lower data type (for example, int) is automatically converted to the higher data type (float) to avoid data loss.

```Python
num_int = 100
num_float = 1.23

num_result = num_int + num_float
print("Value of num_result:",num_result)
print("datatype of num_int:",type(num_int))
print("datatype of num_float:",type(num_float))
print("datatype of num_result:",type(num_result))
```

After calculation, the data type of the original data will not change. It is only during calculation that the lower data type changes into the higher.

*Try to run the code below and see what will happen.*
```Python
num_int = 123
num_str = "456"

print("Data type of num_int:",type(num_int))
print("Data type of num_str:",type(num_str))

print(num_int+num_str)
```

## Explicit Conversions (Forced)

As you can see from the code right above, it reports an error. Python cannot use implicit conversions in such cases. However, Python provides a solution for these types of cases, called explicit conversions.

```Python
a = int("3")
b = float(245)
c = str(3.141)
d = str("goodbye covid")  # data type, when convertd to the data type of itself, remains what it was.
print(a,"\n", b, "\n", c, "\n", d)
```

#### Other explicit conversions
```python
tuple(s)  # convert sequence s to a tuple
list(s)  # convert sequence s to a list
set(s)  # convert s to a mutable set
frozenset(s)  # convert s to a immutable set
dict(d)  # convert d to a dictionary, d has to be a sequence consisting of (key, value)

chr(x) # convert an integer to a single charater
ord(x) # convert a single charater to its integer value
hex(x) # convert an integer to a hexadecimal string
oct(x) # convert an integer to an octal string
```
