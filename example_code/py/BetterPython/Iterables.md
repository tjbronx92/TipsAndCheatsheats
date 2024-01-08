# Iterables

![image](/img/cartman.gif "Dogma")

Notes on working with iterables.

### Check if an object is iterable by passing object to iter().

Tuple: `tuple_iterator object`
```python
TupleObj = mytuple = ("Jay", "Mary", "Greta")
TupleObj_iter = iter(TupleObj)
print(TupleObj_iter)

# OUTPUT: <tuple_iterator object at 0x12aa591e0>
```


String: `str_ascii_iterator object`
```python
stringObj = 'The quick brown fox jumps over the lazy dog'
stringObj_iter = iter(stringObj)

for char in stringObj_iter:
    print(char)
```

Dictionary: `dict_keyiterator object`
```python
countryCapitals = {
  "United States": "Washington D.C.", 
  "Jamaica": "Kingston", 
  "England": "London"
}

countryCapitals_iter = iter(countryCapitals)

for key in countryCapitals_iter:
    print(key)
```