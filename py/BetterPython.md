# Writing Better Python

![image](/img/python.png "ArchPython")

## Tips and tricks to improve Python's performance and readability. 

### Looping over a collection
1. A list is an iterable
2. The FOR loop passes iterables to `iter()` automatically
```python
colors = ['black', 'pink', 'yellow', 'orange']

for color in colors:
    print(color)
```

### Looping Backwards
```python
colors = ['black', 'pink', 'yellow', 'orange']

for color in reversed(colors):
    print(color)
```
---

### Scaling w/ Generators
A function is a generator ***IF AND ONLY IF*** it uses the *YIELD* keyword instead of *RETURN*.
```python
def gen_sq(max_num):
    for num in range(max_num):
        yield num ** 2

MAX = 15

for square in gen_sq(MAX):
    print(square)
```
###### [Scalling w/ Genrators Examples](/example_code/py/BetterPython/Scalling_Generators.md)
---
References:

<sup>1</sup> [[YouTube] Raymond Hettinger Lecture](https://www.youtube.com/watch?v=OSGv2VnC0go&t=3s "Transforming Code into Beautiful, Idiomatic Python")

<sup>2</sup> ["Powerful Python" -by Aaron Maxwell](https://powerfulpython.com/ "The Most Impactful Patterns, Features, and Development Strategies Modern Python Provides")