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

    numArray = [4, 6, -3, 2, 7, 23, 54, 2, -6]

    # returns max value
    print(max(numArray))

    # returns min value
    print(min(numArray))
    
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
