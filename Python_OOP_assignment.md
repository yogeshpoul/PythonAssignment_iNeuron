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
    

Q8. How would you define the superclasses of a class?
- To define superclasses (also known as parent classes or base classes) of a class in Python, you can specify the superclass names in parentheses after the class name in the class definition.
```python
class parent:
    def __init__(self,name,age):
        self.name=name #attribute 1
        self.age=age #attribute 2

class child(parent): #"here we defined superclass(parent) of subclass(child)"
    def __init__(self,name,age): #here we called method of superclass using the super() keyword
        super().__init__(name,age)

p=parent("yogesh",20)
c=child("xyz",2)

print(p.name)
print(p.age)

print(c.name)
print(c.age)
```


Q9. What is the relationship between classes and modules?
- A module can contain one or more classes along with other definitions and statements. 
- Classes can be defined in a module or imported from other modules.
- When you import a module into a Python script, you can access its classes and other definitions using dot notation
```python
import my_module

obj = my_module.MyClass()
```


Q10. How do you make instances and classes?
- classes: methods and attributes created inside classes
- instances: used for calling the methods and attributes from classes at that instance
```python
class MyClass: #this is class
    def __init__(self, name):
        self.name = name

obj1 = MyClass("John") # this is instance 1
obj2 = MyClass("Alice") # this is instance 2
```

Q11. Where and how should be class attributes created?
- class attributes are created inside the class but outside the any methods
```python
class my_class:
    branch="cs" #class attributes(inside the class but outside the method)
    def __init__(self,name):
        self.name=name 

m=my_class 
print(m.branch)
```


Q12. Where and how are instance attributes created?
- instance attributes is created inside the constructor method (__init__) and method is already in class.
```python
class my_class:
    branch="cs" 
    def __init__(self,name):
        self.name=name #instance attributes(inside the method)

s1=my_class("yogesh") 
s2=my_class("xyz")
print(s1.name)
```

Q13. What does the term "self" in a Python class mean?
- the "self" parameter allows instance to access the attributes and methods of class.
- using self, you can modify the instance's state and behavior, and access instance variables. 
```python
class my_class:
    branch="cs" 
    def __init__(self,name):
        self.name=name 

s1=my_class("yogesh") #this instance calls method of the class by the access of self
s2=my_class("xyz")
print(s1.name)
```

Q14. How does a Python class handle operator overloading?
- when the operator is used in the object instance of class then it will call the method(__add__) inside the class
- the behaviour of method(__init__) inside the class can be defined by user according to user convience
```python
class books:
    def __init__(self,name,pages):
        self.name=name
        self.pages=pages
    
    def __add__(self,other): #here we defined method for addition of pages
        return self.pages+other.pages

b1=books("one indian girl",300)
b2=books("making india awesome",200)
print(b1+b2) #with the __add__ method(it will call __add__ method )
print(b1.pages+b2.pages) #without the __add__ method (it not call __add__ method )
```


Q15. When do you consider allowing operator overloading of your classes?
- to make our code more readable ,expressive and convenient syntax for manipulating its elements 
- operator overloading provides us features of defining custom methods known as magic methods
```python
class books:
    def __init__(self,name,pages):
        self.name=name
        self.pages=pages
    
    def __add__(self,other): #here we defined method for addition of pages
        return self.pages+other.pages

b1=books("one indian girl",300)
b2=books("making india awesome",200)

print(b1.pages+b2.pages) #without the operator overloading method it is not that much readable and it is complex
print(b1+b2) #with the operator overloading method it is much readable and it is not complex
```

Q16. What is the most popular form of operator overloading?
- most commonly used used operator overloading is __add()__ in "int" and "str" also

Q17. What are the two most important concepts to grasp in order to comprehend Python OOP code?
- classes and obejcts

Q18. Describe three applications for exception processing.
- exceptions occurs during the execution of programs
  - Error handling: Exceptions can be used to handle errors that occur during program execution. For example, if a file cannot be opened or read, an exception can be raised, allowing the program to gracefully handle the error and prevent a crash.
  - Debugging: Exceptions can be used as a debugging tool to help identify errors in code. By catching and printing exceptions, developers can identify where errors occur and fix them.
  - Program flow control: Exceptions can be used to control the flow of a program. For example, if a program encounters an error, it can raise an exception and stop execution of the current block of code, allowing the program to continue executing other parts of the code.
