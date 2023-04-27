## Python OOP Assignment
Q1. What is the purpose of Python's OOP?
-> 
- in python oop(object oriented programming) is a paradigm that uses objects and classes in programming.
- it aims to implement real world entities like inheritence, polymorphism, encapsulation, etc in the programs.
- the main goal of oop is to bind data and functions work together as a single entity no other part of code can access this data.

Q2. Where does an inheritance search look for an attribute?
- When searching for an attribute in a class hierarchy, Python first looks for the attribute in the instance object itself. If the attribute is not found there, it looks for the attribute in the class of the instance. If the attribute is still not found in the class, Python searches in the first superclass of the class, then in the superclass of that superclass, and so on. If the attribute is not found in any of the superclasses, Python raises an AttributeError.
