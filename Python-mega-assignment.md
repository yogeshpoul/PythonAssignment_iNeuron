## Assignment Part-1
Q1. Why do we call Python as a general purpose and high-level programming language?
-> 1. python is used widely in variety of domains and it qualifies all the rules of general purpose language.
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

Q26. What is a string? How can we declare string in Python?
-> String is a arrays of bytes representing unicode characters.
```python
a="hello world"
```

Q27. How can we access the string using its index?
->
```python
a="hello world"
a[0:3]
#o/p=> 'hel'
```

Q28. Write a code to get the desired output of the following
```
string = "Big Data iNeuron"
desired_output = "iNeuron"
```
->
```python
#Q28ans
string = "Big Data iNeuron"
string[-7:]
#another approach
string[9:16]
```

Q29. Write a code to get the desired output of the following
```
string = "Big Data iNeuron"
desired_output = "norueNi"
```
->
```python
string = "Big Data iNeuron"
string[15:8:-1]
```

Q30. Resverse the string given in the above question.
->
```python
# Q30 ans:
string="Big Data iNeuron"
print(string[::-1])
```

Q31. How can you delete entire string at once?
->
```python
# Q31 ans:
string="Big Data iNeuron"
del(string)
print(string)
#it is throwing error that string is not defined so our string is deleted
```

Q32. What is escape sequence?
->An escape sequence is a sequence of characters that, when used inside a character or string, does not represent itself but is converted into another character or series of characters
for example we want to `print('Who's this?')`  but it gives syntax error because The interpreter needs clarification. It can't find the starting position of a single quote since it occurred three times
To overcome this problem, we can use escape sequences `\` here `print('Who\'s this?')`

Q33. How can you print the below string?
```
'iNeuron's Big Data Course'
```
-> using escape sequence `\` here
```python
print('iNeuron\'s Big Data Course')
```

Q34. What is a list in Python?
-> list is ordered collection of homogeneous or heterogeneous elements enclosed within [] . lists are mutable(changable). we can say that list is array

Q35. How can you create a list in Python?
->
```python
l1=[1,2,'yogesh',True]
```

Q36. How can we access the elements in a list?
->
l1=[1,2,'yogesh',True]
l1[2]
#output -> 'yogesh'

Q37. Write a code to access the word "iNeuron" from the given list.
```
lst = [1,2,3,"Hi",[45,54, "iNeuron"], "Big Data"]
```
->
```python
# Q37 ans:
lst = [1,2,3,"Hi",[45,54, "iNeuron"], "Big Data"]
lst[4][2] 
```

Q38. Take a list as an input from the user and find the length of the list.
->
# Q38 ans:
```python
#approach 1
x=[x for x in input("enter elements for list: ").split(',')]
print(f"length of list is {len(x)}")
```
```python
#approach 2
lst=input("enter the values: ").split(",")
print(f"the length of list is: {len(lst)}")
```

Q39. Add the word "Big" in the 3rd index of the given list.
```
lst = ["Welcome", "to", "Data", "course"]
```
->
```python
# Q39 ans:
lst = ["Welcome", "to", "Data", "course"]
lst.insert(2,"big")
lst
```

Q40. What is a tuple? How is it different from list?
-> list is ordered collection of homogeneous or heterogeneous elements enclosed within () . lists are immutable(non-changable) and list is mutable(changable). for the searching tuple is faster than list

Q41. How can you create a tuple in Python?
->
using () round brackets we can create tuple
```python
tup1=(1,'yogesh',True)
```

Q42. Create a tuple and try to add your name in the tuple. Are you able to do it? Support your answer with reason.
->
no, im not able to add my name directly to tuple because tuple is mutable
```python
tup1=() #tuple is created
tup1.append("yogesh") # tryig to adding name to it
```
but we can convert tuple to list then we can add it name and again we have to convert it to the tuple
->
```python
tup1=()
tup1=list(tup1)
tup1.append("yogesh")
tup1=tuple(tup1)
tup1
```

Q43. Can two tuple be appended. If yes, write a code for it. If not, why?
->
```python
tup1=("big ")
tup2=("data")
tup1+tup2
```

Q44. Take a tuple as an input and print the count of elements in it.
->
# Q44 ans:
```python
#approach 1
tup=input("enter the number").split(",")
tup=tuple(tup)
print(f"the numer of elements in tuple are: {len(tup)} ")
```
#approach 2
```python
x=tuple(x for x in input("enter: ").split(','))
print(f"length of list is {len(x)}")
```

Q45. What are sets in Python?
-> set is unordered and unindexed collection of elements enclosed wih {}. duplicates are not allowed in sets. sets are mutable(changable)

Q46. How can you create a set?
-> set is created using curly brackets {} 

Q47. Create a set and add "iNeuron" in your set.
-> 
```python
s1=set()
s1.add("iNeuron")
s1
```

Q48. Try to add multiple values using add() function.
->
```python
s1=set()
s1.add("iNeuron")
s1.add("big")
s1.add("data")
```

Q49. How is update() different from add()?
->
add() takes exactly one argument at a time
update() takes multiple arguments at a time

Q50. What is clear() in sets?
-> clear() used to delete all the elements from the set

Q51. What is frozen set?
-> immutable version of set. A set is a mutable object while frozenset provides an immutable implementation

Q52. How is frozen set different from set?
-> sets is mutable(changable) while frozen set is immutable(non-changable). Sets can't be used as keys in dictionary where as frozen sets can be used

Q53. What is union() in sets? Explain via code.
-> union() is used to concatenate two sets with union mathematical operation  
```python
s1={1,2,3,4}
s2={3,4,5,6}
s1.union(s2)
```

Q54. What is intersection() in sets? Explain via code.
-> intersection() is used to concatenate two sets with intersection mathematical operation
```python
s1={1,2,3,4}
s2={3,4,5,6}
s1.intersection(s2)
```


Q55. What is dictionary ibn Python?
-> dictionary is unordered collection of key-value pairs enclosed within {} curly brackets. dictionary is mutable(changable). in dictionary we cannot add elements without the combination of key-value pair


Q56. How is dictionary different from all other data structures.
-> dictionary is having key-value pair elements and other data structures has only single value elements in them


Q57. How can we delare a dictionary in Python?
-> we can create dictionary using {} and the elements can be added with comma separated
```python
#method 1
s1=dict()
type(s1)

