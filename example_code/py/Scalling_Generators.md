# Scalling w/ Genrators Examples

### Wrong Way
```python
def fetch_squares(max_root):
    squares = []
    for n in range(max_root):
        squares.append(n**2)
    return squares

MAX = 5

for square in fetch_squares(MAX):
    print(square)
```
- The entire *squares* list must be populated before for loop can print *square* variable. The larger the list, the more memory is hogged.
 