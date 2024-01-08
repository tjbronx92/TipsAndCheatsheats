# Scalling w/ Genrators Examples

### Wrong Way ❌
- The entire *squares* list must be populated in the fetch_squares function before the FOR LOOP can print the *square* variable. 
- The larger the list, the more memory is hogged.

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

### Better Way ✅ 
```python
def findSmallest(arr):
    smallest = arr[0]
    smallest_index = 0
    for i in range(1, len(arr)):
        if arr[i] < smallest:
            smallest = arr[i]
            smallest_index = i
    return smallest_index

def selectionSort(arr):
    newArr = []
    for i in range(len(arr)):
        smallest = findSmallest(arr)
        newArr.append(arr.pop(smallest))
    
    print(newArr)

selectionSort([8, 5, 1, 777, 11])
```

 