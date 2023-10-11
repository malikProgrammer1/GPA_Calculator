from tkinter import *
from tkinter import ttk

def calculate(*args):
    try:
        value = float(grade.get())
        if value > 100:
          GPA.set("Invalid Grade")
        elif value >= 93:
          GPA.set("4.0")
        elif value >= 90:
          GPA.set("3.7")
        elif value >= 87:
          GPA.set("3.3")
        elif value >= 83:
          GPA.set("3.0")
        elif value >= 80:
          GPA.set("2.7")
        elif value >= 77:
          GPA.set("2.3")
        elif value >= 73:
          GPA.set("2.0")
        elif value >= 70:
          GPA.set("1.7")
        elif value >= 67:
          GPA.set("1.3")
        elif value >= 63:
          GPA.set("1.0")
        elif value >= 60:
          GPA.set("0.7")
        elif value >= 0:
          GPA.set("0.0")
        else:
          GPA.set("Invalid Grade")
    except ValueError:
        pass

root = Tk()
root.title("GPA Calculator")

mainframe = ttk.Frame(root, padding="3 3 12 12")
mainframe.grid(column=0, row=0, sticky=(N, W, E, S))
root.columnconfigure(0, weight=1)
root.rowconfigure(0, weight=1)

grade = StringVar()
grade_entry = ttk.Entry(mainframe, width=7, textvariable=grade)
grade_entry.grid(column=2, row=1, sticky=(W, E))

GPA = StringVar()
ttk.Label(mainframe, textvariable=GPA).grid(column=2, row=2, sticky=(W, E))

ttk.Button(mainframe, text="Calculate", command=calculate).grid(column=2, row=3, sticky=W)

ttk.Label(mainframe, text="/100").grid(column=3, row=1, sticky=W)
ttk.Label(mainframe, text="equals a ").grid(column=1, row=2, sticky=E)
ttk.Label(mainframe, text="GPA").grid(column=3, row=2, sticky=W)

for child in mainframe.winfo_children(): 
    child.grid_configure(padx=5, pady=5)

grade_entry.focus()
root.bind("<Return>", calculate)

root.mainloop()
