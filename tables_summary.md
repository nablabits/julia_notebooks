# Getting help

|Julia|Python
|-----|------
|`?obj` | `help(obj)`
|`dump(obj)` | `print(repr(obj))`
|`names(FooModule)` | `dir(foo_module)`
|`methodswith(SomeType)` | `dir(SomeType)`
|`@which func` | `func.__module__`
|`apropos("bar")` | Search for `"bar"` in docstrings of all installed packages
|`typeof(obj)` | `type(obj)`
|`obj isa SomeType`<br />or<br />`isa(obj, SomeType)` | `isinstance(obj, SomeType)`

## Estimating pi

|Julia|Python
|-----|------
|`function` | `def`
|`for i in X`<br />&nbsp;&nbsp;&nbsp;&nbsp;`...`<br />`end` | `for i in X:`<br />&nbsp;&nbsp;&nbsp;&nbsp;`...`
|`1:n` | `range(1, n+1)`
|`cond ? a : b` | `a if cond else b`
|`2i + 1` | `2 * i + 1`
|`4s` | `return 4 * s`
|`println(a, b)` | `print(a, b, sep="")`
|`print(a, b)` | `print(a, b, sep="", end="")`
|`"$p"` | `f"{p}"`
|`"$(p - π)"` | `f"{p - math.pi}"`

## Imports

|Julia|Python
|-----|------
|`using Foo` | `from foo import *; import foo`
|`using Foo.Bar` | `from foo.bar import *; from foo import bar`
|`using Foo.Bar: a, b` | `from foo.bar import a, b`
|`using Foo: Bar` | `from foo import bar`

## Running Python code in Julia

|Julia|Python
|-----|------
|`np = pyimport("numpy")` | `import numpy as np`
|`using PyPlot` | `from pylab import *`
|`1:10` | `range(1, 11)`
|`1:2:10`<br />or<br />`range(1, 11, 2)` | `range(1, 11, 2)`
|`1.2:0.5:10.3`<br />or<br />`range(1.2, 10.3, step=0.5)` | `np.arange(1.2, 10.3, 0.5)`
|`range(1, 10, length=3)` | `np.linspace(1, 10, 3)`
|`collect(1:5)`<br />or<br />`[i for i in 1:5]` | `list(range(1, 6))`<br />or<br />`[i for i in range(1, 6)]`

## Numbers

|Julia|Python
|-----|------
|`3.4 + 4.5im` | `3.4 + 4.5j`
|`BigInt(2)^1000` | `2**1000`
|`BigFloat(3.14)` | `from decimal import Decimal`<br />`Decimal(3.14)`
|`9//8` | `from fractions import Fraction`<br />`Fraction(9, 8)`
|`5/2 == 2.5` | `5/2 == 2.5`
|`5÷2 == 2`<br />or<br />`div(5, 2)` | `5//2 == 2`
|`57%10 == 7` | `57%10 == 7`
|`(-57)%10 == -7` | `(-57)%10 == 3`


## Strings

|Julia|Python
|-----|------
|``repeat("tick, ", 10) * "BOOM!"`` |`` "tick, " * 10 + "BOOM!"``
|``join(array, separator, [last_join])`` |`` array.join([separator])``
|``split(string, [separator])`` |`` string.split([separator])``
|``occursin(member, group)`` |`` member in group``
|``"foo \$$variable \$$(expression)"`` |`` "foo {} {}".format(variable, expression)``
|`try`<br />&nbsp;&nbsp;&nbsp;&nbsp;`...`<br />`catch ex`<br />&nbsp;&nbsp;&nbsp;&nbsp;`...`<br />`end`|`try`<br />&nbsp;&nbsp;&nbsp;&nbsp;`...`<br />`except Exception as ex`<br />&nbsp;&nbsp;&nbsp;&nbsp;`...`<br />`end`


## Control flow

|Julia|Python
|-----|------
|`if cond1`<br />&nbsp;&nbsp;&nbsp;&nbsp;`...`<br/>`elseif cond2`<br />&nbsp;&nbsp;&nbsp;&nbsp;`...`<br/>`else`<br />&nbsp;&nbsp;&nbsp;&nbsp;`...`<br/>`end` |`if cond1:`<br />&nbsp;&nbsp;&nbsp;&nbsp;`...`<br/>`elif cond2:`<br />&nbsp;&nbsp;&nbsp;&nbsp;`...`<br/>`else:`<br />&nbsp;&nbsp;&nbsp;&nbsp;`...`
|`&&` | `and`
|`\|\|` | `or`
|`!` | `not`
|`⊻` (type `\xor<tab>`) | `^`
|`true` | `True`
|`false` | `False`
|`@assert` |` assert`
|`cond && f()` | `if cond: f()`
|`cond \|\| f()` | `if not cond: f()`
|`1 == 1 && println("red")`<br /> `1 == 1 \|\| println("black")`|`'red' if 1 == 1 else 'black'`
|`Nothing` | `None` 
|`for i in 1:5 ... end` | `for i in range(1, 6): ...`
|`for i in 1:5, j in 1:6 ... end` | `from itertools import product`<br />`for i, j in product(range(1, 6), range(1, 7)):`<br />&nbsp;&nbsp;&nbsp;&nbsp;`...`
|`while cond ... end` | `while cond: ...`
|`continue` | `continue`
|`break` | `break`


## Arrays

