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

# Section2 : Python Refresher

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

<blockquote> Be careful the data type by default is **STRING**  </blockquote>

```python
length = input("Length (in feet): ")
length_feet = int (length)
print(length_feet/10.8)
```
