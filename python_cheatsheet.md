<!--TODO:
    Add advance guides for lists such has comprehensions.
 -->

# PYTHON BUILT-IN DATA STRUCTURES CHEAT SHEET

## LISTS

### List Declaration

Lists are a way of storing multiple elements of data. Lists are one of many iterables.

Lists can store data of any type and even contain multiple different types of data.

Lists are mutable meaning they ***can*** be changed after they are created.

Lists are represented inside square brackets []

Examples:

```python
my_list = []                    #Empty list.                             my_list: []

my_list = list()                #Empty list.                             my_list: []

my_list = [1,2,3,4]             #List of ints.                           my_list: [1,2,3,4]

my_list = ["hello", "world"]    #List of strings.                        my_list: ["hello", "world"]

my_list= ["hello", 1234]        #List of strings and ints.               my_list: ["hello", 1234]

my_list = [[1,2,3],[4,5,6]]     #List of lists.                          my_list: [[1,2,3],[4,5,6]]
```

### List Indexing/Subscripting

Lists are zero indexed which means the first element in the list can be found at index 0.
Using negative integers to index a list will start from the end of the list instead of the front.
The end of the list is found at index -1 because -0 is not a valid integer.

The syntax of indexing a list is as follows: list_name[index]

The square brackets [] appended to the name of a data structure is known as subscript notation.
Subscript notation is used by many built-in data structures.

Trying to index a list at an index outside the size of the list will result in a index out of range error.

Examples:

```python
my_list = ["a","b","c"]         #Declares an example list.               my_list: ["a","b","c"]

print(my_list)                  #Prints my_list to screen.               ["a","b","c"]

print(my_list[1])               #Prints index 1 of my_list.              "b"

first = my_list[0]              #Indexes my_list at 0.                   first: "a"

second = my_list[1]             #Indexes my_list at 1.                   second: "b"

third = my_list[2]              #Indexes my_list at 2.                   third: "c"

end = my_list[-1]               #Indexes my_list at the end. -1.         end: "c"

2nd_from_end =  my_list[-2]     #Indexes my_list at 2nd from end.        2nd_from_end: "b"

outside_list = my_list[3]       #Indexes my_list at 3.                   IndexError: list index out of range

outside_list = my_list[-4]      #Indexes my_list at -4.                  IndexError: list index out of range
```

### List Methods

Methods are functions that are built-into classes. The list data structure has many useful methods.

General syntax of list methods is as follows: list_name.method_name()

Examples:

```python
my_list = [1,2,3,4,99]          #Declares an example list.               my_list: [1,2,3,4,99]

my_list.append(5)               #Appends a value to the end of a list.   my_list: [1,2,3,4,99,5]

my_list.append([5,6,7])         #Appends a list to a list.               my_list: [1,2,3,4,99,[5,6,7]]

my_list.append("hey")           #Appends a string to a list              my_list: [1,2,3,4,99,"hey"]

my_list.extend([5,6,7])         #Appends iterable elements to a list.    my_list: [1,2,3,4,99,5,6,7]

my_list.extend("hey")           #Appends iterable elements to a list.    my_list: [1,2,3,4,99,'h','e','y']

my_list.insert(0, 40)           #Insert syntax: insert(index, value).    my_list: [40,1,2,3,4,99]

my_list.pop(0)                  #Removes element at index supplied.      my_list: [2,3,4,99]

my_list.remove(99)              #Removes element by value, not index.    my_list: [1,2,3,4]

my_list.reverse()               #Reverses order of list.                 my_list: [99,4,3,2,1]

my_list.sort()                  #Sorts a list from least to greatest.    my_list: [1,2,3,4,99]

my_list.sort(reverse = True)    #Sorts a list from greatest to least.    my_list: [99,4,3,2,1]

new_list = my_list.copy()       #Returns a copy of a list.               new_list: [1,2,3,4,99]

elements = my_list.count()      #Returns number of elements in a list.   elements: 5

index = my_list.index(99)        #Returns the index of a list element.    index: 4
```

## TUPLES

### Tuple Declaration

Similarly to lists, tuples let you store multiple elements of data. Like lists, tuples are iterables.

