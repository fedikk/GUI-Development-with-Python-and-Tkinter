# Labels in Tkinter 


```python

import tkinter as tk
from tkinter import ttk

# -- Windows only configuration --
try:
    from ctypes import windll
    windll.shcore.SetProcessDpiAwareness(1)
except:
    pass
# -- End Windows only configuration --

root = tk.Tk()
root.resizable(False, False)
root.title("Widget Examples")

# -- Text widgets --

# height is the number of rows of text
text = tk.Text(root, height=8)  # Show what happens if you `.pack()` here, while still assigning to variable.
text.pack()

# Insert content into the text area
text.insert("1.0", "Please enter a comment...")  # Can use \n to insert multiple lines.

# First argument: position within textarea.
# Second argument: text to insert after that position.

# The position is given as two numbers, separated by a `.`.
# First number is the line number, starting at 1.
# Second number is character number within the line, starting at 0.
# So 1.0 is the first line, first character.

# -- Disable text widget --

text["state"] = "disabled"  # "normal" is the counterpart

# -- Get text content --

text_content = text.get("1.0", "end")
print(text_content)

root.mainloop()

```

![image](https://github.com/user-attachments/assets/b75b6b79-81bd-4169-ac18-a26456156452)

# Scrollbar in tkinter 

```python

import tkinter as tk
from tkinter import ttk

# -- Windows only configuration --
try:
    from ctypes import windll
    windll.shcore.SetProcessDpiAwareness(1)
except:
    pass
# -- End Windows only configuration --


root = tk.Tk()
root.grid_columnconfigure(0, weight=1)
root.grid_rowconfigure(0, weight=1)

text = tk.Text(root, height=8)
text.grid(row=0, column=0, sticky="ew")
text.insert("1.0", "Please enter a comment...")

text_scroll = ttk.Scrollbar(root, orient="vertical", command=text.yview)
text_scroll.grid(row=0, column=1, sticky="ns")
text['yscrollcommand'] = text_scroll.set

root.mainloop()

```
![image](https://github.com/user-attachments/assets/1a197134-f310-47e2-b084-64cc9b6a9eb7)

# Separators in TK 

```python
import tkinter as tk
from tkinter import ttk

# -- Windows only configuration --
try:
    from ctypes import windll
    windll.shcore.SetProcessDpiAwareness(1)
except:
    pass
# -- End Windows only configuration --


root = tk.Tk()
root.geometry("600x400")
root.resizable(False,False)
root.title("Tkinter Separators")


root.grid_columnconfigure(0, weight=1)
root.grid_rowconfigure(0, weight=1)

ttk.Label(root, text="hello World !", padding=20).pack()

ttk.Separator(root,orient="horizontal").pack(fill="x")

ttk.Label(root, text="hello World !", padding=20).pack()

ttk.Separator(root,orient="horizontal").pack(fill="x")

root.mainloop()

```

![image](https://github.com/user-attachments/assets/2426b7ef-3dc0-480b-96f0-4c9706e55155)

<blockquote> Dont FORGET </blockquote>

#### create separator with ttk.separator(orient)
#### orient can be "vertical" or "horizental"
#### By default separator are 1px in size 
#### Remember to set fill and sticky property to adjust their size

# CheckButtons in TK

```python
import tkinter as tk
from tkinter import ttk

# -- Windows only configuration --
try:
    from ctypes import windll
    windll.shcore.SetProcessDpiAwareness(1)
except:
    pass
# -- End Windows only configuration --


root = tk.Tk()
root.geometry("600x400")
root.resizable(False,False)
root.title("Tkinter Separators")

selected_option = tk.StringVar()


def print_current_option():
    print(selected_option.get())


check_btn = ttk.Checkbutton(
                            root,
                            text="Click ME!!!", 
                            variable=selected_option,
                            command=print_current_option,
                            onvalue="ON",
                            offvalue="OFF"
                            )
check_btn.pack()

root.mainloop()

```
## On Click 

![image](https://github.com/user-attachments/assets/f1460e1d-bf1c-4b42-aa7b-df73874d982b)

## OFF Click 

![image](https://github.com/user-attachments/assets/4f0e49ad-fb47-41b1-82f3-d463c8c01f5e)


<blockquote> Dont FORGET </blockquote>

#### create check button  with <<ttk.checkbutton(text,variable)>>
#### variable should be  tk.StringVar()
#### Can attach command, a function that runs when the button is checked or unchecked 
#### onvalue and offvalue determinate what value the variable will take 
