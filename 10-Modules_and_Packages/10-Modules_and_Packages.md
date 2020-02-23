Modules and Packages
====================
The core Python programming language can be extended with so-called modules and packages. The standard library, which ships with every Python installation, is a collection of numerous modules for various purposes.

A *module* is a Python script that we can import in our own code in order to use whatever is defined in the module. A *package* organizes a collection of modules. We will see examples for both modules and packages later in this chapter.

We have already used functions from the `math` module (which is part of the standard library). Before using functions defined in a module, we have to import either the whole module or only specific functions from the module. Usually (by PEP8 convention), we import all modules at the top of a script.

Here's an example where we import the whole `math` module and then use some of its names and functions:

```python
>>> import math
>>> math.pi
3.141592653589793
>>> math.e
2.718281828459045
>>> math.sin(math.pi)
1.2246467991473532e-16  # practically zero (limited float precision)
>>> math.cos(math.pi)
-1.0
```

After `import math`, we can access the contents of the module by prepending `math.` to the actual names contained in the module (`math.pi`, `math.e`, `math.sin`, and so on).

The `dir` function lists all definitions contained in a module (we can ignore the dunder names, which are reserved for internal use):

```python
>>> dir (math)
['__doc__', '__file__', '__loader__', '__name__', '__package__', '__spec__', 'acos', 'acosh', 'asin', 'asinh', 'atan', 'atan2', 'atanh', 'ceil', 'comb', 'copysign', 'cos', 'cosh', 'degrees', 'dist', 'e', 'erf', 'erfc', 'exp', 'expm1', 'fabs', 'factorial', 'floor', 'fmod', 'frexp', 'fsum', 'gamma', 'gcd', 'hypot', 'inf', 'isclose', 'isfinite', 'isinf', 'isnan', 'isqrt', 'ldexp', 'lgamma', 'log', 'log10', 'log1p', 'log2', 'modf', 'nan', 'perm', 'pi', 'pow', 'prod', 'radians', 'remainder', 'sin', 'sinh', 'sqrt', 'tan', 'tanh', 'tau', 'trunc']
```

If we only want to use a limited number of functions from a module, we can save us some typing by importing functions from a module like this:

```python
>>> from math import sqrt, pi
>>> sqrt(4)
2.0
>>> 2 * 3**2 * pi
56.548667764616276
```

That way, we can use the functions directly as `sqrt` and `pi` instead of `math.sqrt` and `math.pi`, respectively.





---
![https://creativecommons.org/licenses/by-nc-sa/4.0/](cc_license.png) This document is licensed under the [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) by Clemens Brunner.