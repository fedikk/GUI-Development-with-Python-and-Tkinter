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
