# Python Data Model

> *Objects* are Python’s abstraction for data. All data in a Python program is represented by objects or by relations between objects.

Data Model refers to the behaviour of objects in Python which we often refer to as *Pythonic*. 



## Special Methods

- The data model helps you leverage special methods to perform some basic operations on an object.

- Special methods are implemented by a leading an trailing `__` as in `__len__()`

- These methods are meant to be called by the Python interpreter,  `len(x)`

- Some of these special methods are:

  | special methods             | usage    | description                        |
  | --------------------------- | -------- | ---------------------------------- |
  | `__len__()`                 | `len(x)` | length of an object                |
  | `__getitem__()`             | `x[key]` | access elements of an object       |
  | `__repr__()` or `__str__()` | `str(x)` | string representation of an object |
  | `__call__()`                | `x()`    | make the object callable           |

- `len(x)` is faster than `x.length()` in CPython when `x` is an instance of built-in type because it simply reads from a field in the struct, hence `len()` is not a method due to the special treatment. 

- For more details: 
  - [*Python Language Reference: Data Model*](https://docs.python.org/3/reference/datamodel.html)
  - [*Fluent Python, Chapter 1: The Python Data Model*](https://www.amazon.com/Fluent-Python-Concise-Effective-Programming/dp/1491946008)