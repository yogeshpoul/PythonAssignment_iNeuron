## Python OOP Assignment
Q1. What is the purpose of Python's OOP?
- in python oop(object oriented programming) is a paradigm that uses objects and classes in programming.
- it aims to implement real world entities like inheritence, polymorphism, encapsulation, etc in the programs.
- the main goal of oop is to bind data and functions work together as a single entity no other part of code can access this data.

Q2. Where does an inheritance search look for an attribute?
- When searching for an attribute in a class hierarchy, Python first looks for the attribute in the instance object itself. If the attribute is not found there, it looks for the attribute in the class of the instance. If the attribute is still not found in the class, Python searches in the first superclass of the class, then in the superclass of that superclass, and so on. If the attribute is not found in any of the superclasses, Python raises an AttributeError.

```python
class Base: #step 3:
    def __init__(self):
        self.x="Base" 


class Derived1(Base):  # step 2:
    def __init__(self):
        super().__init__()
        self.x="Derived1"

class Derived2(Base): #step 2:
    def __init__(self):
        super().__init__()
        #self.x="Derived2"


obj1=Derived1()
obj2=Derived2()


obj1.x #step 1: #Accessing attribute x it will print "Derived1"
obj2.x #step 1: #Accessing attribute x it will print "Base" becuase x(attribute) is not found in the Derived1 Class then it will goes to the Base class's attribute
```


Q3. How do you distinguish between a class object and an instance object?
- Class objects define attributes(e.g, model,year,price) and methods(e.g, functions,methods,init method) that are common to all instances of the class.
- while instance objects have their own unique attributes and can also override class attributes.
class object:
```python
class car:
    pass
```
instance object: Instances are created by calling the class constructor (usually denoted by the class name followed by parentheses).
```python
honda=car()
tata=car()
```
- Class:class is blueprint or template for creating objects
        It encapsulates attributes (variables) and methods (functions) that describe the properties and actions associated with objects of that class.
- Instance(Object):An instance is a specific, concrete realization of a class.
                   it is created based on bluprint of the class.
                   each instace has its own attributes and methods independent of the other instances of the same class.


Q4. What makes the first argument in a class’s method function special?
- `self` makes the first argument in class's method function special
- self refers to instance object that the method is called on
- self gives access to method to modify attributes of class object's attributes

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
- most commonly used used operator overloading is __add__() in "int" and "str"(__str__()) also

Q17. What are the two most important concepts to grasp in order to comprehend Python OOP code?
- classes and obejcts

Q18. Describe three applications for exception processing.
- exceptions occurs during the execution of programs
  - Error handling: Exceptions can be used to handle errors that occur during program execution. For example, if a file cannot be opened or read, an exception can be raised, allowing the program to gracefully handle the error and prevent a crash.
  - Debugging: Exceptions can be used as a debugging tool to help identify errors in code. By catching and printing exceptions, developers can identify where errors occur and fix them.
  - Program flow control: Exceptions can be used to control the flow of a program. For example, if a program encounters an error, it can raise an exception and stop execution of the current block of code, allowing the program to continue executing other parts of the code.

Q19. What happens if you don't do something extra to treat an exception?
- if you don't do exception handling in code then if any exception occurs it will terminate code and thows a exception and the remaining code will not works
- it will be more dangerous when you work in production environment this will lead organizations in losses

Q20. What are your options for recovering from an exception in your script?
- catching exceptoin and taking some actions on that exception
- displaying exceptioin message to user so, that user can take appropriate actions
```python
try:
    #code containing exceptions(suspecious code)
except [ExceptionName]:
    #code to handle exception(if occured)
else:
    #if no exception occured this block will execute
```

Q21. Describe two methods for triggering exceptions in your script.
- Try: this method catches exception raised by the program
```python
try:
    number=int('abc')
except ValueError as e:
    print(f"an error occured {e}")
```
- Raise: this method used to Triggers exception manually using custom exceptions
```python
def func(a,b):
    if b==0:
        raise ValueError("division by zero not possible")
    return a/b

try:
    func(1,0)
except ValueError as e:
```

Q22. Identify two methods for specifying actions to be executed at termination time, regardless of  
whether or not an exception exists.
- finally:
finally method is executed regardless of the execution flow 
```python
try:
    # Perform some operations that may raise exceptions
except Exception:
    # Exception handling code
finally:
    # Code to be executed at termination time regardless of execution flow(whether or not an exception exists)
```
- atexit module:
```python
import atexit

def cleanup():
    # Code to be executed at termination time
    ...

atexit.register(cleanup)
```

Q23. What is the purpose of the try statement?
- to define block of code where exception might occur
- block of code is tested in try statement whether the exeptions occurs or not

Q24. What are the two most popular try statement variations?
- try-except: in this try block used to catch exception and except handles exception
- try-finally: in this try block used to catch exception and finally executes regardless of exeception

Q25. What is the purpose of the raise statement?
- raise statement is used to catch the exception manually using custom exeptions

Q26. What does the assert statement do, and what other statement is it like?
- assert statement is used to debug the code
- used to test if condition in code returns True then nothing happens and if condition in code returns False, AssertionError is raised
```python
x = "hello"
#if condition returns True, then nothing happens:
assert x == "hello" 
```
output:
it returns nothing

```python
x = "hello"
#if condition returns False, AssertionError is raised:
assert x == "goodbye"
```
output: 
`Traceback (most recent call last):
  File "demo_ref_keyword_assert.py", line 5, in <module>
    assert x == "goodbye"
AssertionError`