#method 2
s1={1:"mango"}
```

Q58. What will the output of the following?
```
var = {}
print(type(var))
```
`dict`


Q59. How can we add an element in a dictionary?
```python
s1=dict()
s1[1]="mango"
s1["name"]="hapus"
```


Q60. Create a dictionary and access all the values in that dictionary.
```python
s1={1: 'mango', 'name': 'hapus',"region":"konkan"}
for i in s1.items():
    print(i)
```

Q61. Create a nested dictionary and access all the element in the inner dictionary.
```python
s1={1: 'mango', 'name': 'hapus',"region":{"city":"mumbai","populatoin":100000}}
for i in s1.items():
    print(i)
```

Q62. What is the use of get() function?
-> get(key_name) is used to access elements corresponding to the paticular key_name
```python
s1={1: 'mango', 'name': 'hapus',"region":{"city":"mumbai","populatoin":100000}}
s1.get("region")
```

Q63. What is the use of items() function?
-> to access all the elements list from the dictionary
```python
s1={1: 'mango', 'name': 'hapus',"region":{"city":"mumbai","populatoin":100000}}
s1.items()
```


Q64. What is the use of pop() function?
->
pop() is used to remove element from the dictionary 
```python
s1={1: 'mango', 'name': 'hapus',"region":{"city":"mumbai","populatoin":100000}}
s1.pop(1)
```

Q65. What is the use of popitems() function?
-> popitems() removes the last inserted key-value pair 
```python
s1={'name': 'hapus',"region":{"city":"mumbai","populatoin":100000}}
s1.popitem()
```

Q66. What is the use of keys() function?
-> keys() returns only keys from the dictionary 
```python
s1={1: 'mango', 'name': 'hapus',"region":{"city":"mumbai","populatoin":100000}}
s1.keys()
```

Q67. What is the use of values() function?
-> values() returns only values from the dictionary 
```python
s1={1: 'mango', 'name': 'hapus',"region":{"city":"mumbai","populatoin":100000}}
s1.values()
```

Q68. What are loops in Python?
->A for loop in Python is a control flow statement that is used to repeatedly execute a group of statements as long as the condition is satisfied


Q69. How many type of loop are there in Python?
-> there are two types of loops in python "for" and "while"

Q70. What is the difference between for and while loops?
For loop is used when the number of iterations is already known. While loop is used when the number of iterations is already Unknown


Q71. What is the use of continue statement?
-> to end the current iteration in a for loop and start the next iteration


Q72. What is the use of break statement?
-> to exit from the loop when the particular block is occured


Q73. What is the use of pass statement?
-> pass statement is used in the empty place where you have to add code in future 

Q74. What is the use of range() function?
-> range(start,end,step)
   range(0,end,1) by default
   range(end) in this range function start=0 and step=1 is by default 
   range(start,end) in this range function step=1 is by default 
range function returns sequence of numbers 

Q75. How can you loop over a dictionary?
->
```python
s1={1: 'mango', 'name': 'hapus',"region":{"city":"mumbai","populatoin":100000}}
for i in s1.items():
    print(i)
```
