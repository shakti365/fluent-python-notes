# Array of Sequences

## Built-in Sequences

- **Container Sequences: **holds references to the objects of any type.
  - `list, collections.deque, tuple`
- **Flat Sequences:** holds values of the objects of only primitive types.
  - `str, bytes, bytearray, memoryview, array.array`
- **Mutable Sequences:** 
  - `list, bytearray, array.array, collections.deque, memoryview`
- **Immutable Sequences:**
  - `tuple, str, bytes`



## List Comprehensions

- Use it only for creating new lists.

- Leaked variables in Python 2 but was fixed in Python 3: variables assigned within the expression are local but do not mask the surrounding scope.

-  `map` and `filter` are not faster than *listcomps*

  ```
  >>> x = "abc"
  >>> y = [ord(x) for x in x]
  >>> x
  'abc'
  >>> y
  [97, 98, 99]
  ```

## Generator Expressions

- To initialize other sequences like tuples, array, etc use *genexp* because it saves memory.

- It yields items one by one using iterator.

  ```
  >>> x = "abc"
  >>> (ord(x) for x in x)
  <generator object <genexpr> at 0x7f103a496d00>
  >>> for y in (ord(x) for x in x):
  ...     print(y)
  ... 
  97
  98
  99
  ```

