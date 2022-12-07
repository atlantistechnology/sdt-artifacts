---
author: Nikita Denissov
date: November 7, 2022
thread: [Guide to syntax changes by Python version?](https://discuss.python.org/t/guide-to-syntax-changes-by-python-version/20715/22)
---

 **3.11**
* [PEP 654: Exception Groups and except*](https://docs.python.org/3.12/whatsnew/3.11.html#whatsnew311-pep654)
* [PEP 646: Variadic generics](https://peps.python.org/646)

**3.10**
* [**PEP 634**](https://peps.python.org/pep-0634/), Structural Pattern Matching: Specification
* [**PEP 635**](https://peps.python.org/pep-0635/), Structural Pattern Matching: Motivation and Rationale
* [**PEP 636**](https://peps.python.org/pep-0636/), Structural Pattern Matching: Tutorial
* [bpo-12782](https://bugs.python.org/issue?@action=redirect&bpo=12782), Parenthesized context managers are now officially allowed.

**3.9**
* [**PEP 584**](https://peps.python.org/pep-0584/), union operators added to `dict`;
* [**PEP 585**](https://peps.python.org/pep-0585/), type hinting generics in standard collections;
* [**PEP 614**](https://peps.python.org/pep-0614/), relaxed grammar restrictions on decorators.

**3.8**
* [**PEP 572**](https://peps.python.org/pep-0572/) Assignment expressions (`:=`)
* [**PEP 570**](https://peps.python.org/pep-0570/) Positional-only parameters (`def quantiles(dist, /, n=4, *, method='exclusive')`)
* [f-strings support `=`](https://docs.python.org/3.12/whatsnew/3.8.html#f-strings-support-for-self-documenting-expressions-and-debugging) (`f'{user=} {member_since=}'`)
* A [`continue`](https://docs.python.org/3.12/reference/simple_stmts.html#continue) statement was illegal in the [`finally`](https://docs.python.org/3.12/reference/compound_stmts.html#finally) clause due to a problem with the implementation. In Python 3.8 this restriction was lifted. (Contributed by Serhiy Storchaka in [bpo-32489](https://bugs.python.org/issue?@action=redirect&bpo=32489).)
* The syntax allowed for keyword names in function calls was further restricted. In particular, `f((keyword)=arg)` is no longer allowed. It was never intended to permit more than a bare name on the left-hand side of a keyword argument assignment term. (Contributed by Benjamin Peterson in [bpo-34641](https://bugs.python.org/issue?@action=redirect&bpo=34641).)

* Generalized iterable unpacking in [`yield`](https://docs.python.org/3.12/reference/simple_stmts.html#yield) and [`return`](https://docs.python.org/3.12/reference/simple_stmts.html#return) statements no longer requires enclosing parentheses. This brings the *yield* and *return* syntax into better agreement with normal assignment syntax:

```python
def parse(family):
        lastname, *members = family.split()
        return lastname.upper(), *members
```

**3.7**
* [PEP 563](https://docs.python.org/3.12/whatsnew/3.7.html#whatsnew37-pep563), postponed evaluation of type annotations.

**3.6**
* [PEP 498](https://docs.python.org/3.12/whatsnew/3.6.html#whatsnew36-pep498), formatted string literals.
* [PEP 515](https://docs.python.org/3.12/whatsnew/3.6.html#whatsnew36-pep515), underscores in numeric literals.
* [PEP 526](https://docs.python.org/3.12/whatsnew/3.6.html#whatsnew36-pep526), syntax for variable annotations.
* [PEP 525](https://docs.python.org/3.12/whatsnew/3.6.html#whatsnew36-pep525), asynchronous generators.
* [PEP 530](https://docs.python.org/3.12/whatsnew/3.6.html#whatsnew36-pep530): asynchronous comprehensions.

**3.5**
* [PEP 492](https://docs.python.org/3.12/whatsnew/3.5.html#whatsnew-pep-492), coroutines with async and await syntax.
* [PEP 465](https://docs.python.org/3.12/whatsnew/3.5.html#whatsnew-pep-465), a new matrix multiplication operator: `a @ b`.
* [PEP 448](https://docs.python.org/3.12/whatsnew/3.5.html#whatsnew-pep-448), additional unpacking generalizations.

**3.4**
* No new syntax features were added in Python 3.4.

**3.3**
* New `yield from` expression for [generator delegation](https://docs.python.org/3.12/whatsnew/3.3.html#pep-380).
* The `u'unicode'` syntax is accepted again for [`str`](https://docs.python.org/3.12/library/stdtypes.html#str) objects.

**3.2**
* Previously it was illegal to delete a name from the local namespace if it occurs as a free variable in a nested block:
```python
def outer(x):
    def inner():
        return x
    inner()
    del x
```
This is now allowed. Remember that the target of an [`except`](https://docs.python.org/3.12/reference/compound_stmts.html#except) clause is cleared, so this code which used to work with Python 2.6, raised a [`SyntaxError`](https://docs.python.org/3.12/library/exceptions.html#SyntaxError) with Python 3.1 and now works again:
```python
def f():
    def print_error():
        print(e)
    try:
        something
    except Exception as e:
        print_error()
        # implicit "del e" here
```
(See [bpo-4617](https://bugs.python.org/issue?@action=redirect&bpo=4617).)

**3.1**
* The syntax of the [`with`](https://docs.python.org/3.12/reference/compound_stmts.html#with) statement now allows multiple context managers in a single statement:
```python
with open('mylog.txt') as infile, open('a.out', 'w') as outfile:
    for line in infile:
        if '<critical>' in line:
            outfile.write(line)
```
With the new syntax, the `contextlib.nested()` function is no longer needed and is now deprecated.(Contributed by Georg Brandl and Mattias Brändström; [appspot issue 53094](https://codereview.appspot.com/53094).)

**3.0**
* [Print Is A Function](https://docs.python.org/3.12/whatsnew/3.0.html#print-is-a-function)
* [**PEP 238**](https://peps.python.org/pep-0238/): An expression like `1/2` returns a float. Use `1//2` to get the truncating behavior. (The latter syntax has existed for years, at least since Python 2.2.)
* You can no longer use `u"..."` literals for Unicode text. However, you must use `b"..."` literals for binary data.
* All backslashes in raw string literals are interpreted literally. This means that `'\U'` and `'\u'` escapes in raw strings are not treated specially. For example, `r'\u20ac'` is a string of 6 characters in Python 3.0, whereas in 2.6, `ur'\u20ac'` was the single “euro” character. (Of course, this change only affects raw string literals; the euro character is `'\u20ac'` in Python 3.0.)
* [**PEP 3131**](https://peps.python.org/pep-3131/): Non-ASCII letters are now allowed in identifiers. (However, the standard library remains ASCII-only with the exception of contributor names in comments.)

* [**PEP 3107**](https://peps.python.org/pep-3107/): Function argument and return value annotations. This provides a standardized way of annotating a function’s parameters and return value. There are no semantics attached to such annotations except that they can be introspected at runtime using the `__annotations__` attribute. The intent is to encourage experimentation through metaclasses, decorators or frameworks.
* [**PEP 3102**](https://peps.python.org/pep-3102/): Keyword-only arguments. Named parameters occurring after `*args` in the parameter list *must* be specified using keyword syntax in the call. You can also use a bare `*` in the parameter list to indicate that you don’t accept a variable-length argument list, but you do have keyword-only arguments.
* Keyword arguments are allowed after the list of base classes in a class definition. This is used by the new convention for specifying a metaclass (see next section), but can be used for other purposes as well, as long as the metaclass supports it.
* [**PEP 3104**](https://peps.python.org/pep-3104/): [`nonlocal`](https://docs.python.org/3.12/reference/simple_stmts.html#nonlocal) statement. Using `nonlocal x` you can now assign directly to a variable in an outer (but non-global) scope. `nonlocal` is a new reserved word.
* [**PEP 3132**](https://peps.python.org/pep-3132/): Extended Iterable Unpacking. You can now write things like `a, b, *rest = some_sequence`. And even `*rest, a = stuff`. The `rest` object is always a (possibly empty) list; the right-hand side may be any iterable. Example:
```python
(a, *rest, b) = range(5)
```
This sets *a* to `0` , *b* to `4` , and *rest* to `[1, 2, 3]`.

* Dictionary comprehensions: `{k: v for k, v in stuff}` means the same thing as `dict(stuff)` but is more flexible. (This is [**PEP 274**](https://peps.python.org/pep-0274/) vindicated. :-)
* Set literals, e.g. `{1, 2}`. Note that `{}` is an empty dictionary; use `set()` for an empty set. Set comprehensions are also supported; e.g., `{x for x in stuff}` means the same thing as `set(stuff)` but is more flexible.
* New octal literals, e.g. `0o720` (already in 2.6). The old octal literals (`0720`) are gone.
* New binary literals, e.g. `0b1010` (already in 2.6), and there is a new corresponding built-in function, [`bin()`](https://docs.python.org/3.12/library/functions.html#bin).
* Bytes literals are introduced with a leading `b` or `B`, and there is a new corresponding built-in function, [`bytes()`](https://docs.python.org/3.12/library/stdtypes.html#bytes).
* [**PEP 3109**](https://peps.python.org/pep-3109/) and [**PEP 3134**](https://peps.python.org/pep-3134/): new [`raise`](https://docs.python.org/3.12/reference/simple_stmts.html#raise) statement syntax: `raise [expr [from expr]]`. See below.
* `as` and [`with`](https://docs.python.org/3.12/reference/compound_stmts.html#with) are now reserved words. (Since 2.6, actually.)
* `True`, `False`, and `None` are reserved words. (2.6 partially enforced the restrictions on `None` already.)
* Change from [`except`](https://docs.python.org/3.12/reference/compound_stmts.html#except) *exc*, *var* to `except` *exc* `as` *var*. See [**PEP 3110**](https://peps.python.org/pep-3110/).
* [**PEP 3115**](https://peps.python.org/pep-3115/): New Metaclass Syntax. Instead of:
```python
class C:
    __metaclass__ = M
    ...
```
you must now use:
```python
class C(metaclass=M):
    ...
```
* The module-global `__metaclass__` variable is no longer supported. (It was a crutch to make it easier to default to new-style classes without deriving every class from [`object`](https://docs.python.org/3.12/library/functions.html#object).)
* List comprehensions no longer support the syntactic form `[... for var in item1, item2, ...]`. Use `[... for var in (item1, item2, ...)]` instead. Also note that list comprehensions have different semantics: they are closer to syntactic sugar for a generator expression inside a [`list()`](https://docs.python.org/3.12/library/stdtypes.html#list) constructor, and in particular the loop control variables are no longer leaked into the surrounding scope.
* The *ellipsis* (`...`) can be used as an atomic expression anywhere. (Previously it was only allowed in slices.) Also, it *must* now be spelled as `...`. (Previously it could also be spelled as `. . .`, by a mere accident of the grammar.)

* [**PEP 3113**](https://peps.python.org/pep-3113/): Tuple parameter unpacking removed. You can no longer write `def foo(a, (b, c)): ...`. Use `def foo(a, b_c): b, c = b_c` instead.
* Removed backticks (use [`repr()`](https://docs.python.org/3.12/library/functions.html#repr) instead).
* Removed `<>` (use `!=` instead).
* Removed keyword: [`exec()`](https://docs.python.org/3.12/library/functions.html#exec) is no longer a keyword; it remains as a function. (Fortunately the function syntax was also accepted in 2.x.) Also note that [`exec()`](https://docs.python.org/3.12/library/functions.html#exec) no longer takes a stream argument; instead of `exec(f)` you can use `exec(f.read())`.
* Integer literals no longer support a trailing `l` or `L`.
* String literals no longer support a leading `u` or `U`.
* The [`from`](https://docs.python.org/3.12/reference/simple_stmts.html#from) *module* [`import`](https://docs.python.org/3.12/reference/simple_stmts.html#import) `*` syntax is only allowed at the module level, no longer inside functions.
* The only acceptable syntax for relative imports is `from .[module] import name`. All [`import`](https://docs.python.org/3.12/reference/simple_stmts.html#import) forms not starting with `.` are interpreted as absolute imports. ([**PEP 328**](https://peps.python.org/pep-0328/))
* Classic classes are gone.

**2.7**
* The syntax for set literals (`{1,2,3}` is a mutable set).
* The new `","` format specifier described in [PEP 378: Format Specifier for Thousands Separator](https://docs.python.org/3.12/whatsnew/2.7.html#pep-0378).
* Dictionary and set comprehensions are another feature backported from 3.x, generalizing list/generator comprehensions to use the literal syntax for sets and dictionaries.
* The [`with`](https://docs.python.org/3.12/reference/compound_stmts.html#with) statement can now use multiple context managers in one statement. Context managers are processed from left to right and each one is treated as beginning a new `with` statement. 
* Extra parentheses in function definitions are illegal in Python 3.x, meaning that you get a syntax error from `def f((x)): pass`. In Python3-warning mode, Python 2.7 will now warn about this odd usage. (Noted by James Lingard; [bpo-7362](https://bugs.python.org/issue?@action=redirect&bpo=7362).)

**2.6**
* Alternate syntax for catching exceptions: `except TypeError as exc`.
* [**PEP 3127**](https://peps.python.org/pep-3127/) - Integer Literal Support and Syntax (*backported*)
* [**PEP 3129**](https://peps.python.org/pep-3129/) - Class Decorators
```python
@foo
@bar
class A:
  pass
```
* It’s also become legal to provide keyword arguments after a *args argument to a function call.

```python
def f(*args, **kw):
    print args, kw
f(1,2,3, *(4,5,6), keyword=13)
```
* Previously this would have been a syntax error. (Contributed by Amaury Forgeot d’Arc; [bpo-3473](https://bugs.python.org/issue?@action=redirect&bpo=3473).)

**2.5**
* [PEP 308: Conditional Expressions](https://docs.python.org/3.12/whatsnew/2.5.html#pep-308)
* [PEP 343: The ‘with’ statement](https://docs.python.org/3.12/whatsnew/2.5.html#pep-343)

**2.4**
* [PEP 318](https://peps.python.org/318) [Decorators for Functions and Methods](https://PEP 318: Decorators for Functions and Methods)
* [`None`](https://docs.python.org/3.12/library/constants.html#None) is now a constant; code that binds a new value to the name `None` is now a syntax error. (Contributed by Raymond Hettinger.)

**2.2 - 2.3**
* [PEP 255](https://peps.python.org/255): Simple Generators [`yield`](https://docs.python.org/3.12/reference/simple_stmts.html#yield) is now always a keyword

**2.1**
```python
x = 1
def f():
    # The next line is a syntax error
    exec 'x=2'
    def g():
        return x
```

**2.0**
* [List Comprehensions](https://docs.python.org/3.12/whatsnew/2.0.html#list-comprehensions)
```python
# Syntax error
[ x,y for x in seq1 for y in seq2]
# Correct
[ (x,y) for x in seq1 for y in seq2]
```
* The full list of [supported assignment operators](https://docs.python.org/3.12/whatsnew/2.0.html#augmented-assignment) is `+=` , `-=` , `*=` , `/=` , `%=` , `**=` , `&=` , `|=` , `^=` , `>>=` , and `<<=` .
* The `print` statement can now have its output directed to a file-like object by following the `print` with `>> file`
```python
print >> sys.stderr, "Warning: action field not supplied"
```
* `f(*args, **kw)` is a shorter and clearer way to achieve the same effect. This syntax is symmetrical with the syntax for defining functions:
* Modules can now be renamed on importing them, using the syntax `import module as name` or `from module import name as othername` . The patch was submitted by Thomas Wouters.