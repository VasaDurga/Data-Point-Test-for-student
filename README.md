# Test Python
# Questions

Question 1: What is the difference between a list and a tuple?
A)  List and Tuple in Python are the class of data structure. The list is dynamic, whereas the tuple has static characteristics. 
LIST:-

List is just like the arrays, declared in other languages. Lists need not be homogeneous always which makes it the most powerful tool in Python. In Python, the list is a type of container in Data Structures, which is used to store multiple data at the same time. Lists are a useful tool for preserving a sequence of data and further iterating over it. 
Syntax: 
list_data = ['an', 'example', 'of', 'a', 'list

TUPLE:-

Tuple is also a sequence data type that can contain elements of different data types, but these are immutable in nature. In other words, a tuple is a collection of Python objects separated by commas. The tuple is faster than the list because of static in nature. 
Syntax:  
tuple_data = ('this', 'is', 'an', 'example', 'of', 'tuple

Difference Between List and Tuple in Python:  

1	Lists are mutable	Tuples are immutable
2	Implication of iterations is Time-consuming	in list whereas in tuple the implication of iterations is comparatively Faster
3	The list is better for performing operations, such as insertion and deletion whereas Tuple data type is appropriate for accessing the elements
4	Lists consume more memory	where Tuple consume less memory as compared to the list
5	Lists have several built-in methods	where Tuple does not have many built-in methods.
6	The unexpected changes and errors are more likely to occurbut in tuple, it is hard to take place.

Question 2: How would you convert a list into a tuple?
A) 

PROGRAM:-

#Convert list to tuple
listx = [5, 10, 7, 4, 15, 3]
print(listx)
#use the tuple() function built-in Python, passing as parameter the list
tuplex = tuple(listx)
print(tuplex)

OUTPUT:-
[5, 10, 7, 4, 15, 3]                                                                                          
(5, 10, 7, 4, 15, 3)


Question 3: How is memory managed in Python?
A)
Understanding Memory allocation is important to any software developer as writing efficient code means writing a memory-efficient code. Memory allocation can be defined as allocating a block of space in the computer memory to a program. In Python memory allocation and deallocation method is automatic as the Python developers created a garbage collector for Python so that the user does not have to do manual garbage collection.

Garbage Collection:-

Garbage collection is a process in which the interpreter frees up the memory when not in use to make it available for other objects.
Assume a case where no reference is pointing to an object in memory i.e. it is not in use so, the virtual machine has a garbage collector that automatically deletes that object from the heap memory

Reference Counting:-

Reference counting works by counting the number of times an object is referenced by other objects in the system. When references to an object are removed, the reference count for an object is decremented. When the reference count becomes zero, the object is deallocated.

For example, Let’s suppose there are two or more variables that have the same value, so, what Python virtual machine does is, rather than creating another object of the same value in the private heap, it actually makes the second variable point to that originally existing value in the private heap. Therefore, in the case of classes, having a number of references may occupy a large amount of space in the memory, in such a case referencing counting is highly beneficial to preserve the memory to be available for other objects.

program:-

x = 10
y = x
  
if id(x) == id(y):
    print("x and y refer to the same object")
    
Output:

x and y refer to the same object

Question 4: What is a lambda function? Give an example of when it’s useful and when it’s not?

A)
In Python, an anonymous function is a function that is defined without a name.

While normal functions are defined using the def keyword in Python, anonymous functions are defined using the lambda keyword.

Hence, anonymous functions are also called lambda functions.
How to use lambda Functions in Python?
A lambda function in python has the following syntax.

Syntax of Lambda Function in python
lambda arguments: expression
Lambda functions can have any number of arguments but only one expression. The expression is evaluated and returned. Lambda functions can be used wherever function objects are required.

Example of Lambda Function in python
Here is an example of lambda function that doubles the input value.

# Program to show the use of lambda functions
double = lambda x: x * 2

print(double(5))

Output:--

10

Use of Lambda Function in python
--------------------------------------
We use lambda functions when we require a nameless function for a short period of time.

In Python, we generally use it as an argument to a higher-order function (a function that takes in other functions as arguments). Lambda functions are used along with built-in functions like filter(), map() etc.

Example use with filter()

The filter() function in Python takes in a function and a list as arguments.

The function is called with all the items in the list and a new list is returned which contains items for which the function evaluates to True.

Here is an example use of filter() function to filter out only even numbers from a list.

# Program to filter out only the even items from a list
my_list = [1, 5, 4, 6, 8, 11, 3, 12]

new_list = list(filter(lambda x: (x%2 == 0) , my_list))

print(new_list)

Output:-

[4, 6, 8, 12]

Example use with map()

The map() function in Python takes in a function and a list.

