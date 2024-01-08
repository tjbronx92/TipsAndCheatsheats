# Scalling w/ Genrators Examples

### Wrong Way ❌
- The entire *squares* list must be populated in the fetch_squares function before the FOR LOOP can print the *square* variable. 
- The larger the list, the more memory is hogged.

```python
def fetch_squares(max_num):
    squares = []
    for n in range(max_num):
        squares.append(n**2)
    return squares

MAX = 5

for square in fetch_squares(MAX):
    print(square)
```

### Better Way ✅ 
```python
def gen_sq(max_num):
    for num in range(max_num):
        yield num ** 2

MAX = 15

for square in gen_sq(MAX):
    print(square)
```

 