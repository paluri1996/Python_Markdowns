---
Title: python comprehensions
Keywords: python comprehensions, zip function
Author: Rakesh Reddy Paluri
---

# Python Comprehensions 
* Python comprehensions, are shourtcut syntactic constructs that are
  used with sets, lists and dictionaries
* They can be used to create new lists / dicts from existing lists, based on 
  some calculations, filters.

## Apply calculations on Lists and Dicts
* Python comprehensions enable us to perform calculations on Lists and Dicts
  to generete new lists and dicts.

## Generate New Lists / Dicts based on calculations


```
# Generate list with squares 
list_1 = [5, 6, 7]
# list comprehension
squared_list = [c**2 for c in list_1]
print(squared_list)

# output :[25, 36, 49]
```
```
# Generate new dict by adding 5 to every value of the dict
list_1 = [5, 6, 7]
add5_dict = {c:c+5 for c in list_1}
print(add5_dict)

# output: {5: 10, 6: 11, 7: 12}
```


## Apply Filters and Calculations on Lists and Dicts
* Python comprehensions enable us to filter elements of list and perform 
  calculations on Lists and Dicts, to generete new lists and dicts.

* Generate New Lists / Dicts based on filters
* Generate new list from the current list after adding 5 to the "even" 

```
# elements of the 
list_2 = [2, 3, 4, 5]
even_add5_list = [c+5 for c in list_2 if c%2 == 0]
print(even_add5_list)
# output: [7 ,9]
```
```
squared_dict = {c:c+5 for c in list_2 if c%2 != 0}
print(squared_dict)
# output {11: 121, 3: 9 , 5: 25 , 7: 49}
```
```
## Parallel Iterators using zip function
* Apply Comprehensions on multiple lists
* Converts TWO lists into list of pairs of tuples
* Using loop to Convert lists using zip
```

# Combine multiple Lists to a single list

## Combine sum of multiple lists into a single list
list_a = [1, 2, 3]
list_b = [4, 5, 6]

## Parallel Iteration using ZIP function
```
list_a = [1, 2, 3]
list_b = [4, 5, 6]
list_c = [(x + y) for (x,y) in zip(list_a, list_b)]
print(list_c)
# OUTPUT: [5, 7, 9]
```


## Create a Dict
keys = [1,2,3,4,5]
values = ['a','b','c','d','e']
```
## Create List of Tuples with list and zip
keys = [1,2,3,4,5]
values = ['a','b','c','d','e']
L1 = list(zip(keys,values))
print(L1)
# OUTPUT: [(1, 'a'), (2, 'b'), (3, 'c'), (4, 'd'), (5, 'e')]
```
```
# Create Dictionary with dict and zip
keys = [1,2,3,4,5]
values = ['a','b','c','d','e']
D1 = dict(zip(keys,values))
print(D1)
# OUTPUT: {1: 'a', 2: 'b', 3: 'c', 4: 'd', 5: 'e'}
```
```
# Dictionary Comprehension using loop and zip
keys = [1,2,3,4,5]
values = ['a','b','c','d','e']
D2 = dict(zip([x for x in 'abcdefg'], range(8)))
print(D2)
# OUTPUT: {'a': 0, 'b': 1, 'c': 2, 'd': 3, 'e': 4, 'f': 5, 'g': 6}
```
```
# Dictionary Comprehension using loop and zip
keys = [1,2,3,4,5]
values = ['a','b','c','d','e']
D3 = { k:v for(k,v) in zip(keys, values)}
print(D3)
# OUTPUT: {1: 'a', 2: 'b', 3: 'c', 4: 'd', 5: 'e'}
```