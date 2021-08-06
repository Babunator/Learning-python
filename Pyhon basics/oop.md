# What is Object Oriented Programming
Object Oriented Programming (`OOP`) allows to create their own objects that have methods and attributes.\
Recall that after defining a `objeact` (list, string,... ) with `.methode_name()` syntax.\
These `methods` act as functions that use information about the `object`, as well as the `object` itself to return results, ro change the current `object`.\
Allows to create code that is repetable and organized.\

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
``` is 
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

```
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