Tuples can store data of any type and even contain multiple different types of data.

Tuples are immutable meaning they ***can not*** be changed after they are created.

Tuples are represented inside parentheses () but you can declare them without them.

Examples:

```python
my_tuple = ()                   #Empty tuple.                            my_tuple: ()

my_tuple = tuple()              #Empty tuple.                            my_tuple: ()

my_tuple = (1)                  #This is an int, not a tuple.            my_tuple: 1

my_tuple = (1,)                 #This is a tuple with 1 element.         my_tuple: (1,)

my_tuple = (1,2,3,4)            #Tuple of ints.                          my_tuple: (1,2,3,4)

my_tuple = 1,2,3,4              #Tuple of ints.                          my_tuple: (1,2,3,4)

my_tuple = ("hello", "world")   #Tuple of strings.                       my_tuple: ("hello", "world")

my_tuple = "hello", "world"     #Tuple of strings.                       my_tuple: ("hello", "world")

my_tuple = ("hello", 1234)      #Tuple of strings and ints.              my_tuple: ("hello", 1234)

my_tuple = "hello", 1234        #Tuple of strings and ints.              my_tuple: ("hello", 1234)

my_tuple = ((1,2,3),(4,5,6))    #Tuple of tuples.                        my_tuple: ((1,2,3),(4,5,6))

my_tuple = (1,2,3),(4,5,6)      #Tuple of tuples.                        my_tuple: ((1,2,3),(4,5,6))
```

### Tuple Indexing/Subscripting

Tuples are zero indexed just like lists. The first element in the tuple is found at index 0.
Using negative integers to index a tuple will start from the end of the tuple instead of the front.
The end of the tuple is found at index -1 because -0 is not a valid integer.

The syntax of indexing a tuple is as follows: tuple_name[index]

The square brackets [] appended to the name of a data structure is known as subscript notation.
Subscript notation is used by many built-in data structures.

Trying to index a tuple at an index outside the size of the tuple will result in a index out of range error.

Examples:

```python
my_tuple = ("a","b","c")        #Declares an example tuple.              my_tuple: ("a","b","c")

print(my_tuple)                 #Prints my_tuple to screen.              ("a","b","c")

print(my_tuple[1])              #Prints index 1 of my_tuple.             "b"

first = my_tuple[0]             #Indexes my_tuple at 0.                  first: "a"

second = my_tuple[1]            #Indexes my_tuple at 1.                  second: "b"

third = my_tuple[2]             #Indexes my_tuple at 2.                  third: "c"

end = my_tuple[-1]              #Indexes my_tuple at the end. -1.        end: "c"

2nd_from_end =  my_tuple[-2]    #Indexes my_tuple at 2nd from the end.   2nd_from_end: "b"

outside_tuple = my_tuple[3]     #Indexes my_tuple at 3.                  IndexError: tuple index out of range

outside_tuple = my_tuple[-4]    #Indexes my_tuple at -4.                 IndexError: tuple index out of range
```

### Tuple Methods

Methods are functions that are built-into classes. Tuples don't have many because tuples can't be changed.

General Syntax of tuple methods is as follows: tuple_name.method_name()

Examples:

```python
my_tuple = (1,2,3,4,99)         #Declares an example tuple.              my_tuple: (1,2,3,4,99)

elements = my_tuple.count()     #Returns number of elements in a tuple.  elements: 5

index = my_tuple.index(99)      #Returns the index of a tuple element.   index: 4
```

## DICTIONARIES

### Dictionary Declaration

Dictionaries are used for storing key-value pairs.

Dictionaries are mutable meaning they ***can*** be changed after they are created.

Dict is short for dictionary.

Dictionaries are represented in curly brackets {}.

Examples:

```python
my_dict = {}                    #Empty dict.                             my_dict: {}

my_dict = dict()                #Empty dict.                             my_dict: {}

my_dict = {"apples": 1}         #Dict with key-value apples and 1.       my_dict: {"apples": 1}

my_dict = {"hat": 2, "cat": 5}  #Dict with 2 key-value pairs.            my_dict: {"hat":2, "cat": 5}
```

