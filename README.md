# GUI-Development-with-Python-and-Tkinter

## Initial setup (for newer Pythonistas)
Hey, in this lecture we'll talk about how to do Python development, just in case you're coming from a different programming language.

### Python version
I recommend you use the latest Python version. For Tkinter development you really need to use Python 3.5+ as Tkinter added new features that make our programs much nicer.

### Work with Python
By far the easiest way to quickly code in Python is to use Repl.it. It's a fast, responsive, web-based editor that allows you to code in Python and also code in Tkinter (and shows you the output!).

I recommend this tool to all my students when they're starting out: [**repl**](https://repl.it)

If you want to take it to the next level and have the ability to code larger projects, and you want to work in your own IDE, I usually recommend PyCharm. PyCharm has a free version called the Community Edition that is plenty powerful for almost anything you'll ever need.

You can get PyCharm here: [**Pycharm**](https://www.jetbrains.com/pycharm/download/)

And you'll need to get Python downloaded as well: [**Python**](https://www.python.org/)

If you'd like to use a different editor, feel free to do so. I often use Visual Studio Code when I'm working on smaller files and projects.

Thanks again for joining me in this course, let's get started!

___ 

# Python Refresher

## Get the Python Refresher code here
To make it easier for you to refer back to the code whenever it's necessary, we've put all the code that we'll cover in this section on GitHub.

You can read it and also download it here: [**Github**](https://github.com/tecladocode/python-refresher)

## Variables 

To define an __**int**__ : 
```python
x = 14 
```
To define a __**float**__ : 
```python
x = 14.7
```
To define a __**String**__ : 
```python
Ch = " TKinter Course "
print ( ch * 2 )
>>> TKinter Course TKinter Course 
```

## Work with strings 

```python
name = "fedi"
greeting = f"hello i'am {name}"
print(greeting)
name = "ghada"
print(greeting)
```
<blockquote> OUTPUT  </blockquote>

```
hello i'am fedi
hello i'am ghada
```
<blockquote> Similar Code  </blockquote>

```python
name = "fedi"
greeting = "hello i'am {} , my lastname is {} "
with_name = greeting.format(name,"kouki")
print(with_name)
```

## Getting user Input 

```python
name = input("Enter your name: ")
print(name)
```
<blockquote> OUTPUT  </blockquote>

```
Enter your name: fedi
fedi
```

<blockquote> Be careful the data type by default is STRING  </blockquote>

```python
length = input("Length (in feet): ")
length_feet = int (length)
print(length_feet/10.8)
```

# Lists, tuples, and sets 

```python
list = ["fedi", "ghada", "baha","emna"]
tuple = ("fedi", "ghada", "baha","emna")
set = {"fedi", "ghada", "baha","emna"}
```
<blockquote> index go from 0 --> length - 1  </blockquote>

<blockquote> You can't modify a tuple  </blockquote>

<blockquote> You can't have multiple element in a set ad dont have order  </blockquote>

## Access to variable in a list, tuple and set 

```python

print (list[0])

```
to add  and delete element 

```python

list.append("Yosri")
l.remove("emna")
set.add("brahim")

```

## Advanced set operations

```python

friends = {"fedi", "ghada", "baha","emna"}
abroad = {"fedi", "baha","emna"}

local_friends = friends.difference(abroad)
print(local_friends)

```
<blockquote> OUTPUT  </blockquote>

```
{'ghada'}
```

### usefull functions for sets 

- set.union(other_set)
- set.intersection(other_set)


## booleans in python

how we get it :
  - comparisons: == , != , < , >, <= , >=

## IF statement 

the template is : 

```python

if ( A ) :
  action A
elif (B) :
  action B
else :
  action C

```

## The 'in' keyword in Python

it uses to check if an elemnt is in a list, a tuple or a set or a substring in a string 

## If statements with the 'in' keyword

```python

user_input =input("Enter 'y' if you would like to play")
if user_input in ("y", "Y"):
  print("Welcome to league of legends ")
else :
  print(" Go Fly ")

```


# The loop in Python 

## While Loop 

```python
while stop_condition :
   do 
```

infinit loop : 

```python
while 1 :
   do
    if cdt :
      break
```

```python
while True :
   do 
```

## For Loop 

```python

friends = ["Fedi","Ghada","Baha","Emna","PApoutsou"]
for friend in friends :
  print(f"Bonjour mon ami {friend}")
for i in range(10):
  print(f"Compteur= {i}")

```

# List comprehensions 

```python

numbers = [1,3,5,7,9]
dubled =[]
for i in numbers:
  doubled.append(i*2)

```
The Second way : 

```python

numbers = [1,3,5,7,9]
dubled =[num*2 for num in numbers]

```

```python

friends = ["Fedi","Ghada","Baha","Emna","Papoutsou"]
strats_s = [ friend for friend in friends if friend.startswith("S") ]

```

## Dictionaries  

```python

friends_ages = {"fedi": 24, "ghada": 24, "pappoutsou":23, "pohpoh":24}
friends_ages["emna"]= 25
print(friends_ages["pappoutsou"])
print(friends_ages)

```

List of dict : 

```python

friends = [
  {"name": "fedi", "age": 24}
  {"name": "ghada", "age": 24}
  {"name": "pappoutsou", "age": 23}
          ]
print(friends[1]["name"])

```

How to parcour a dict : 

```python

friends_ages = {"fedi": 24, "ghada": 24, "pappoutsou":23, "pohpoh":24}
for key in friends_ages:
  print(f"The age of {key} : {friends_ages[key]}") 

```
how to get the key and the value : 

```python

friends_ages = {"fedi": 24, "ghada": 24, "pappoutsou":23, "pohpoh":24}
for name , age  in friends_ages.items():
  print(f"The age of {name} : {age}") 

```

# Destructing variables 

```python

t = 14 , 18  # t will be a tuple 
x, y = t     # x will get the first value and y the second 
print(x,y)

```

```python

head, *tail = [1,2,3,4,5,6]
print(head) # will be 1
print(tail) # will be [2,3,4,5,6]

*head, tail = [1,2,3,4,5,6]
print(*head) # will be 1 2 3 4 5
print(tail) # will be 6

```

# Functions 

## structure of simple function 

```python

def hello():
  print("Hello World!!!")

```

## function args and params 

```python

def add(x,y):
  result = x+y 
  return result

def say_hello(name, surname):
  print(f"hello {name} {surname}")

add(5,3)
say_hello("pappoutssou","pappou")

```

How to set the default value 

```python

default_y = 4
def add(x,y=default_y):
  result = x+y 
  print(result)

add(5)  #  the result 9
default_y = 2
 add(5)  #  the result 7

```
How to return a value 

```python

def add(x,y):
  return x+y

print(add(5,8)) # the result 13


def devide(dividend,divisor):
  if divisor !=0:
    return dividend / divisor
  else:
    return "You Fool"

print(devide(15,3)) # the result will be 5
print(devide(15,0)) # the result will be You Fool 

```

## Lambda functions 

Your first lambda function 

```python

add = lambda x,y : x+y
print(add(5,8)) # the result 13

sequence = [1,3,5,7,9]
doubled = [ (lambda x: x*2)(x) for x in sequence]
doubled = list(map(lambda x:x*2,sequence))

```

##  Dictionary comprehensions

```python
users = [
    (0,"fedi","password"),
    (1,"Ggh","password1"),
    (2,"Poh","password2"),
        ]

user_mapping = { user[1]: user for user in users}

```

##  Unpacking Arguments

```python

def multiply(*args):
  print(args)

multiply(1,3,5) # we will get a tuple (1,3,5)

```

```python

def multiply(*args):
  print(args)
  total = 1 
  for agr in args:
    total = total * arg
  return total

multiply(1,3,5) # we will get 15

```

```python

def add(x,y):
  result = x+y 

nums = [3,5]
print(add(*nums))

nums = {"x":15,"y":16}
print(add(x=nums["x"],y=nums["y"]))
print(add(**nums))

```
multiple args : 

```python

def multiply(*args):
  print(args)
  total = 1 
  for agr in args:
    total = total * arg
  return total

def apply(*args,operator):
  if operator=="*":
    return multiply(*args)
  elif operator =="+":
    return sum(args)
  else :
    return "No valid operator provided to apply()."

print(apply(1,3,6,7,operator="+"))
multiply(1,3,5) # we will get 15

```
## Unpacking keyword arguments 


```python

def named (**kwargs):
  print(kwargs)

named(name='fedi', age=24)  # the output : {'name':'fedi','age': 24 }

```
<blockquote> If we want to have the dict value </blockquote>

```python

def named (name,age):
  print(name,age)

details = {'name':'fedi','age': 24 }
named(**details)  # the output : fedi  24

```
lets make it general : 

```python

def named (**kwargs):
  print(kwargs)

def print_nicely(**kwargs):
  named(**kwargs)
for arg,value in kwargs.items():
  print(f"{arg}:{value}")

print_nicely(name='fedi', age=24)
# {'name':'fedi','age': 24 }
# name:fedi
# age:24

```
__args&kwargs__

```python

def both (*args, **kwargs):
  print(args)
  print(kwargs)

both (1,3,5, name="Fedi" , age=25)
# THE OUTPUT :
# (1,3,5)
# {'name": "Fedi", "age":24}

```

<blockquote> Be patient </blockquote>

```python

def myfunction (**kwargs):
  print(kwargs)
myfunction(**"FEDI") # Error , must be mapping
myfunction(**None) # Error , must be mapping
```

# Objected oriented Programming 

```python
class Student:

   def __init__(self,name,grades):
      self.name = name
      self.grades=grades

   def average(self):
      return sum(self.grades) / len(self.grades)

student =Student("fedi", (19,19.5,20,20,18,17.75) )
print(student.name)
print(student.average())

```

## Magic methods: __str__ and __repr__

In Python, "magic methods" (also known as dunder methods or special methods) are methods with double underscores before and after their names. They allow you to define how objects of a class should behave with respect to built-in operations and functions. These methods enable custom behavior for operators, type conversion, attribute access, and more.

### Print method 

```python
class Student:

    def __init__(self,name,age,grades):
      self.name = name
      self.age= age
      self.grades=grades

    def average(self):
      return sum(self.grades) / len(self.grades)

    def __str__(self):
      return (f"hello my name is {self.name}, and i'am {self.age} Yo}

    def __repr__(self):
      return f"<Student({self.name},{self.age})"

student =Student("fedi",24, (19,19.5,20,20,18,17.75) )
print(student) # student.__str__

```
**if str was not defined and repr is print will be the repr function**

# Class Methods and static method 

```python
class ClassTest:
    def instance_method(self):
        print(f"Called instance_method of {self}")

    @classmethod
    def class_method(cls):
        print(f"Called class_method of {cls}")

    @staticmethod
    def static_method():
        print(f"Called static_method. We don't get any object or class info here.")


instance = ClassTest()
instance.instance_method()

ClassTest.class_method()
ClassTest.static_method()

# -- What are they used for? --

# Instance methods are used for most things. When you want to produce an action that uses the data stored in an object.
# Static methods are used to just place a method inside a class because you feel it
# belongs there (i.e. for code organisation, mostly!)
# Class methods are often used as factories.


class Book:
    TYPES = ("hardcover", "paperback")

    def __init__(self, name, book_type, weight):
        self.name = name
        self.book_type = book_type
        self.weight = weight

    def __repr__(self):
        return f"<Book {self.name}, {self.book_type}, weighing {self.weight}g>"

    @classmethod
    def hardcover(cls, name, page_weight):
        return cls(name, cls.TYPES[0], page_weight + 100)

    @classmethod
    def paperback(cls, name, page_weight):
        return cls(name, cls.TYPES[1], page_weight)


heavy = Book.hardcover("Harry Potter", 1500)
light = Book.paperback("Python 101", 600)

print(heavy)
print(light)

```


# Class inheritence 

```python
class Device:
    def __init__(self, name, connected_by):
        self.name = name
        self.connected_by = connected_by
        self.connected = True

    def __str__(self):
        return f"Device {self.name!r} ({self.connected_by})"

    def disconnect(self):
        self.connected = False


# printer = Device("Printer", "USB")
# print(printer)

# We don't want to add printer-specific stuff to Device, so...


class Printer(Device):
    def __init__(self, name, connected_by, capacity):
        # super(Printer, self).__init__(name, connected_by)  - Python2.7
        super().__init__(name, connected_by)  # Python3+
        self.capacity = capacity
        self.remaining_pages = capacity

    def __str__(self):
        return f"{super().__str__()} ({self.remaining_pages} pages remaining)"

    def print(self, pages):
        if not self.connected:
            raise TypeError("Device is disconnected at this time, cannot print.")
        print(f"Printing {pages} pages.")
        self.remaining_pages -= pages


printer = Printer("Printer", "USB", 500)
printer.print(20)
print(printer)
printer.print(50)
print(printer)
printer.disconnect()
printer.print(30)  # Error
```

## Class Composition

```python

# Something I see a lot, but you SHOULDN'T DO


class BookShelf:
    def __init__(self, quantity):
        self.quantity = quantity

    def __str__(self):
        return f"BookShelf with {self.quantity} books."


shelf = BookShelf(300)


class Book(BookShelf):
    def __init__(self, name, quantity):
        super().__init__(quantity)
        self.name = name


# This makes no sense, because now you need to pass `quantity` to a single book:

book = Book("Harry Potter", 120)
print(book)  # What?

# -- Composition over inheritance here --

# Inheritance: "A Book is a BookShelf"
# Composition: "A BookShelf has many Books"


class BookShelf:
    def __init__(self, *books):
        self.books = books

    def __str__(self):
        return f"BookShelf with {len(self.books)} books."


class Book:
    def __init__(self, name):
        self.name = name


book = Book("Harry Potter")
book2 = Book("Python 101")
shelf = BookShelf(book, book2)
print(shelf)

```
# Type hinting in Python 3.5+

```python

def list_avg(sequence: list) -> float:
    return sum(sequence) / len(sequence)


# -- Type hinting classes --


class Book:
    def __init__(self, name: str, page_count: int):
        self.name = name
        self.page_count = page_count


# -- Lists and collections --

from typing import List  # , Tuple, Set, etc...


class BookShelf:
    def __init__(self, books: List[Book]):
        self.books = books

    def __str__(self) -> str:
        return f"BookShelf with {len(self.books)} books."


# Key benefit is now you'll get told if you pass in the wrong thing...

book = Book(
    "Harry Potter", "352"
)  # Suggests this is incorrect if you have a tool that will analyse your code (e.g. PyCharm or Pylint)
shelf = BookShelf(book)  # Suggests this is incorrect too
# Type hinting is that: hints. It doesn't stop your code from working... although it can save you at times!

# -- Hinting the current object --


class Book:
    TYPES = ("hardcover", "paperback")

    def __init__(self, name: str, book_type: str, weight: int):
        self.name = name
        self.book_type = book_type
        self.weight = weight

    def __repr__(self) -> str:
        return f"<Book {self.name}, {self.book_type}, weighing {self.weight}g>"

    @classmethod
    def hardcover(cls, name: str, page_weight: int) -> "Book":
        return cls(name, cls.TYPES[0], page_weight + 100)

    @classmethod
    def paperback(cls, name: str, page_weight: int) -> "Book":
        return cls(name, cls.TYPES[1], page_weight)

```

# imports in python 

we have to file one is : 
## mymodule.py

```python

def divide(dividend, divisor):
    return dividend / divisor


print("mymodule.py:", __name__)

# -- importing from a folder --

import libs.mylib

print("mymodule.py:", __name__)

```
the second is 
## code.py

```python

# -- importing --

from mymodule import divide

print(divide(10, 2))

# -- __name__ --

print(__name__)

# -- importing with names --

import mymodule

print("code.py: ", __name__)

# How does Python know where `mymodule` is?
# Answer, it looks at the paths in sys.path in order:

import sys

print(sys.path)

# The first path is the folder containing the file that you ran.
# The second path is the environment variable PYTHONPATH, if it is set.
# We won't cover environment variables in depth here, but they are variables you can set in your operating system.
# It can help Python find things to import when the folder structure is ambiguous.

# -- circular imports --
# Make mymodule.py import code.py as well.

# -- importing from a folder --

import mymodule

print("code.py: ", __name__)

import sys

print(sys.modules)

```

# Errors in python 
## code.py

```python
def divide(dividend, divisor):
    if divisor == 0:
        raise ZeroDivisionError("Divisor cannot be 0.")

    return dividend / divisor


grades = []  # Imagine we have no grades yet
# average = divide(sum(grades) / len(grades))  # Error!

try:
    average = divide(sum(grades), len(grades))
    print(average)
except ZeroDivisionError as e:
    print(e)
    # Much friendlier error message because now we're dealing with it
    # In a "students and grades" context, not purely in a mathematical context
    # I.e. it doesn't make sense to put "There are no grades yet in your list"
    # inside the `divide` function, because you could be dividing something
    # that isn't grades, in another program.
    print("There are no grades yet in your list.")

# -- Built-in errors --

# TypeError: something was the wrong type
# ValueError: something had the wrong value
# RuntimeError: most other things

# Full list of built-in errors: https://docs.python.org/3/library/exceptions.html


# -- Doing something if no error is raised --

grades = [90, 100, 85]

try:
    average = divide(sum(grades), len(grades))
except ZeroDivisionError:
    print("There are no grades yet in your list.")
else:
    print(f"The average was {average}")


# -- Doing something no matter what --
# This is particularly useful when dealing with resources that you open and then must close
# The `finally` part always runs, so you could use it to close things down
# You can also use it to print something at the end of your try-block if you like.

students = [
    {"name": "Bob", "grades": [75, 90]},
    {"name": "Rolf", "grades": []},
    {"name": "Jen", "grades": [100, 90]},
]

try:
    for student in students:
        name = student["name"]
        grades = student["grades"]
        average = divide(sum(grades), len(grades))
        print(f"{name} averaged {average}.")
except ZeroDivisionError:
    print(f"ERROR: {name} has no grades!")
else:
    print("-- All student averages calculated --")
finally:
    print("-- End of student average calculation --")
```


# Custom error classes 

```python

class Book:
    def __init__(self, name: str, page_count: int):
        self.name = name
        self.page_count = page_count
        self.pages_read = 0

    def __repr__(self):
        return (
            f"<Book {self.name}, read {self.pages_read} pages out of {self.page_count}>"
        )

    def read(self, pages: int):
        self.pages_read += pages
        print(f"You have now read {self.pages_read} pages out of {self.page_count}")


python101 = Book("Python 101", 50)
python101.read(35)
python101.read(50)  # Whaaaat

# -- Errors used to prevent things from happening --


class TooManyPagesReadError(ValueError):
    pass


class Book:
    def __init__(self, name: str, page_count: int):
        self.name = name
        self.page_count = page_count
        self.pages_read = 0

    def __repr__(self):
        return (
            f"<Book {self.name}, read {self.pages_read} pages out of {self.page_count}>"
        )

    def read(self, pages: int):
        if self.pages_read + pages > self.page_count:
            raise TooManyPagesReadError(
                f"You tried to read {self.pages_read + pages} pages, but this book only has {self.page_count} pages."
            )
        self.pages_read += pages
        print(f"You have now read {self.pages_read} pages out of {self.page_count}")


python101 = Book("Python 101", 50)
try:
    python101.read(35)
    python101.read(50)  # This now raises an error, which has a helpful name and a helpful error message.
except TooManyPagesReadError as e:
    print(e)
```
# First Class functions 

```python

# A first class function just means that functions can be passed as arguments to functions.

def calculate(*values, operator):
    return operator(*values)


def divide(dividend, divisor):
    if divisor != 0:
        return dividend / divisor
    else:
        return "You fool!"


# We pass the `divide` function as an argument
result = calculate(20, 4, operator=divide)
print(result)


def average(*values):
    return sum(values) / len(values)


result = calculate(10, 20, 30, 40, operator=average)
print(result)

# -- searching with first-class functions --


def search(sequence, expected, finder):
    for elem in sequence:
        if finder(elem) == expected:
            return elem
    raise RuntimeError(f"Could not find an element with {expected}")


friends = [
    {"name": "Rolf Smith", "age": 24},
    {"name": "Adam Wool", "age": 30},
    {"name": "Anne Pun", "age": 27},
]


def get_friend_name(friend):
    return friend["name"]


print(search(friends, "Bob Smith", get_friend_name))

# -- using lambdas since this can be simple enough --


def search(sequence, expected, finder):
    for elem in sequence:
        if finder(elem) == expected:
            return elem
    raise RuntimeError(f"Could not find an element with {expected}")


friends = [
    {"name": "Rolf Smith", "age": 24},
    {"name": "Adam Wool", "age": 30},
    {"name": "Anne Pun", "age": 27},
]

print(search(friends, "Bob Smith", lambda friend: friend["name"]))


# -- or as an extra, using built-in functions --

from operator import itemgetter


def search(sequence, expected, finder):
    for elem in sequence:
        if finder(elem) == expected:
            return elem
    raise RuntimeError(f"Could not find an element with {expected}")


friends = [
    {"name": "Rolf Smith", "age": 24},
    {"name": "Adam Wool", "age": 30},
    {"name": "Anne Pun", "age": 27},
]

print(search(friends, "Rolf Smith", itemgetter("name")))

```

# Simple Decorators 

```python
user = {"username": "jose", "access_level": "guest"}


def get_admin_password():
    return "1234"


print(get_admin_password())  # Can do this even though I'm a "guest"

# Now this only runs if I'm an admin... but
if user["access_level"] == "admin":
    print(get_admin_password())

print(get_admin_password())  # The function itself is still unsecured

# -- "secure" function --


def secure_get_admin():
    if user["access_level"] == "admin":
        print(get_admin_password())


# Now secure_get_admin() is secure.
# But get_admin_password() is still around, and I could call it:

secure_get_admin()
print(get_admin_password())

# We want to get rid of get_admin_password so that only the secure function remains!
# Maybe something like this?


def secure_function(func):
    if user["access_level"] == "admin":
        return func


user = {"username": "bob", "access_level": "admin"}

get_admin_password = secure_function(get_admin_password)
print(get_admin_password())  # Error!

# When we ran `secure_function`, we checked the user's access level. Because at that point the user was not an admin,
# the function did not `return func`. Therefore `get_admin_password` is set to `None`.

# We want to delay overwriting until we run the function


def get_admin_password():
    return "1234"


def make_secure(func):
    def secure_function():
        if user["access_level"] == "admin":
            return func()

    return secure_function


get_admin_password = make_secure(
    get_admin_password
)  # `get_admin_password` is now `secure_func` from above

user = {"username": "jose", "access_level": "guest"}
print(get_admin_password())  # Now we check access level

user = {"username": "bob", "access_level": "admin"}
print(get_admin_password())  # Now we check access level

# -- More information or error handling --


def get_admin_password():
    return "1234"


def make_secure(func):
    def secure_function():
        if user["access_level"] == "admin":
            return func()
        else:
            return f"No admin permissions for {user['username']}."

    return secure_function


get_admin_password = make_secure(
    get_admin_password
)  # `get_admin_password` is now `secure_func` from above

user = {"username": "jose", "access_level": "guest"}
print(get_admin_password())  # Now we check access level

user = {"username": "bob", "access_level": "admin"}
print(get_admin_password())  # Now we check access level

```

# The 'At' syntax 

```python

user = {"username": "jose", "access_level": "guest"}

def make_secure(func):
    def secure_function():
        if user["access_level"] == "admin":
            return func()
        else:
            return f"No admin permissions for {user['username']}."

    return secure_function


@make_secure
def get_admin_password():
    return "1234"


# -- keeping function name and docstring --
import functools


user = {"username": "jose", "access_level": "guest"}


def make_secure(func):
    @functools.wraps(func)
    def secure_function():
        if user["access_level"] == "admin":
            return func()
        else:
            return f"No admin permissions for {user['username']}."

    return secure_function


@make_secure
def get_admin_password():
    return "1234"

```

# Decorating functions with params

```python

import functools


user = {"username": "jose", "access_level": "guest"}


def make_secure(func):
    @functools.wraps(func)
    def secure_function(panel):
        if user["access_level"] == "admin":
            return func(panel)
        else:
            return f"No admin permissions for {user['username']}."

    return secure_function


@make_secure
def get_password(panel):
    if panel == "admin":
        return "1234"
    elif panel == "billing":
        return "super_secure_password"


# print(get_password("admin"))  # Error before adding parameters, works after
# But now we've coupled our function to our decorator. We can't decorate a different function, which isn't great!
# Instead we could take unlimited parameters and pass whatever we get down to the original function


def make_secure(func):
    @functools.wraps(func)
    def secure_function(*args, **kwargs):
        if user["access_level"] == "admin":
            return func(*args, **kwargs)
        else:
            return f"No admin permissions for {user['username']}."

    return secure_function


@make_secure
def get_password(panel):
    if panel == "admin":
        return "1234"
    elif panel == "billing":
        return "super_secure_password"


print(get_password("admin"))
print(get_password("billing"))

user = {"username": "bob", "access_level": "admin"}

print(get_password("admin"))
print(get_password("billing"))

```

# Decorator with params 

```python
import functools

user = {"username": "anna", "access_level": "user"}


def make_secure(func):
    @functools.wraps(func)
    def secure_function(*args, **kwargs):
        if user["access_level"] == "admin":
            return func(*args, **kwargs)
        else:
            return f"No admin permissions for {user['username']}."

    return secure_function


@make_secure
def get_admin_password():
    return "admin: 1234"


@make_secure
def get_dashboard_password():
    return "user: user_password"


# What if we wanted some passwords to be available to "user" and others to "admin" ?

user = {"username": "anna", "access_level": "user"}


def make_secure(access_level):
    def decorator(func):
        @functools.wraps(func)
        def secure_function(*args, **kwargs):
            if user["access_level"] == access_level:
                return func(*args, **kwargs)
            else:
                return f"No {access_level} permissions for {user['username']}."

        return secure_function

    return decorator


@make_secure(
    "admin"
)  # This runs the make_secure function, which returns decorator. Essentially the same to doing `@decorator`, which is what we had before.
def get_admin_password():
    return "admin: 1234"


@make_secure("user")
def get_dashboard_password():
    return "user: user_password"


print(get_admin_password())
print(get_dashboard_password())

user = {"username": "anna", "access_level": "admin"}

print(get_admin_password())
print(get_dashboard_password())

```

# Mutability 

```python

a = []
b = a

# Remember a and b are _names_ for the list. They both have the _same_ value.

a.append(35)  # Modify the value.

print(a)
print(b)

# We mutated (changed) the value, its names still point to the _same thing_, so it doesn't matter which name you use.

a = []
b = []

a.append(35)

print(a)
print(b)

# Here they are different lists, because [] creates a new list every time. You can check whether two things are the _same_ one by usingt the `id()` function:

print(id(a))
print(id(b))  # Different from id(a)

# -- immutable --

# Some values can't be changed because they don't have methods that modify the value itself.
# In case of the list, `.append()` mutates the list.
# For example integers don't have any such methods, so they are called _immutable_.

a = 8597
b = 8597

print(id(a))
print(id(b))  # Same one

a = 8598

print(id(a))
print(
    id(b)
)  # Different, because we didn't change 8597. We just used the name 'a' for a different value. 'b' still is a name for 8597.

# Most things are mutable in Python. If you want to keep one of your classes immutable, don't add any methods that change the objects' properties.

# Tuples and strings are the only fundamental collection in Python which is immutable.
# Lists, sets, dictionaries are all mutable.
# Integers, floats, and booleans are all immutable.

# -- += and similar --

# A lot of beginners think this:

a = "hello"
b = a

print(id(a))
print(id(b))

a += "world"

# Would cause 'b' to change
# But it doesn't, because strings are immutable. When you do str + str, a _new_ string is created.
# This means that a becomes a new string containing "helloworld", but b still is a name for "hello".

print(id(a))
print(id(b))

```

# Mutability 

```python

a = []
b = a

# Remember a and b are _names_ for the list. They both have the _same_ value.

a.append(35)  # Modify the value.

print(a)
print(b)

# We mutated (changed) the value, its names still point to the _same thing_, so it doesn't matter which name you use.

a = []
b = []

a.append(35)

print(a)
print(b)

# Here they are different lists, because [] creates a new list every time. You can check whether two things are the _same_ one by usingt the `id()` function:

print(id(a))
print(id(b))  # Different from id(a)

# -- immutable --

# Some values can't be changed because they don't have methods that modify the value itself.
# In case of the list, `.append()` mutates the list.
# For example integers don't have any such methods, so they are called _immutable_.

a = 8597
b = 8597

print(id(a))
print(id(b))  # Same one

a = 8598

print(id(a))
print(
    id(b)
)  # Different, because we didn't change 8597. We just used the name 'a' for a different value. 'b' still is a name for 8597.

# Most things are mutable in Python. If you want to keep one of your classes immutable, don't add any methods that change the objects' properties.

# Tuples and strings are the only fundamental collection in Python which is immutable.
# Lists, sets, dictionaries are all mutable.
# Integers, floats, and booleans are all immutable.

# -- += and similar --

# A lot of beginners think this:

a = "hello"
b = a

print(id(a))
print(id(b))

a += "world"

# Would cause 'b' to change
# But it doesn't, because strings are immutable. When you do str + str, a _new_ string is created.
# This means that a becomes a new string containing "helloworld", but b still is a name for "hello".

print(id(a))
print(id(b))

```
