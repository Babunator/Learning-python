### type() 
- The type() function returns the type of the specified object
- type(object, bases, dict)
  - object	Required. If only one parameter is specified, the type() function returns the type of this object
  - bases	Optional. Specifies the base classes
  - dict	Optional. Specifies the namespace with the definition for the class

### range() 
- The range() function returns a sequence of numbers, starting from 0 by default, and increments by 1 (by default), and stops before a specified number.
- range(start, stop, step)
  - start	Optional. An integer number specifying at which position to start. Default is 0
  - stop	Required. An integer number specifying at which position to stop (not included).
  - step	Optional. An integer number specifying the incrementation. Default is 1 

### len()
- The len() function returns the number of items in an object.
- When the object is a string, the len() function returns the number of characters in the string.
- len(object)
  - object	Required. An object. Must be a sequence or a collection
  - 
### del 
- The del keyword is used to delete objects. In Python everything is an object, so the del keyword can also be used to delete variables, lists, or parts of a list etc.

### index
- The index() method returns the position at the first occurrence of the specified value. (e.g. in lists, strings...)
- list.index(elmnt)
  - elmnt	Required. Any type (string, number, list, etc.). The element to search for
- string.index(value, start, end)
  -  value	Required. The value to search for
  -  start	Optional. Where to start the search. Default is 0
  -  end	Optional. Where to end the search. Default is to the end of the string

## Stirng Methods

### split()
- The split() method splits a string into a list. You can specify the separator, default separator is any whitespace.
- string.split(separator, maxsplit)
  - separator	Optional. Specifies the separator to use when splitting the string. By default any whitespace is a separator
  - maxsplit	Optional. Specifies how many splits to do. Default value is -1, which is "all occurrences". Note: When maxsplit is specified, the list will contain the specified number of elements plus one.
  
### lower() , upper()
- The  method returns a string where all characters are lower / upper case. Symbols and Numbers are ignored.
- string.lower() / string.upper()

### center() , ljust() , rjust()
- The center() method will center align the string, using a specified character (space is default) as the fill character.
- The ljust()/rjust() method will left/right align the string, using a specified character (space is default) as the fill character.
- string.center(length, character)
  - length	Required. The length of the returned string
  - character	Optional. The character to fill the missing space on each side. Default is " " (space)

### count()
- The count() method returns the number of times a specified value appears in the string.
- string.count(value, start, end)
  - value	Required. A String. The string to value to search for
  - start	Optional. An Integer. The position to start the search. Default is 0
  - end	Optional. An Integer. The position to end the search. Default is the end of the string

## List Methods

### append()
- The append() method appends an element to the end of the list.
- list.append(elmnt)
  -  elmnt	Required. An element of any type (string, number, object etc.)

### insert()
- The insert() method inserts the specified value at the specified position.
- list.insert(pos, elmnt)
  - pos	Required. A number specifying in which position to insert the value
  - elmnt	Required. An element of any type (string, number, object etc.)

### pop()
- The pop() method removes the element at the specified position.
- list.pop(pos)
- pos	Optional. A number specifying the position of the element you want to remove, default value is -1, which returns the last item

### remove()
- The remove() method removes the first occurrence of the element with the specified value.
- list.remove(elmnt)
  - elmnt	Required. Any type (string, number, list etc.) The element you want to remove

### clear()
- The clear() method removes all the elements from a list.
- list.clear()

### sort() 
- The sort() method sorts the list ascending by default. You can also make a function to decide the sorting criteria(s).
- list.sort(reverse=True|False, key=myFunc)
  - reverse	Optional. reverse=True will sort the list descending. Default is reverse=False
  - key	Optional. A function to specify the sorting criteria(s)

### count()
- The count() method returns the number of elements with the specified value.
- list.count(value)
  - value	Required. Any type (string, number, list, tuple, etc.). The value to search for.

## Set Methods 
![alt_text](https://i.imgur.com/8nINiKJ.png)

### add()
- the add() method adds an element to the set.
- If the element already exists, the add() method does not add the element.
- set.add(elmnt)

### remove() / discard()
- The remove() method removes the specified element from the set.
- This method is different from the discard() method, because the remove() method will raise an error if the specified item does not exist, and the discard() method will not.
- set.remove(item) / set.discard(value)

### pop()
- The pop() method removes a random item from the set.
- This method returns the removed item.
- set.pop()

### clear()
- The clear() method removes all the elements from a set.
- set.clear()

### union()
- The union() method returns a set that contains all items from the original set, and all items from the specified set(s). You can specify as many sets you want, separated by commas.
- It does not have to be a set, it can be any iterable object.
- set.union(set1, set2...)

### intersection()
- The intersection() method returns a set that contains the similarity between two or more sets.
- Meaning: The returned set contains only items that exist in both sets, or in all sets if the comparison is done with more than two sets.
- set.intersection(set1, set2 ... etc)

### difference() 
- The difference() method returns a set that contains the difference between two sets.
- Meaning: The returned set contains items that exist only in the first set, and not in both sets.
- set.difference(set)

### issubset()
- The issubset() method returns True if all items in the set exists in the specified set, otherwise it retuns False.
- set.issubset(set)

## Dictionaries Methods

### keys()
- The keys() method returns a view object. The view object contains the keys of the dictionary, as a list.
- The view object will reflect any changes done to the dictionary.
- dictionary.keys()

### values()
- The values() method returns a view object. The view object contains the values of the dictionary, as a list.
- The view object will reflect any changes done to the dictionary.
- dictionary.values()

## items()
- The items() method returns a view object. The view object contains the key-value pairs of the dictionary, as tuples in a list.
- The view object will reflect any changes done to the dictionary.
- dictionary.items()

## get()
- The get() method returns the value of the item with the specified key.
- dictionary.get(keyname, value)
