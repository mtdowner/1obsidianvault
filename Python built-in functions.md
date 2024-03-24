Built-in Functions

**A**

[`abs()`](https://docs.python.org/3/library/functions.html#abs "abs")
Return the absolute value of a number. The argument may be an integer, a floating point number, or an object implementing [`__abs__()`](https://docs.python.org/3/reference/datamodel.html#object.__abs__ "object.__abs__"). If the argument is a complex number, its magnitude is returned.

[`aiter()`](https://docs.python.org/3/library/functions.html#aiter "aiter")
Return an [asynchronous iterator](https://docs.python.org/3/glossary.html#term-asynchronous-iterator) for an [asynchronous iterable](https://docs.python.org/3/glossary.html#term-asynchronous-iterable). Equivalent to calling `x.__aiter__()`.

> Note: Unlike [`iter()`](https://docs.python.org/3/library/functions.html#iter "iter"), [`aiter()`](https://docs.python.org/3/library/functions.html#aiter "aiter") has no 2-argument variant.

[`all()`](https://docs.python.org/3/library/functions.html#all "all")
Return `True` if all elements of the _iterable_ are true (or if the iterable is empty). Equivalent to:
```py
def all(iterable):
    for element in iterable:
        if not element:
            return False
    return True
```

`_awaitable_ anext`(_async_iterator_)[](https://docs.python.org/3/library/functions.html#anext "Link to this definition")

`_awaitable_ anext`(_async_iterator_, _default_)

When awaited, return the next item from the given [asynchronous iterator](https://docs.python.org/3/glossary.html#term-asynchronous-iterator), or _default_ if given and the iterator is exhausted.

This is the async variant of the [`next()`](https://docs.python.org/3/library/functions.html#next "next") builtin, and behaves similarly.

This calls the [`__anext__()`](https://docs.python.org/3/reference/datamodel.html#object.__anext__ "object.__anext__") method of _async_iterator_, returning an [awaitable](https://docs.python.org/3/glossary.html#term-awaitable). Awaiting this returns the next value of the iterator. If _default_ is given, it is returned if the iterator is exhausted, otherwise [`StopAsyncIteration`](https://docs.python.org/3/library/exceptions.html#StopAsyncIteration "StopAsyncIteration") is raised.

[`anext()`](https://docs.python.org/3/library/functions.html#anext "anext")

[`any()`](https://docs.python.org/3/library/functions.html#any "any")

[`ascii()`](https://docs.python.org/3/library/functions.html#ascii "ascii")

  

**B**

[`bin()`](https://docs.python.org/3/library/functions.html#bin "bin")

[`bool()`](https://docs.python.org/3/library/functions.html#bool "bool")

[`breakpoint()`](https://docs.python.org/3/library/functions.html#breakpoint "breakpoint")

[`bytearray()`](https://docs.python.org/3/library/functions.html#func-bytearray)

[`bytes()`](https://docs.python.org/3/library/functions.html#func-bytes)

  

**C**

[`callable()`](https://docs.python.org/3/library/functions.html#callable "callable")

[`chr()`](https://docs.python.org/3/library/functions.html#chr "chr")

[`classmethod()`](https://docs.python.org/3/library/functions.html#classmethod "classmethod")

[`compile()`](https://docs.python.org/3/library/functions.html#compile "compile")

[`complex()`](https://docs.python.org/3/library/functions.html#complex "complex")

  

**D**

[`delattr()`](https://docs.python.org/3/library/functions.html#delattr "delattr")

[`dict()`](https://docs.python.org/3/library/functions.html#func-dict)

[`dir()`](https://docs.python.org/3/library/functions.html#dir "dir")

[`divmod()`](https://docs.python.org/3/library/functions.html#divmod "divmod")

  

**E**

[`enumerate()`](https://docs.python.org/3/library/functions.html#enumerate "enumerate")

[`eval()`](https://docs.python.org/3/library/functions.html#eval "eval")

[`exec()`](https://docs.python.org/3/library/functions.html#exec "exec")

  

**F**

[`filter()`](https://docs.python.org/3/library/functions.html#filter "filter")

[`float()`](https://docs.python.org/3/library/functions.html#float "float")

[`format()`](https://docs.python.org/3/library/functions.html#format "format")

[`frozenset()`](https://docs.python.org/3/library/functions.html#func-frozenset)

  

**G**

[`getattr()`](https://docs.python.org/3/library/functions.html#getattr "getattr")

[`globals()`](https://docs.python.org/3/library/functions.html#globals "globals")

  

**H**

[`hasattr()`](https://docs.python.org/3/library/functions.html#hasattr "hasattr")

[`hash()`](https://docs.python.org/3/library/functions.html#hash "hash")

[`help()`](https://docs.python.org/3/library/functions.html#help "help")

[`hex()`](https://docs.python.org/3/library/functions.html#hex "hex")

  

**I**

[`id()`](https://docs.python.org/3/library/functions.html#id "id")

[`input()`](https://docs.python.org/3/library/functions.html#input "input")

[`int()`](https://docs.python.org/3/library/functions.html#int "int")

[`isinstance()`](https://docs.python.org/3/library/functions.html#isinstance "isinstance")

[`issubclass()`](https://docs.python.org/3/library/functions.html#issubclass "issubclass")

[`iter()`](https://docs.python.org/3/library/functions.html#iter "iter")

**L**

[`len()`](https://docs.python.org/3/library/functions.html#len "len")

[`list()`](https://docs.python.org/3/library/functions.html#func-list)

[`locals()`](https://docs.python.org/3/library/functions.html#locals "locals")

  

**M**

[`map()`](https://docs.python.org/3/library/functions.html#map "map")

[`max()`](https://docs.python.org/3/library/functions.html#max "max")

[`memoryview()`](https://docs.python.org/3/library/functions.html#func-memoryview)

[`min()`](https://docs.python.org/3/library/functions.html#min "min")

  

**N**

[`next()`](https://docs.python.org/3/library/functions.html#next "next")

  

**O**

[`object()`](https://docs.python.org/3/library/functions.html#object "object")

[`oct()`](https://docs.python.org/3/library/functions.html#oct "oct")

[`open()`](https://docs.python.org/3/library/functions.html#open "open")

[`ord()`](https://docs.python.org/3/library/functions.html#ord "ord")

  

**P**

[`pow()`](https://docs.python.org/3/library/functions.html#pow "pow")

[`print()`](https://docs.python.org/3/library/functions.html#print "print")

[`property()`](https://docs.python.org/3/library/functions.html#property "property")

  

  

  

  

**R**

[`range()`](https://docs.python.org/3/library/functions.html#func-range)

[`repr()`](https://docs.python.org/3/library/functions.html#repr "repr")

[`reversed()`](https://docs.python.org/3/library/functions.html#reversed "reversed")

[`round()`](https://docs.python.org/3/library/functions.html#round "round")

  

**S**

[`set()`](https://docs.python.org/3/library/functions.html#func-set)

[`setattr()`](https://docs.python.org/3/library/functions.html#setattr "setattr")

[`slice()`](https://docs.python.org/3/library/functions.html#slice "slice")

[`sorted()`](https://docs.python.org/3/library/functions.html#sorted "sorted")

[`staticmethod()`](https://docs.python.org/3/library/functions.html#staticmethod "staticmethod")

[`str()`](https://docs.python.org/3/library/functions.html#func-str)

[`sum()`](https://docs.python.org/3/library/functions.html#sum "sum")

[`super()`](https://docs.python.org/3/library/functions.html#super "super")

  

**T**

[`tuple()`](https://docs.python.org/3/library/functions.html#func-tuple)

[`type()`](https://docs.python.org/3/library/functions.html#type "type")

  

**V**

[`vars()`](https://docs.python.org/3/library/functions.html#vars "vars")

  

**Z**

[`zip()`](https://docs.python.org/3/library/functions.html#zip "zip")

  

**_**

[`__import__()`](https://docs.python.org/3/library/functions.html#import__ "__import__")