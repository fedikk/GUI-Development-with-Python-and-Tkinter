# Creating your first tkinter App

## Setting up the enviorement 

you will create a app.py : 
```python 
import tkinter 
tkinter.__test()
```

![0](https://github.com/user-attachments/assets/e4979e31-f7ff-41f8-89a6-da45846878b3)

## Hello World with tkinter 

```python
import tkinter as tk
import tkinter  as ttk


root = tk.Tk()

#ttk.Label(parent,text=value).pack() pack will put the element in the window 
ttk.Label(root,text="hello,World!").pack()
root.mainloop()

```

![image](https://github.com/user-attachments/assets/4fda7a64-75d9-44d3-b3d9-4fd14702c7ea)

Let's see now after adding the padding : 

```python

import tkinter as tk
import tkinter  as ttk


root = tk.Tk()

#ttk.Label(parent,text=value,padding(x,y)).pack() pack will put the element in the window 
ttk.Label(root, text="hello,World!",padx=30,pady=10).pack()
root.mainloop()

```

![image](https://github.com/user-attachments/assets/edc98720-6001-4406-849c-d5b8f9a6bd49)


## Adding buttons 

```python

import tkinter as tk
import tkinter  as ttk


root = tk.Tk()

#ttk.Label(parent,text=value,padding(x,y)).pack() pack will put the element in the window 
greet_button = ttk.Button(root, text="Greeting Button").pack()

root.mainloop()

```
![image](https://github.com/user-attachments/assets/64743019-8b0a-4c8a-b72b-9a4999ba578c)

### Let's add the command 

```python

import tkinter as tk
import tkinter  as ttk

def greet():
    print("Hello World!!!")

root = tk.Tk()

greet_button = ttk.Button(root, text="Greeting Button", command=greet).pack()

quit_button = ttk.Button(root,text="Quit",command=root.destroy).pack()
root.mainloop()

```
![image](https://github.com/user-attachments/assets/369b6610-0433-4f76-95d2-d8c6c685ddc9)

![image](https://github.com/user-attachments/assets/7f7095bd-cb17-4544-928a-6a9ee113b217)


```python
import tkinter as tk
import tkinter  as ttk

def greet():
    print("Hello World!!!")

root = tk.Tk()

greet_button = ttk.Button(root, text="Greet", command=greet).pack(side="left", fill="y")

quit_button = ttk.Button(root,text="Quit",command=root.destroy).pack(side="left")
root.mainloop()
```

![image](https://github.com/user-attachments/assets/66d16e76-4827-4e6e-8a72-31788c48ab5b)
