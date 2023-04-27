## Python OOP Assignment
Q1. What is the purpose of Python's OOP?
- in python oop(object oriented programming) is a paradigm that uses objects and classes in programming.
- it aims to implement real world entities like inheritence, polymorphism, encapsulation, etc in the programs.
- the main goal of oop is to bind data and functions work together as a single entity no other part of code can access this data.

Q2. Where does an inheritance search look for an attribute?
- When searching for an attribute in a class hierarchy, Python first looks for the attribute in the instance object itself. If the attribute is not found there, it looks for the attribute in the class of the instance. If the attribute is still not found in the class, Python searches in the first superclass of the class, then in the superclass of that superclass, and so on. If the attribute is not found in any of the superclasses, Python raises an AttributeError.

Q3. How do you distinguish between a class object and an instance object?
- Class objects define attributes(model,year,price) and methods(functions,methods,init method) that are common to all instances of the class.
- while instance objects have their own unique attributes and can also override class attributes.
class object:
```python
class car:
    pass
```
instance object:
```python
honda=car()
tata=car()
```


Q4. What makes the first argument in a class’s method function special?
- `self` makes the first argument in class's method function speacial
- self refers to instance object that the method is called on
- self gives access to methos to modify attributes of class object's attributes

Q5. What is the purpose of the init method?
- init method is used to initialize attributes of class oject
- when object instance is instantiated then the init method from class object is called and sets initial values of class object's attributes

Q6. What is the process for creating a class instance?
- step 1: creting class
```python
class car():
    pass
```

- step 2: creating object instance of class(class instance)
```python
my_object = MyClass()
```

for example:
```python
class Person: #step 1 : creting class
    def __init__(self, name, age): # method
        self.name = name
        self.age = age

person = Person("John", 25) #step 2: creating object instance of class(class instance)

#accessing instance attributes
print(person.name) # Output: John
print(person.age)  # Output: 25
```


Q7. What is the process for creating a class?
for creating class:
- step 1: define class name using "class" keyword
```python
class my_class:
    pass
```

- step 2: defining methods(init method) and attributes(name,age) inside the class(my_class) that will used by all object instances which will be created in future
```python
class my_class: #class
    def __init__(self,name,age): #method
        self.name=name #attribute 1
        self.age=age #attribute 2

my_object=my_class("yogesh",20)  #object intance is instantiated with attributes defined in it
print(my_object.name) # accessing attribute 1
print(my_object.age) # accessing attribute 2
```
