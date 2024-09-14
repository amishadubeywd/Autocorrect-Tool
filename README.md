# Autocorrect-Tool

from tkinter import *
from textblob import TextBlob

def check_spelling():
    a=TextBlob(spell_check.get())
    spell = Label(window,text="The spelling is checked : ",font=("Arial",20,"bold"),bg="grey")
    spell.pack()
    correct_text = Label(window,text=str(a.correct() ),font=("Times New Roman",28,"bold"),bg="green")
    correct_text.pack()

window = Tk()
window.title("Spelling Autocorrector")
window.geometry("600x500")
window.config(background = "black")

text_heading = Label(window, text = "Spelling Autocorrector", font=("Times New Roman", 30 , "bold"), bg="grey",fg="black")
text_heading.pack()

text_check =  Label(window, text="\-----",font=("Times New Roman", 10,"bold"),bg="black",fg="black")
text_check.pack()

text_check =  Label(window, text="Enter the Spelling : ",font=("Times New Roman", 28,"bold"), bg="yellow",fg="black")
text_check.pack()

text_check =  Label(window, text="-----",font=("Times New Roman", 30,"bold"),bg="black",fg="black")
text_check.pack()
text_check =  Label(window, text="-----------------------------------------------------------------------------------------------------------------------------------------------------------------",font=("Times New Roman", 10,"bold"),bg="black",fg="white")
text_check.pack()

spell_check=Entry(window,font=("Times New Roman",20,"bold"),width=400,bg="white",fg="black")
spell_check.pack()

text_check =  Label(window, text="-----------------------------------------------------------------------------------------------------------------------------------------------------------------",font=("Times New Roman", 10,"bold"),bg="black",fg="white")
text_check.pack()

text_check =  Label(window, text="-----",font=("Times New Roman", 15,"bold"),bg="black",fg="black")
text_check.pack()

check_button=Button(window,text="Check !! ",font=("Arial",20,"bold"),fg="white",bg="red",command=check_spelling)
check_button.pack()

window.mainloop()