The function is called with all the items in the list and a new list is returned which contains items returned by that function for each item.

Here is an example use of map() function to double all the items in a list.

# Program to double each item in a list using map()

my_list = [1, 5, 4, 6, 8, 11, 3, 12]

new_list = list(map(lambda x: x * 2 , my_list))

print(new_list)

Output:-

[2, 10, 8, 12, 16, 22, 6, 24]

Question 5: Explain range().
A)  The range() function is used to generate a sequence of numbers over time. At its simplest, it accepts an integer and returns a range object (a type of iterable). In Python 2, the range() returns a list which is not very efficient to handle large data.

The syntax of the range() function is as follows:

Syntax:

range([start,] stop [, step]) -> range object
PARAMETER	DESCRIPTION
start	(optional) Starting point of the sequence. It defaults to 0.
stop (required)	Endpoint of the sequence. This item will not be included in the sequence.
step (optional)	Step size of the sequence. It defaults to 1.

example1:-
range(5)
range(0, 5)
>>> 
>>> list(range(5)) # list() call is not required in Python 2
[0, 1, 2, 3, 4]

----------------------------------

print(range(5))

# list() call is not required in Python 2 
print(list(range(5)))
o/p:-
range(0, 5)
[0, 1, 2, 3, 4]

example2:-
range(5, 10)
range(5, 10)
>>> 
>>> list(range(5, 10))
[5, 6, 7, 8, 9]

-------------------------------------

print(range(5, 10))
print(list(range(5, 10)))
output:-
range(5, 10)
[5, 6, 7, 8, 9]


Question 6: Write a Python function to sum all the numbers in a list.
             li = [8, 2, 3, 0, 7]
             o/p: total = 20
 A)program:-
  # Python program to find sum of elements in list
total = 0
 
# creating a list
li = [8, 2, 3, 0, 7]
 
# Iterate each element in list
# and add them in variale total
for ele in range(0, len(li)):
    total = total + li[ele]
 
# printing total value
print("total = ",total)

output:-
total = 20


Question 7: Write a function to reverse a string?
            s = '1234abcd'
            
def reverse(s):
  str = ""
  for i in s:
    str = i + str
  return str
  
s = "1234abcd"
  
print ("The original string  is : ",end="")
print (s)
  
print ("The reversed string(using loops) is : ",end="")
print (reverse(s))

output:-

The original string  is : 1234abcd
The reversed string(using loops) is : dcba4321



Question 8: Write a simple Python function to check whether x is even or odd
A)
num = int(input("Enter a number: "))  
if (num % 2) == 0:  
   print("{0} is Even number".format(num))  
else:  
   print("{0} is Odd number".format(num))  
   
output:-

Enter a number: 6
6 is Even number

Enter a number: 7
7 is Odd number

Question 9: Explain map() and reduce() with example?
The map() function:
The map() function is a type of higher-order. As mentioned earlier, this function takes another function as a parameter along with a sequence of iterables and returns an output after applying the function to each iterable present in the sequence. Its syntax is as follows:

SYNTAX:

map(function, iterables)  

EXAMPLE:

def newfunc(a):
    return a*a
x = map(newfunc, (1,2,3,4))  #x is the map object
print(x)
print(set(x))

OUTPUT:

<map object at 0x00000284B9AEADD8>

{16, 1, 4, 9}

The reduce() function

The reduce() function, as the name describes, applies a given function to the iterables and returns a single value.

SYNTAX:

reduce(function, iterables)

EXAMPLE:

from functools import reduce
reduce(lambda a,b: a+b,[23,21,45,98])

OUTPUT: 187

Question 10: Write a function called fizz_buzz that takes a number.

            - If the number is divisible by 3, it should return “Fizz”.

            - If it is divisible by 5, it should return “Buzz”.
            
            - If it is divisible by both 3 and 5, it should return “FizzBuzz”.
            
            - Otherwise, it should return the same number.
A)

for fizzbuzz in range(59):
    if fizzbuzz % 3 == 0 and fizzbuzz % 5 == 0:
        print("fizzbuzz")
        continue
    elif fizzbuzz % 3 == 0:
        print("fizz")
        continue
    elif fizzbuzz % 5 == 0:
        print("buzz")
        continue
    print(fizzbuzz)
	
OUTPUT:-
fizzbuzz
1
2
fizz
4
buzz
fizz
7
8
fizz
buzz
11
fizz
13
14
fizzbuzz
16
17
fizz
19
buzz
fizz
22
23
fizz
buzz
26
fizz
28
29
fizzbuzz
31
32
fizz
34
buzz
fizz
37
38
fizz
buzz
41
fizz
43
44
fizzbuzz
46
47
fizz
49
buzz
fizz
52
53
fizz
buzz
56
fizz
58
