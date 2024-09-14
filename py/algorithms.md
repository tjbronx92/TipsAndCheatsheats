# Algorithms

![image](/img/charlie-day.gif "Connect The Dots")

Notes on writing more efficient algorithms.

Selection Sort
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

Recursion
```python

```

Quicksort
```python

```

---
References:

<sup>1</sup> ["Grokking Algorithms" -by Aditya Y. Bhargava](https://www.manning.com/books/grokking-algorithms?ar=false&lpse=B)