|Julia|Python
|-----|------
|`a = [1, 2, 3]` | `a = [1, 2, 3]`<br />or<br />`import numpy as np`<br />`np.array([1, 2, 3])`
|`a[1]` | `a[0]`
|`a[end]` | `a[-1]`
|`a[2:end-1]` | `a[1:-1]`
|`push!(a, 5)` | `a.append(5)`
|`pop!(a)` | `a.pop()`
|`M = [1 2 3]` | `np.array([[1, 2, 3]])`
|`M = [1 2 3]'` | `np.array([[1, 2, 3]]).T`
|`M = hvcat(1,  1, 2, 3)` | `np.array([[1], [2], [3]])`
|`M = [1 2 3`<br />&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;`4 5 6]`<br />or<br />`M = [1 2 3; 4 5 6]` | `M = np.array([[1,2,3], [4,5,6]])`
|`M[1:2, 2:3]` | `M[0:2, 1:3]`
|`[M1; M2]` | `np.r_[M1, M2]`
|`[M1  M2]` | `np.c_[M1, M2]`
|`[M1 M2; M3]` | `np.r_[np.c_[M1, M2], M3]`


## Dictionaries

Julia|Python
|-----|------
|`Dict("tree"=>"arbre", "love"=>"amour")` | `{"tree": "arbre", "love": "amour"}`
|`d["arbre"]` | `d["arbre"]`
|`get(d, "unknown", "default")` | `d.get("unknown", "default")`
|`keys(d)` | `d.keys()`
|`values(d)` | `d.values()`
|`haskey(d, k)` | `k in d`
|`Dict(i=>i^2 for i in 1:4)` | `{i: i**2 for i in 1:4}`
|`for (k, v) in d` | `for k, v in d.items():`
|`merge(d1, d2)` | `{**d1, **d2}`
|`merge!(d1, d2)` | `d1.update(d2)`


## Sets

|Julia|Python
|-----|------
|`Set([1, 3, 5, 7])` | `{1, 3, 5, 7}`
|`5 in odd` | `5 in odd`
|`Set([i^2 for i in 1:4])` | `{i**2 for i in range(1, 5)}`
|`odd ∪ primes` | `odd | primes`
|`union(odd, primes)` | `odd.union(primes)`
|`odd ∩ primes` | `odd & primes`
|`insersect(odd, primes)` | `odd.intersection(primes)`
|`setdiff(odd, primes)` | `odd - primes` or `odd.difference(primes)`
|`symdiff(odd, primes)` | `odd ^ primes` or `odd.symmetric_difference(primes)`


## Enums

|Julia|Python
|-----|------
|`@enum Fruit apple=1 banana=2 orange=3` | `from enum import Enum`<br />`class Fruit(Enum):`<br />&nbsp;&nbsp;&nbsp;&nbsp;`APPLE = 1`<br />&nbsp;&nbsp;&nbsp;&nbsp;`BANANA = 2`<br />&nbsp;&nbsp;&nbsp;&nbsp;`ORANGE = 3`
| `Fruit(2) === banana` | `Fruit(2) is Fruit.BANANA`
| `instances(Fruit)` | `dir(Fruit)`


## Object identity

|Julia|Python
|-----|------
|`a === b` | `a is b`
|`a !== b` | `a is not b`
|`objectid(obj)` | `id(obj)`


## Functions

|Julia|Python (3.8+ if `/` is used)
|-----|------
| `function foo(a, b=2, c=3)`<br />&nbsp;&nbsp;&nbsp;&nbsp;`...`<br />`end`<br /><br />`foo(1, 2) # positional only` | `def foo(a, b=2, c=3, /):`<br />&nbsp;&nbsp;&nbsp;&nbsp;`...`<br /><br />`foo(1, 2) # pos only because of /`
| `function foo(;a=1, b, c=3)`<br />&nbsp;&nbsp;&nbsp;&nbsp;`...`<br />`end`<br /><br />`foo(c=30, b=2) # keyword only` | `def foo(*, a=1, b, c=3):`<br />&nbsp;&nbsp;&nbsp;&nbsp;`...`<br /><br />`foo(c=30, b=2) # kw only because of *`
| `function foo(a, b=2; c=3, d)`<br />&nbsp;&nbsp;&nbsp;&nbsp;`...`<br />`end`<br /><br />`foo(1; d=4) # pos only; then keyword only` | `def foo(a, b=2, /, *, c=3, d):`<br />&nbsp;&nbsp;&nbsp;&nbsp;`...`<br /><br />`foo(1, d=4) # pos only then kw only`
| `function foo(a, b=2, c...)`<br />&nbsp;&nbsp;&nbsp;&nbsp;`...`<br />`end`<br /><br />`foo(1, 2, 3, 4) # positional only` | `def foo(a, b=2, /, *c):`<br />&nbsp;&nbsp;&nbsp;&nbsp;`...`<br /><br />`foo(1, 2, 3, 4) # positional only`
| `function foo(a, b=1, c...; d=1, e, f...)`<br />&nbsp;&nbsp;&nbsp;&nbsp;`...`<br />`end`<br /><br />`foo(1, 2, 3, 4, e=5, x=10, y=20)`<br /> | `def foo(a, b=1, /, *c, d=1, e, **f):`<br />&nbsp;&nbsp;&nbsp;&nbsp;`...`<br /><br />`foo(1, 2, 3, 4, e=5, x=10, y=20)`


## Anonymous functions

|Julia|Python
|-----|------
|`x -> x^2` | `lambda x: x**2`
|`(x,y) -> x + y` | `lambda x,y: x + y `
|`() -> println("yes")` | `lambda: print("yes")`