Q27. What is the purpose of the with/as argument, and what other statement is it like?
- ensures closing resources right after processing them. 
- without using with/as arguement
```python
#without try finally
file = open("example.txt", 'w')
file.write('hello world !')
file.close()#in this we need to ensure that file must be closed
```
```python
#with finally block
file = open("example.txt", 'w')
try:
    file.write('hello world !')
except FileNotFoundError as e:
    print(e)
finally:
    file.close() #in this we need to ensure that file must be closed
```
- using with/as arguement
```python
with open("example.txt",'r') as file:
    file.read() #in this we dont need to close the file
```
Q28. What are *args, **kwargs?
- *args(positional argument), **kwargs(keyword arguments) allow to pass variable number of arguments to a function without specifying them explicitly in function

- *args(Arbitrary positional argument):
- *args syntax allows to pass variable number of positoinal argument to a function stores them as tuple 
```python
def func(*args):
    for arg in args:
        print(arg)
func(1,2,3,4)
```
- *kwargs(Arbitrary keyword argument):
- *kwargs syntax allows variable number of keyword arguments to function and stores them as dictionary
```python
def func(**kwargs):
    for k,v in kwargs.items():
        print(k,v)
func(k1=1,k2=2)
```

Q29. How can I pass optional or keyword parameters from one function to another?
- to pass optional or keyword parameters from one function to another '*args' and '**kwargs' unpacking syntax is used
- this approach allows to forward arguments from one function to second function without explicitely listing each argument
```python
def func1(*args,**kwargs):
    # Perform some operations in fun1
    # Forward the arguments to func2
    func2(*args,**kwargs)
    
    
def func2(*args,**kwargs):
    # Perform some operations in func2
    # Access the forwarded arguments
    print(f"the args are: {args}")
    print(f"the args are: {kwargs}")
    
func1(10,2,3,4,k1="hello",k2="wordl")
```
- especially useful when you want to create wrapper functions or when you want to delegate specific tasks to different functions while maintaining a consistent interface.


Q30. What are Lambda Functions?
- lambda function is small anonymous function that can have any number of arguments but can have only one expression
- lambda functions are often used when you need simple, short function for specific task and don't want to define full fledged function name using keyword "def" 
syntax for lambda function:
```python
lambda arguments: expression
```
example:
```python
square=lambda x:x**2
square(5)
```
```python
arr=[1,2,3,4,5]
square=map(lambda x:x**2,arr)
list(square)
```

Q31. Explain Inheritance in Python with an example?
- inheritance allows code reuse and creation of more specialised classes from based on existing one
- inheritance allows a new class(child class) to inherit properties and behaviours(attributes and methods) from an existring class(parent class)
```python
class Animal: # parent class is created
    def __init__(self, name):# constructor is created
        self.name = name

    def speak(self):
        pass
    
class Cat(Animal): #Cat class is inherited from the parent class Animal
    def sounds(self):
        return f"{self.name} says meow"
    
c=Cat("gundya") #object is created
print(c.sounds()) #object is called
```

Q32. Suppose class C inherits from classes A and B as class C(A,B).Classes A and B both have their own versions of method func(). If we call func() from an object of 
class C, which version gets invoked?
```python
class A:
    def func(self):
        return "you are in class A"
    
class B:
    def func(self):
        return "you are in class B"
class C(A,B):
    pass
    #def func(self):
        #return "you are in class c"
c=C()
c.func()
```
- when a class is inherited from the multiple classes then it is called as multiple inheritence
- the method resolution order(MRO) determines order in which function(method) from class  are looked up and invoked
- in this case method resolution order(MRO) is '(C,A,B)' means python will look into the function of class C then class A and finally B

Q33. Which methods/functions do we use to determine the type of instance and inheritance?
- isinstance() and issubclass() are used to determine the type of instance and inheritance respectively
1. isinstance(object,classinfo): isinstance function returns true if provided object is instance of class specified in classinfo argument or any subclass(direct,indirect or virtual) derived from it
2. issubclass(class,classinfo): issubclass function returns true if provided class is subclass(direct,indirect or virtual) of class specified in classinfo argument. it also considers that the class to be class itself
```python
class A:
    pass

class B(A):
    pass

obj = B()
print(isinstance(obj, B))  # Output: True
print(isinstance(obj, A))  # Output: True
print(issubclass(B,A))    # Output: True
print(issubclass(A,B))    # Output: False
```

Q34.Explain the use of the 'nonlocal' keyword in Python.
- 'nonlocal' keyword is used to modify the variable that is not in local to current function but also not in global scope.
- this is particularly useful when we nested function and we want modify variable from outer function in the inner function
```python
#without nonlocal keyword x is not getting modified by the inner function
def outer_function():
    x="john"
    def inner_function():
        x="hello"
    inner_function()
    return x #o/p x=john

print(outer_function())
```
```python
#using nonlocal keyword x is getting modified by the inner function
def outer_function():
    x="john"
    def inner_function():
        nonlocal x
        x="hello"
    inner_function()
    return x #o/p x=hello

print(outer_function())
```

Q35. What is the global keyword?
- when we declare a variable outside the scope of function then we can only access it we can not modify it inside the function
- for modification of global varibles inside the function the global keyword is used
```python
#Example 1: Accessing global Variable From Inside a Function
a=5
b=10 #global variables

def add():
    c=a+b #global variables can be accessed inside function but cannot be modified
    return c #o/p: 15
add()
```
```python
#Example 2: Modifiying global variables inside the function without using the global keyword
a=5
def modification():
    a=a+5
    return a
modification()
#o/p: UnboundLocalError: local variable 'a' referenced before assignment
#inside the function the global variable can not be modified without using global keyword
```
```python
#Example 3: Modifiying global variables inside the function using the global keyword
a=5
def modification():
    global
    a=a+5
    return a
modification()
#o/p: 10
#inside the function the global variable can not be modified without using global keyword
```
