## Assignment Part-1
Q1. Why do we call Python as a general purpose and high-level programming language?
Q1.ans -> 1. python is used widely in variety of domains and it qualifies all the rules of general purpose language.
   2. Python is interpreted language ,python code is written in very, simple language and its source code is converted into bytecode(machine level code) to understand the machine

Q2. Why is Python called a dynamically typed language?
-> variable is assigned when python code is interpreted. Basically, we don’t need declare the variables


Q3. List some pros and cons of Python programming language?
-> Pros: user friendly 
	     Large community 
	     Large number of libraries
   cons: takes too much time for execution
         slow speed
         heavy memory usage

Q4. In what all domains can we use Python?
-> python is used widely in variety of domains ranging from Data Science, Machine Learning, Deep Learning, Artificial Intelligence, Scientific Computing Scripting, Networking, Game Development to Web Development
but the best domains are for python are:
**-Data Science.
-Automation.
-Application Development.
-AI & Machine Learning.
-Audio/Video Applications.
-Console Applications.
-Desktop GUI.**

Q5. What are variable and how can we declare them?
-> 1. Variables are the basic unit of storage in a programming language. A variable is created the moment you first assign a value to it.
   2. Python has no command for declaring a variable
```python
x = 5
y = "yogesh"
```

Q6. How can we take an input from the user in Python?
-> we can take input from user by using input keyword and that input we have to store in variable
```python
x=input("enter the input: ")
```

Q7. What is the default datatype of the value that has been taken as an input using input() function?
-> string data type

Q8. What is type casting?
-> The conversion of one data type into the other data type is known as type casting in python.
```python
z=10
type(z)

m=float(z)
type(m)
```

Q9. Can we take more than one input from the user using single input() function? If yes, how? If no, why?
-> yes, we can take more than one input from user using single input() by attaching split() function 

#approach 1: fixed inputs
```python
x,y,z=input("enter input:").split(',')
print(x,y,z)
```
#approach 2: dynamic inputs
```python
x=[x for x in input("enter input: ").split(',')]
print(x)
```

Q10. What are keywords?
-> keywords are special reserved words. keywords can not be used as a variables

Q11. Can we use keywords as a variable? Support your answer with reason.
-> no, we can not use keywords as a variable because keywords have special meanings to the compiler and They are used to define the syntax and structure of the Python language

Q12. What is indentation? What's the use of indentaion in Python?
-> identation is 4 white spaces. Python uses indentation to indicate a block of code. Python will give you an error if you skip the indentation

Q13. How can we throw some output in Python?
->using print() statement 
```python
print("this is output")
```

Q14. What are operators in Python?
-> operators are special symbols that designate that some sort of computation should be performed
-Arithmetic Operators
-Comparison Operators
   -Equality Comparison on Floating-Point Values
-Logical Operators
   -Logical Expressions Involving Boolean Operands
   -Evaluation of Non-Boolean Values in Boolean Context
   -Logical Expressions Involving Non-Boolean Operands
   -Compound Logical Expressions and Short-Circuit Evaluation
   -Idioms That Exploit Short-Circuit Evaluation
   -Chained Comparisons
-Bitwise Operators
-Identity Operators
-Operator Precedence
-Augmented Assignment Operators

Q15. What is difference between / and // operators?
'/' is used for the normal division of two numbers.
'//' is used to obtain the smallest integer nearest to the quotient obtained by dividing two numbers.


Q16. Write a code that gives following as an output.
```
iNeuroniNeuroniNeuroniNeuron
```
->
```python
string="iNeuron"
print(string*3)
```

Q17. Write a code to take a number as an input from the user and check if the number is odd or even.
```python
# Q 17 ans :
x=int(input("enter the input : "))
if x%2==0:
    print(x," is even")
else:
    print(x," is odd")
```

Q18. What are boolean operator?
->True , False , not , and , or are boolean operators

Q19. What will the output of the following?
```
1 or 0

0 and 0

True and False and True

1 or 0 or 0
```
->
```python
1
0
False
1
```

Q20. What are conditional statements in Python?
-> conditional statement in python:
-if statement
-if-else statement
-if-elif-else ladder

Q21. What is use of 'if', 'elif' and 'else' keywords?
->
'if', 'elif' and 'else' are used to create conditional statements 
there is always if condition is checked first then elif and at the end else
if "if" is false then "elif" is executed if all the blocks of conditional statements of "if" and "elif" are executed and failed then else block is executed

Q22. Write a code to take the age of person as an input and if age >= 18 display "I can vote". If age is < 18 display "I can't vote".
```python
# Q 22 ans:
age=int(input("enter age: "))
if age>=18:
    print("I Can Vote")
else:
    print("I Can Vote")
```

Q23. Write a code that displays the sum of all the even numbers from the given list.
```
numbers = [12, 75, 150, 180, 145, 525, 50]
```
```python
# Q23 ans :
numbers = [12, 75, 150, 180, 145, 525, 50]
sumofEven=0
for number in numbers:
    if number%2==0:
        sumofEven+=number
print(sumofEven)
```

Q24. Write a code to take 3 numbers as an input from the user and display the greatest no as output.
```python
# Q24 ans:
x,y,z=input("enter three numbers: ").split()
if x>y and x>z:
    print(x," is greater")
elif y>z and y>x:
    print(y," is greater")
    
else:
    print(z," is greater")

```

Q25. Write a program to display only those numbers from a list that satisfy the following conditions

- The number must be divisible by five

- If the number is greater than 150, then skip it and move to the next number

- If the number is greater than 500, then stop the loop
```
numbers = [12, 75, 150, 180, 145, 525, 50]
```

```python
numbers = [12, 75, 150, 180, 145, 525, 50]
for number in numbers:
    if number>150:
        if number>500:
            break
        continue
    
    if number%5==0:
        print(number)
```