Hard coded dictionaries can take a lot of space. You can declare them on many lines with the following syntax:

```python
my_dict = {
    "username1": "birdman",
    "username2": "hammy",
    "secret": 42,
    1: 2,
    2: "two",
    1.5: "float"
    }
```

You can get creative with the keys in dictionaries but don't make it confusing.

### Dictionary Key Subscripting

Dictionaries are an unordered data structure, unlike lists and tuples which are ordered.

To access data from a dictionary, you use the subscript notion and supply the key. You you will get the value stored with that key in return.

The syntax of retrieving data from a dictionary is dict_name[key_name]

The square brackets [] appended to the name of a data structure is known as subscript notation.
Subscript notation is used by many built-in data structures.

Trying to access a dictionary with a key that is not in the dictionary results in a KeyError.

Examples:

```python
my_dict = {'f_name': 'john', 'l_name': 'smith', 'age', 30}               #Declares an example dictionary

print(my_dict['f_name'])        #Prints value of key 'f_name'            'john'

print(my_dict['l_name'])        #Prints value of key 'l_name'            'smith'

print(my_dict['age'])           #Prints value of key 'age'               30

f_name = my_dict['f_name']      #Retrieves value of key 'f_name'         f_name: 'john'
```

### Dictionary Methods

Methods are functions that are built-into classes. The dictionary data structure has many useful methods.

General syntax of dictionary methods is as follows: dict_name.method_name()

Examples:

```python
#Declares an example dictionary
my_dict = {'name': 'smith', 'age': 3, 'height': 12, 'weight': 48}

#Get works like the subscripting method but will not throw an error if key is not in the dictionary
result = my_dict.get('name')
#                               result: 'smith'

#Get works like the subscripting method but will not throw an error if key is not in the dictionary
result = my_dict.get('not_in')
#                               result: None

#Searches for a key, if it is found, the value is returned, otherwise the key is added with a default value.
#Usage dict.setdefault(key, default_value)
result = my_dict.setdefault('name')
#                               result: 'smith'

#Searches for a key, if it is found, the value is returned, otherwise the key is added with a default value.
#Usage dict.setdefault(key, default_value)
result = my_dict.setdefault('hat')
#                               result: None
#                               my_dict: {'name': 'smith', 'age': 3, 'height': 12, 'weight': 48, 'hat': None}

#Searches for a key, if it is found, the value is returned, otherwise the key is added with a default value.
#Usage dict.setdefault(key, default_value)
result = my_dict.setdefault('hat', 'Yes')
#                               result: None
#                               my_dict: {'name': 'smith', 'age': 3, 'height': 12, 'weight': 48, 'hat': 'Yes'}

#Adds or updates elements in the dict. Usage is dict_name.update(dictionary)
my_dict.update({'new': 10})
#                               my_dict: {'name': 'smith', 'age': 3, 'height': 12, 'weight': 48, 'new': 10}

#Adds or updates elements in the dict. Usage is dict_name.update(dictionary)
my_dict.update({'name': 'john'})
#                               my_dict: {'name': 'john', 'age': 3, 'height': 12, 'weight': 48}

#Removes key value pair from dict based on supplied key and returns value of key.
removed = my_dict.pop('name')
#                               removed: 'smith'
#                               my_dict: {'age': 3, 'height': 12, 'weight': 48}

#Removes the most recent key-value pair that had been added to the dictionary and returns the pair as a tuple.
removed = my_dict.popitem()
#                               removed: ('weight': 48)
#                               my_dict: {'name': 'smith', 'age': 3, 'height': 12}

#The fromkeys method returns a dictionary so we use the dict keyword as the dict we are calling the method on.
#The fromkeys method does not modify the dictionary it is called on.
#Usage is dict.fromkeys(iterable_data, default_value) if no default value is supplied, None will be the default.
new_dict = dict.fromkeys([1,2,3,4], 'Default')
#                               new_dict = {1: 'Default', 2: 'Default', 3: 'Default', 4: 'Default'}

my_dict.clear()                 #Removes all elements from the dict      my_dict: None
```