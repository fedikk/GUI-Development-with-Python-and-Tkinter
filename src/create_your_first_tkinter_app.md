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


```python
import tkinter as tk
import tkinter  as ttk

def greet():
    print("Hello World!!!")

root = tk.Tk()

greet_button = ttk.Button(root, text="Greet", command=greet).pack(side="left", fill="both",expand=True)

quit_button = ttk.Button(root,text="Quit",command=root.destroy).pack(side="left",fill="both",expand=True)
root.mainloop()

```
![image](https://github.com/user-attachments/assets/8fffb0ae-cb81-416e-8d63-f8b8effff224)


# Creating a Greating App 

```python
import tkinter as tk
import tkinter  as ttk

def greet():
    print(f"Hello {user_name.get()}!!!")

root = tk.Tk()

user_name = tk.StringVar()

name_label = ttk.Label(root,text="Name: ")
name_label.pack(side="left",padx=(0,10))
name_entry = ttk.Entry(root, width=15, textvariable=user_name)
name_entry.pack(side="left")
name_entry.focus()


greet_button = ttk.Button(root, text="Greet", command=greet).pack(side="left", fill="both",expand=True)

quit_button = ttk.Button(root,text="Quit",command=root.destroy).pack(side="left",fill="both",expand=True)


root.mainloop()
```

![image](https://github.com/user-attachments/assets/2ccbeb67-11c8-4147-a532-49fe378cc1d6)

# Packing components

![image](https://github.com/user-attachments/assets/e55748d7-345c-47dd-b366-3da4c1c2e65e)

![image](https://github.com/user-attachments/assets/c5f30725-4004-490a-a5fa-e15a7ac6ec38)

![image](https://github.com/user-attachments/assets/aa152c81-832e-4da0-a45a-e2de74aef879)

![image](https://github.com/user-attachments/assets/45edc969-ce7e-4313-9d9b-77c7b7fb3f57)

![image](https://github.com/user-attachments/assets/33bb8089-1f82-4a0b-999a-0483212e859d)

![image](https://github.com/user-attachments/assets/a196ba88-bd4f-47c8-b1da-1ca9c285a9cf)

![image](https://github.com/user-attachments/assets/cf1b9330-d38e-43e8-8646-ce54ae38ebb9)

![image](https://github.com/user-attachments/assets/709ee58b-fbcc-493b-80f0-10fdd135a333)

![image](https://github.com/user-attachments/assets/3aca45e0-7aca-4aff-84c8-a0107e15f834)

![image](https://github.com/user-attachments/assets/6a5e6a64-de7e-4a8d-9d0f-843d7457fa30)

![image](https://github.com/user-attachments/assets/eee61b4f-21cb-4b04-9bec-a5f09e5c39df)

![image](https://github.com/user-attachments/assets/42fafb92-9b85-49e7-9930-96e71c3923c5)

![image](https://github.com/user-attachments/assets/afe0f629-727c-4737-ad05-1b5ff3482205)

![image](https://github.com/user-attachments/assets/0bb10b58-2c0a-40d9-a0a7-6ae0cfc76b66)

# Packing componants with frames 

```python
import tkinter as tk
import tkinter  as ttk


root = tk.Tk()

tk.Label(root, text="label top",bg="red").pack(side="top",fill="both",expand=True)
tk.Label(root, text="label top",bg="red").pack(side="top",fill="both",expand=True)
tk.Label(root, text="label left",bg="green").pack(side="left",fill="both",expand=True)


root.mainloop()
```

![image](https://github.com/user-attachments/assets/ac6d330e-392a-454b-bc12-85649e0c2411)

Let's add Frame now : 

```python
import tkinter as tk
import tkinter  as ttk


root = tk.Tk()

main = ttk.Frame(root)
main.pack(side="left",fill="both",expand=True)
tk.Label(main, text="label top",bg="red").pack(side="top",fill="both",expand=True)
tk.Label(main, text="label top",bg="red").pack(side="top",fill="both",expand=True)
tk.Label(root, text="label left",bg="green").pack(side="left",fill="both",expand=True)


root.mainloop()

```

![image](https://github.com/user-attachments/assets/5e0b4756-e646-4d8b-8719-c76cc88ac1a7)

```python

import tkinter as tk
import tkinter  as ttk


root = tk.Tk()

navbar = ttk.Frame(root)
navbar.pack(side="left",fill="both",expand=True)
tk.Label(navbar, text="Home",bg="black",fg="white").pack(side="top",fill="both",expand=True)
tk.Label(navbar, text="Config",bg="black",fg="white").pack(side="top",fill="both",expand=True)
tk.Label(navbar, text="Help",bg="black",fg="white").pack(side="top",fill="both",expand=True)
tk.Label(navbar, text="close",bg="black",fg="white").pack(side="top",fill="both",expand=True)
tk.Label(root, text="Main App",bg="green").pack(side="left",fill="both",expand=True)


root.mainloop()

```

![image](https://github.com/user-attachments/assets/45a6f198-bcc0-4696-8cff-1ff81df073a8)

# Greeting app using frames 

```python
import tkinter as tk
import tkinter  as ttk

def greet():
    print(f"Hello {user_name.get()}!!!")

root = tk.Tk()

user_name = tk.StringVar()

input_frame = ttk.Frame(root, padx=20,pady=20)
input_frame.pack( fill="both")



name_label = ttk.Label(input_frame,text="Name: ")
name_label.pack(side="left",padx=(0,10))
name_entry = ttk.Entry(input_frame, width=15, textvariable=user_name)
name_entry.pack(side="left")
name_entry.focus()


button_frame = ttk.Frame(root, padx=20,pady=10)
button_frame.pack( fill="both")

greet_button = ttk.Button(button_frame, text="Greet", command=greet).pack(side="left", fill="x",expand=True)

quit_button = ttk.Button(button_frame,text="Quit",command=root.destroy).pack(side="right",fill="x",expand=True)


root.mainloop()

```

![image](https://github.com/user-attachments/assets/d6397ba4-9e36-4f5d-97f5-ec366dbd1ae9)

# The Grid geometry manager

```python
import tkinter as tk
import tkinter  as ttk

def greet():
    print(f"Hello {user_name.get()}!!!")

root = tk.Tk()

user_name = tk.StringVar()

input_frame = ttk.Frame(root, padx=20,pady=20)
input_frame.grid()



name_label = ttk.Label(input_frame,text="Name: ")
name_label.grid(padx=(0,10))


name_entry = ttk.Entry(input_frame, width=15, textvariable=user_name)
name_entry.grid()
name_entry.focus()


button_frame = ttk.Frame(root, padx=20,pady=10)
button_frame.grid( )

greet_button = ttk.Button(button_frame, text="Greet", command=greet).grid()

quit_button = ttk.Button(button_frame,text="Quit",command=root.destroy).grid()


root.mainloop()

```
![image](https://github.com/user-attachments/assets/d5c3ebcf-f07a-42d2-be5b-322b1e16cb24)

```python
import tkinter as tk
import tkinter  as ttk

def greet():
    print(f"Hello {user_name.get()}!!!")

root = tk.Tk()
root.title("Greeter")

root.columnconfigure(0, weight=1)



user_name = tk.StringVar()

input_frame = ttk.Frame(root, padx=20,pady=20)
input_frame.grid(row=0,column=0)



name_label = ttk.Label(input_frame,text="Name: ")
name_label.grid(row=0,column=0,padx=(0,10))


name_entry = ttk.Entry(input_frame, width=15, textvariable=user_name)
name_entry.grid(row=0,column=1)
name_entry.focus()


button_frame = ttk.Frame(root, padx=20,pady=10)
button_frame.grid()

greet_button = ttk.Button(button_frame, text="Greet", command=greet).grid(row=0,column=0)

quit_button = ttk.Button(button_frame,text="Quit",command=root.destroy).grid(row=0,column=1)


root.mainloop()

```
![image](https://github.com/user-attachments/assets/cbe6be9e-5d9e-42d9-9212-8a06cdeaf283)

### Sticky buttons 

```python

import tkinter as tk
import tkinter  as ttk

def greet():
    print(f"Hello {user_name.get()}!!!")

root = tk.Tk()
root.title("Greeter")

root.columnconfigure(0, weight=1)



user_name = tk.StringVar()

input_frame = ttk.Frame(root, padx=20,pady=20)
input_frame.grid(row=0,column=0)



name_label = ttk.Label(input_frame,text="Name: ")
name_label.grid(row=0,column=0,padx=(0,10))


name_entry = ttk.Entry(input_frame, width=15, textvariable=user_name)
name_entry.grid(row=0,column=1)
name_entry.focus()


button_frame = ttk.Frame(root, padx=20,pady=10)
button_frame.grid(sticky="EW")

greet_button = ttk.Button(button_frame, text="Greet", command=greet).grid(row=0,column=0)

quit_button = ttk.Button(button_frame,text="Quit",command=root.destroy).grid(row=0,column=1)


root.mainloop()

```
![image](https://github.com/user-attachments/assets/45327325-d4a2-4204-be15-26a6d187bfe9)

# Sticky & columnconfigure

```python
import tkinter as tk
import tkinter  as ttk

def greet():
    print(f"Hello {user_name.get()}!!!")

root = tk.Tk()
root.title("Greeter")

root.columnconfigure(0, weight=1)



user_name = tk.StringVar()

input_frame = ttk.Frame(root, padx=20,pady=20)
input_frame.grid(row=0,column=0)



name_label = ttk.Label(input_frame,text="Name: ")
name_label.grid(row=0,column=0,padx=(0,10))


name_entry = ttk.Entry(input_frame, width=15, textvariable=user_name)
name_entry.grid(row=0,column=1)
name_entry.focus()


button_frame = ttk.Frame(root, padx=20,pady=10)
button_frame.grid(sticky="EW")

button_frame.columnconfigure(0,weight=1)
button_frame.columnconfigure(1,weight=1)

greet_button = ttk.Button(button_frame, text="Greet", command=greet).grid(row=0,column=0,sticky="EW")

quit_button = ttk.Button(button_frame,text="Quit",command=root.destroy).grid(row=0,column=1,sticky="EW")


root.mainloop()

```
![image](https://github.com/user-attachments/assets/8f9eff42-f189-4c30-a1de-d5a1a8784521)
