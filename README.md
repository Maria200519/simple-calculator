# simple-calculator
A simple calculator created by using tkinter
import tkinter as tk
field_text=""
def add_field(sth):
    global field_text
    field_text=field_text+str(sth)
    field.delete("1.0","end")
    field.insert("1.0",field_text)
def calculate():
    global field_text
    result=str(eval(field_text))
    field.delete("1.0","end")
    field.insert("1.0",result)
def clear():
    global field_text
    field_text=""
    field.delete("1.0","end")
root=tk.Tk()
root.geometry("300x300")
root.title("Calculator")
field=tk.Text(root,height=2,width=100)
field.grid(row=1,column=1,columnspan=4)
b1=tk.Button(root,height=3,width=7,text="1",command=lambda:add_field(1))
b1.place(x=1,y=40)
b2=tk.Button(root,height=3,width=7,text="2",command=lambda:add_field(2))
b2.place(x=70,y=40)
b3=tk.Button(root,height=3,width=7,text="3",command=lambda:add_field(3))
b3.place(x=140,y=40)
b4=tk.Button(root,height=3,width=7,text="4",command=lambda:add_field(4))
b4.place(x=1,y=100)
b5=tk.Button(root,height=3,width=7,text="5",command=lambda:add_field(5))
b5.place(x=70,y=100)
b6=tk.Button(root,height=3,width=7,text="6",command=lambda:add_field(6))
b6.place(x=140,y=100)
b7=tk.Button(root,height=3,width=7,text="7",command=lambda:add_field(7))
b7.place(x=1,y=160)
b8=tk.Button(root,height=3,width=7,text="8",command=lambda:add_field(8))
b8.place(x=70,y=160)
b9=tk.Button(root,height=3,width=7,text="9",command=lambda:add_field(9))
b9.place(x=140,y=160)
b0=tk.Button(root,height=3,width=7,text="0",command=lambda:add_field(0))
b0.place(x=70,y=220)
ba=tk.Button(root,height=3,width=7,text="+",command=lambda:add_field("+"))
ba.place(x=210,y=40)
be=tk.Button(root,height=3,width=7,text="=",command=lambda:calculate())
be.place(x=140,y=220)
bc=tk.Button(root,height=3,width=7,text="CLEAR",command=lambda:clear())
bc.place(x=1,y=220)
bs=tk.Button(root,height=3,width=7,text="-",command=lambda:add_field("-"))
bs.place(x=210,y=100)
b_d=bs=tk.Button(root,height=3,width=7,text="/",command=lambda:add_field("/"))
b_d.place(x=210,y=160)
bm=bs=tk.Button(root,height=3,width=7,text="x",command=lambda:add_field("*"))
bm.place(x=210,y=220)
root.mainloop()
