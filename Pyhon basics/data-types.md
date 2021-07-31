# Python Data Types
##Numeric classes
* int : It's an integer like 5,3,4
* float: a data type composed of a number that is not an integer, because it includes a fraction represented in decimal format. 1.2, 2.55
* Int and float can use standard arithmetic operations, +, -, *, /, and ** (exponentiation). Other very useful operations are the remainder (modulo) operator, %, and integer division, //. 

## Boolean classes
* Bool: True or False values (often used with relational and logical operators)
![alt_text](https://i.imgur.com/SwrD4n3.png)


## Collection Data Types
### ordered sequence
* list : It's an ordered sequence of different data types for example ['1','apple','10.5']
  * lists are heterogeneous, meaning that the data objects need not all be from the same class 
- Since lists are considered to be sequentially ordered, they support a number of operations that can be applied to any Python sequence:
![alt_text](https://i.imgur.com/WCfnH0l.png)
- Note that the indices for lists (sequences) start counting with 0. The slice operation, myList[1:3], returns a list of items starting with the item indexed by 1 up to but not including the item indexed by 3.


- str: Strings are sequential collections of zero or more letters, numbers and other symbols. Called characters
- A major difference between lists and strings is that lists can be modified while strings cannot. This is referred to as mutability. Lists are mutable; strings are immutable. For example, you can change an item in a list by using indexing and assignment. With a string that change is not allowed.

* tuple : It's an immutable ordered sequence of different data types: ('1', 'apple', '10.5')

### unordered sequence
* dict : It's a collection of key value pairs {'name':'john'}
![alt_text](https://i.imgur.com/BqQ7ZOn.png)
* set : It's a collection of unique data: {1, 'apple', 10.5}. Sets do not allow duplicates
* frozenset : It's an immutable collection of unique data: frozenset({1, 'apple', 10.5})

##### Examples
```Python 
x = true # Boolean
y = "Hello World" # This is a string
numbers = [1, 2, 3, 'four'] # this is a list
letters = ('a', 'b', 'c', 'd') # this is a tuple
v = {
    'name':'john',
    'address':'xyz street'
} # Its a dictionary in python

my_set = {1, 'apple', 10.5} # this is a set
my_set.add('banana') # this adds 'banana' to my set : my_set = {1, 'apple', 10.5, 'banana'}
my_set.add('apple') # this won't add nothing because apple is already in the set
my_set.remove('apple') # this removes 'apple' from the set: my_set = {1, 10.5, 'banana'}

my_frozen_set = frozenset(my_set) # this freezes my_set
```

##### Important Note
* Python is dynamically typed language it means that variable can be changed readily but its different in languages like JAVA, C++ C or etc where we have to specify the variable type thats why they are called statically typed languages
* **None Key Word in Python is just like Null**
* **We can use type() Function to see the data type**
