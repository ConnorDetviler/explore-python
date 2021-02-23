# First steps into python

I followed these instructions for installing python and doing my first hello world program

https://code.visualstudio.com/docs/python/python-tutorial

installed with 'brew install python3' in terminal

selected a python interpreter in VSCode

created 'hello.py' with simple declaration and print statement:

    msg = "Hello World"
    print(msg)

learned how to use the debugger

installed the 'matplotlib' package and ran it inside a virtual environment

# Doing my own practice

Then, I moved on to practicing various built-in python functions to get a feel for the language:

    msg = "hello world"
    print(msg)

    # splits each group of characters divided by spaces into seperate strings
    # then stores each string in array
    print(msg.split())

    # counts number of times 'o' occurs in string
    print(msg.count('o'))

    # capitalizes first letter of each word in string
    print(msg.title())

    # returns absolute value (3 in this case)
    print(abs(-3))

    numList = [4, 6, -3, 2, 7, 23, 54, 2, -6]

    # returns max value
    print(max(numList))

    # returns min value
    print(min(numList))
    
Upon reading the docs, I stumbled upon arrays and lists so I needed to figure out the difference

Lists are like arrays in JS, they can store multiple data types

Arrays in python can only store one data type. Python does not support arrays by default - module must be imported to declare array

more differences between the two are described here: https://www.geeksforgeeks.org/difference-between-list-and-array-in-python/

# Writing Functions

    # defining a function
    def add_two_numbers(num_one, num_two):
        return num_one + num_two

    # calling it inside of a print
    print('adding two numbers together,', add_two_numbers(2, 5))
    
returns:
adding two numbers together, 7
    
## Function with conditional

    def greet(name):
        if name:
            return 'Hello ' + name + '!'
        else:
            return "You didn't tell me your name!"

  
    print(greet('Connor'))
    print(greet(''))
    
The first print returns 'Hello Connor!', since name is a truthy value

Because an empty string is a falsy value, the second print returns 'You didn't tell me your name!'

# Objects and classes

The following examples were pulled from https://www.w3schools.com/python/python_classes.asp

classes act as constructors for objects

    #classes and objects
    class MyClass:
        x='Im a property'

    p1 = MyClass()
    print (p1.x)
    # returns 'Im a property'

the init function assigns values for name and age:
methods can be defined within objects as well
myfunc is being defined as a method within the p1 object

    class Person:
        def __init__ (self, name, age):
            self.name = name
            self.age = age

        def myfunc(self):
            print("hello, my name is " + self.name)

    p1 = Person("John", 36)
    p1.myfunc()
    
object properties can be changed later too:

p1.name = 'Jerry'

# Whiteboard challenge

Prompt:
Write a function that takes in two arguments, a list of strings and a string.
The function should return the number of times the string is found in the list.

    list_one = ['dog', 'cat', 'dog', 'dog', 'elephant', 'tiger', 'tiger', 'dog', 'elephant']

    def string_occur(list, string):
        # len gets the length of list, range creates a sequence of numbers from 0 to the full length of the list
        # then i is each index in the iteration of that sequence
        x = 0
        for i in range(len(list)):
            # each time the string is found in the loop, x is incremented by one
            if string == list[i]:
                x += 1
        # when the loop is done, x contains the desired value
        return x


    print(string_occur(list_one, 'dog'))
    # returns 4

    print(string_occur(list_one, 'cat'))
    # returns 1

    print(string_occur(list_one, 'elephant'))
    # returns 2
