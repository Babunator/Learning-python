# What is Object Oriented Programming
Object Oriented Programming (`OOP`) allows to create their own objects that have methods and attributes.\
Recall that after defining a `objeact` (list, string,... ) with `.methode_name()` syntax.\
These `methods` act as functions that use information about the `object`, as well as the `object` itself to return results, ro change the current `object`.\
Allows to create code that is repetable and organized.\
\
##  Class
A `Class` is a blueprint for objects.It can contain methods (functions) and attributes.\
An `instance` or `object` they are constructed from a class blueprint that contains their class methods and properties.\
By convention we give classes a name that starts with a capital letter.
```python3
# Create a new object type called Sample
class Sample:
    pass
``` 
\
For example, we can create a `class` called Dog. An `attribute` of a dog may be its breed or its name, while a `method` of a dog may be defined by a .bark() method which returns a sound.\
\
## Attributes
The syntax for creating an attribute is:\
```python3
self.attribute = something
``` 
\
There is a special method called:
```python3
__init__()
``` 
\
This method is used to initialize the attributes of an object. For example:
```python3
class Dog:
    def __init__(self,breed):
        self.breed = breed
        
sam = Dog(breed='Lab')
frank = Dog(breed='Huskie') 
```

Here:
`method` 
```python3
__init__() 
``` 
is 
```python3
def __init__(self, breed):
```
\
is called automatically right after the `object` has been created:
```python3
self.breed = breed
```
\
access these attributes like this:
```python3
sam.breed
```
\
In Python there are also class object attributes and theyare the same for any instance of the class. For example, we could create the attribute species for the Dog class. Dogs, regardless of their breed, name, or other attributes, will always be mammals.
```python3
class Dog:
    
    # Class Object Attribute
    species = 'mammal'
    
    def __init__(self,breed,name):
        self.breed = breed
        self.name = name

sam = Dog('Lab','Sam')  
sam.name
# 'Sam'

sam.species
# 'mammal'
```
\
## Methods
Methods are functions defined inside the body of a class. 
They are used to perform operations with the attributes of our objects.\
You can basically think of methods as functions acting on an Object that take the Object itself into account through its *self* argument.\
E.g.
```python3
class Circle:
    pi = 3.14

    # Circle gets instantiated with a radius (default is 1)
    def __init__(self, radius=1):
        self.radius = radius 
        self.area = radius * radius * Circle.pi

    # Method for resetting Radius
    def setRadius(self, new_radius):
        self.radius = new_radius
        self.area = new_radius * new_radius * self.pi

    # Method for getting Circumference
    def getCircumference(self):
        return self.radius * self.pi * 2


c = Circle()

print('Radius is: ',c.radius)
print('Area is: ',c.area)
print('Circumference is: ',c.getCircumference())
```
\
In the _init_ method above, in order to calculate the area attribute, we had to call Circle.pi.
This is because the object does not yet have its own .pi attribute, so we call the Class Object Attribute pi instead.\
\
## Inheritance
Inheritance is a way to form new classes using classes that have already been defined. The newly formed classes are called derived classes.\
Important benefits of inheritance are code reuse and reduction of complexity of a program. The derived classes (descendants) override or extend the functionality of base classes (ancestors).
```python3
class Animal:
    def __init__(self):
        print("Animal created")

    def whoAmI(self):
        print("Animal")

    def eat(self):
        print("Eating")


class Dog(Animal):
    def __init__(self):
        Animal.__init__(self)
        print("Dog created")

    def whoAmI(self):
        print("Dog")

    def bark(self):
        print("Woof!")

```

```python3
d = Dog()
# Animal created
# Dog created

d.whoAmI()
# Dog
d.eat()
# Eating
d.bark()
# Woof!
```
The Animal is the base class, the Dog is the derived class.\
The derived class inherits the functionality of the base class.\
- It is shown by the eat() method.
The derived class modifies existing behavior of the base class.\
- shown by the whoAmI() method.
Finally, the derived class extends the functionality of the base class, by defining a new bark() method.\
\
## Polymorphism
We've learned that while functions can take in different arguments, methods belong to the objects they act on. In Python, polymorphism refers to the way in which different object classes can share the same method name, and those methods can be called from the same place even though a variety of different objects might be passed in. \
```python3
class Dog:
    def __init__(self, name):
        self.name = name

    def speak(self):
        return self.name+' says Woof!'
    
class Cat:
    def __init__(self, name):
        self.name = name

    def speak(self):
        return self.name+' says Meow!' 
    
niko = Dog('Niko')
felix = Cat('Felix')

print(niko.speak())
print(felix.speak())
# Niko says Woof!
# Felix says Meow!
```
\
Another is with functions:
```python3
def pet_speak(pet):
    print(pet.speak())

pet_speak(niko)
pet_speak(felix)
# Niko says Woof!
# Felix says Meow!
```
\
In both cases we were able to pass in different object types, and we obtained object-specific results from the same mechanism.

A more common practice is to use abstract classes and inheritance. An abstract class is one that never expects to be instantiated. For example, we will never have an Animal object, only Dog and Cat objects, although Dogs and Cats are derived from Animals:
```python3
class Animal:
    def __init__(self, name):    # Constructor of the class
        self.name = name

    def speak(self):              # Abstract method, defined by convention only
        raise NotImplementedError("Subclass must implement abstract method")


class Dog(Animal):
    
    def speak(self):
        return self.name+' says Woof!'
    
class Cat(Animal):

    def speak(self):
        return self.name+' says Meow!'
    
fido = Dog('Fido')
isis = Cat('Isis')

print(fido.speak())
print(isis.speak())
```
Real life examples of polymorphism include:
- opening different file types - different tools are needed to display Word, pdf and Excel files
- adding different objects - the + operator performs arithmetic and concatenation
\
# Special Methods
lasses in Python can implement certain operations with special method names. These methods are not actually called directly but by Python specific language syntax.
```python3
class Book:
    def __init__(self, title, author, pages):
        print("A book is created")
        self.title = title
        self.author = author
        self.pages = pages

    def __str__(self):
        return "Title: %s, author: %s, pages: %s" %(self.title, self.author, self.pages)

    def __len__(self):
        return self.pages

    def __del__(self):
        print("A book is destroyed")
```
```python3
book = Book("Python Rocks!", "Jose Portilla", 159)

#Special Methods
print(book)
print(len(book))
del book
# A book is created
# Title: Python Rocks!, author: Jose Portilla, pages: 159
# 159
# A book is destroyed
```
The __init__(), __str__(), __len__() and __del__() methods\
These special methods are defined by their use of underscores. They allow us to use Python specific functions on objects created through our class.
