from tkinter import ttk
from tkinter import *
from tkinter import messagebox
import pyttsx3
import time
import tkinter  as tk
#from PIL import Image, ImageTk #module for jpg image


engine = pyttsx3.init()
engine.say('Good Morning all Teachers..')
engine.runAndWait()

def login(): #window 1 function
    username=entry1.get()
    password=entry2.get()

    if(username=="" and password==""):
        messagebox.showerror("","Blank Not Allowed")
        engine.say('Blank Not Allowed')
        engine.runAndWait()
    elif (username=="k" and password=="1"):

        messagebox.showinfo("","Login Successful ")

        def register(): #window 2 submmited button
            choice = name_ent.get()
            choice1 = var.get()
            choice2 = snumber.get()
            choice3 = dt.get()
            choice4 = var1.get()
            choice5 = Tin.get()
            choice6 = Tout.get()
            choice7 = snu1_ent.get()

            if choice == "":
                messagebox.showerror("Error!","Please Enter Student name")
            elif choice5 == "":
                messagebox.showerror("Error!", "Please Enter Time in section")
            elif choice7 == "":
                messagebox.showerror("Error!","Please Fill No. Of Student Section")
            else :
                messagebox.showinfo("Sucessfull","Submmited sucessfull")
            print(f"{name_ent.get(),var.get(),namedt_ent.get(), snu1_ent.get(),var1.get(),dt.get(),Tin.get(),Tout.get()}\n")
            with open("reco.txt", "a") as f:
                f.write("\n\nName:  "+name_ent.get())
                f.write("\nAbsent Present or Late:  "+var.get())
                f.write("\nEnrollment Number:  "+namedt_ent.get())
                f.write("\nNO. OF DAYS OF STUDENT:  "+snu1_ent.get())
                f.write("\nStudent Branch :  "+var1.get())
                f.write("\nDATE :  " + dt.get())
                f.write("\nTime In :  "+Tin.get())
                f.write("\nTime OUT :  "+Tout.get())


        def clear(): #w2 clear btn

            name_ent.delete(0, END)
            namedt_ent.delete(0,END)
            Tin.delete(0,END)
            snu1_ent.delete(0,END)

            engine.say('Clear')
            engine.runAndWait()
        def change(): #w2 change color btn
            choice = entry3.get()
            if choice == "red":
                new_windows.configure(bg="red")
            if choice == "red":
                engine.say('Red color')
                engine.runAndWait()
            if choice == "orange":

                new_windows.configure(bg="orange")
            if choice == "orange":
                engine.say('orange color')
                engine.runAndWait()

            if choice == "yellow":
                new_windows.configure(bg="yellow")
            if choice == "yellow":
                engine.say('yellow color')
                engine.runAndWait()
            if choice == "green":
                new_windows.configure(bg="green")
            if choice == "green":
                engine.say('green color')
                engine.runAndWait()
            if choice == "blue":
                new_windows.configure(bg="blue")
            if choice == "blue":
                engine.say('blue color')
                engine.runAndWait()
            if choice == "magenta":
                new_windows.configure(bg="magenta")
            if choice == "magenta":
                engine.say('magenta color')
                engine.runAndWait()
            if choice == "purple":
                new_windows.configure(bg="purple")
            if choice == "purple":
                engine.say('pueple color')
                engine.runAndWait()
            if choice == "brown":
                new_windows.configure(bg="brown")
            if choice == "brown":
                engine.say('brown color')
                engine.runAndWait()
            if choice == "pink":
                new_windows.configure(bg="pink")
            if choice == "pink":
                engine.say('pink color')
                engine.runAndWait()
            if choice == "black":
                new_windows.configure(bg="black")
            if choice == "black":
                engine.say('black color')
                engine.runAndWait()

            if choice == "violet":
                new_windows.configure(bg="violet")
            if choice == "violet":
                engine.say('violet color')
                engine.runAndWait()
                engine.runAndWait()
            if choice == "cyan":
                new_windows.configure(bg="cyan")
            if choice == "cyan":
                engine.say('cyan color')
                engine.runAndWait()
            if choice == "white":
                new_windows.configure(bg="white")
            if choice == "white":
                engine.say('white color')
                engine.runAndWait()

            if choice == "silver":
                new_windows.configure(bg="silver")
            if choice == "silver":
                engine.say('silver color')
                engine.runAndWait()

            if choice == "royal blue":
                new_windows.configure(bg="royal blue")
            if choice == "royal blue":
                engine.say('royal blue color')
                engine.runAndWait()
            if choice == "gray":
                new_windows.configure(bg="gray")
            if choice == "gray":
                engine.say('gray color')
                engine.runAndWait()


            if choice == "khaki":
                new_windows.configure(bg="khaki")
            if choice == "khaki":
                engine.say('khaki color')
                engine.runAndWait()

            if choice == "chocolate":
                new_windows.configure(bg="chocolate")
            if choice == "chocolate":
                engine.say('chocolate color')
                engine.runAndWait()

        def about():
            engine.say('This App Is Made By Diploma Last Year Students.... Kartikey Shukla..Ritik Singh..Shubham Singh')
            engine.runAndWait()
            messagebox.showinfo("Message","This App Is Made By Diploma Last Year Students.... Kartikey Shukla,Ritik Singh,Shubham Singh")
        new_windows = Toplevel(root) #making window 2
        new_windows.geometry("990x560")
        def percentage():
            new_windows1 = Toplevel(root)  # making window 2
            new_windows1.geometry("700x600")
            new_windows1.title("Percentage section")
            new_windows1.configure(bg="gray")
            heading = Label(new_windows1, text="Percentage Section", font="arial 30 bold", bg="blue",
                            fg="yellow")  # bg="#000" for black color
            heading.pack(fill=X)

            classh = Label(new_windows1, text="Number of class held", font="comicsansms 13 bold")
            classa = Label(root, text="Number of class attend of student", font="comicsansms 13 bold")
            # name of our form
            classh = Label(new_windows1, text="Number of class held", font="comicsansms 13 bold", bg="yellow")
            classh.place(x=320, y=100)
            classa = Label(new_windows1, text="Number of class attend of student ", font="comicsansms 13 bold", bg="yellow")
            classa.place(x=310, y=160)
            # Entries

            classh = Entry(new_windows1, bd=6)
            classh.place(x=530, y=100)

            classa = Entry(new_windows1, bd=6)
            classa.place(x=600, y=160)
            def clear():
                classh.delete(0, END)
                classa.delete(0, END)

            def percentage():
                choice = classa.get()
                choice1 = classh.get()
                a = int(classh.get())
                b = int(classa.get())
                percentage = b / a * 100

                Label(new_windows1,text=f"{percentage}", font="arial 30 bold", fg="blue").place(x=400, y=500)

                if percentage >= 75:
                    engine.say('Good Luck,The student is allowed to sit in the exam hall')
                    engine.runAndWait()
                    messagebox.showinfo("Good luck", "The student is allowed to sit in the exam hall")

                if percentage > 100:
                    engine.say('Error,Please Cheack Your Entry Your Entry Is More Than 100 %')
                    engine.runAndWait()
                    messagebox.askretrycancel("Error", "Please Cheack Your Entry Your Entry Is More Than 100 %..")

                if percentage < 75:
                    engine.say(
                        'bad luck,The student is not allowed to sit in the exam hall beacause the attandace is less than 75%')
                    engine.runAndWait()
                    # Label(text=f"{percentage}", font="arial 60 bold", fg="red").place(x=400, y=600)
                    messagebox.showerror("bad luck","The student is not allowed to sit in the exam hall beacause the attandace is less than 75%")


            Button(new_windows1, text="Calculate percentage", bg="green", command=percentage, height=3, width=18, bd=6,
                   font=("Arial", 13)).place(x=400, y=250)
            Button(new_windows1, text="clear", bg="red", command=clear, height=3, width=14, bd=6, font=("Arial", 13)).place(
                x=400, y=350)



        global entry3 #Entry 3 is for changing color
       # new_windows.wm_iconbitmap("2.ico")




        new_windows.configure(bg="black")
        heading = Label(new_windows, text="WELCOME TO SORT ATTENDANCE REGISTER", font="arial 40 bold", bg="blue", fg="yellow")  # bg="#000" for black color
        heading.pack(fill=X)
        Label(new_windows, font=("arial", 15, "bold"), text="current time:", bg="papaya whip").place(x=10, y=70)
        new_windows.title("Attendance Section")



        #name of form

        name = Label(new_windows, text="STUDENT FULLL NAME", font="comicsansms 13 bold",bg="yellow")
        name.place(x=310,y=104)
        absent = Label(new_windows, text="ABSENT PRESENT,LATE ", font="comicsansms 13 bold",bg="yellow")
        absent.place(x=310,y=160)
        snumber = Label(new_windows, text="ENROLLMENT NUMBER", font="comicsansms 13 bold",bg="yellow")
        snumber.place(x=310,y=220)
        snu1 = Label(new_windows, text="DAYS OF STUDENT", font="comicsansms 13 bold",bg="yellow")
        snu1.place(x=310,y=280)
        entry3 = Label(new_windows, text="Window color change ", font="comicsansms 13 bold", bg="yellow")
        entry3.place(x=880, y=100)
        branch = Label(new_windows, text="STUDENT BRANCH", font="comicsansms 13 bold",bg="yellow")
        branch.place(x=310, y=340)

        dt = Label(new_windows, text="TODAY DATE",font="comicsansms 13 bold", bg="yellow")
        dt.place(x=310, y=400)


        Tin = Label(new_windows, text="Time IN ", font="comicsansms 13 bold", bg="yellow")
        Tin.place(x=310, y=450)
        Tout = Label(new_windows, text="Time OUT", font="comicsansms 13 bold", bg="yellow")
        Tout.place(x=310, y=500)

        # Tkinter variable for storing entries
        name = StringVar()
        var = StringVar()
        var.set("Empty")
        snumber = StringVar()
        snumber.set("PU -              ")
        dt = StringVar()
        dt.set("        /       /       ")  #set date
        entry3 = StringVar()
        var1 = StringVar()
        var1.set("Empty")


        # Entries for our form

        name_ent = ttk.Combobox(new_windows, font=('Arial', 10), width=20,
                                  )  # state="readonly" jb koi value ko fix
        name_ent['value'] = ("Kartikey", "Ritik", "Shubham","Mukesh","Vishal","Sunny","M.D" ,"Adil Alam")

        name_ent.place(x=530,y=107)

        radio1 = Radiobutton(new_windows, text="Absent", padx=10, variable=var, value="Absent",bg="red")
        radio1.place(x=550,y=162)
        radio2 = Radiobutton(new_windows, text="Present", padx=14, variable=var, value="Present",bg="green")
        radio2.place(x=650,y=162)

        radio3 = Radiobutton(new_windows, text="Late", padx=14, variable=var, value="Late",bg="yellow")
        radio3.place(x=770,y=162)
        radio4 = Radiobutton(new_windows, text="Diploma", padx=14, variable=var1, value="Diploma", bg="green")
        radio4.place(x=510, y=340)
        dt = Entry(new_windows, bd=6, textvariable=dt)
        dt.place(x=500, y=400)
        Tin = Entry(new_windows, bd=6, textvariable=Tin)
        Tin.place(x=500,y=450)
        Tout = Entry(new_windows, bd=6, textvariable=Tout)
        Tout.place(x=500, y=500)

        namedt_ent = ttk.Combobox(new_windows, font=('Arial', 10), width=22)  # state="readonly" jb koi value ko fix
        namedt_ent['value'] = ("Kartikey PU-062162005C2", "Ritik PU-063162005C2", "Shubham", "Mukesh", "Vishal", "Sunny", "M.D Adil Alam")

        namedt_ent.place(x=530, y=220)
        snu1_ent = ttk.Combobox(new_windows, font=('Arial', 10), width=15,height=5)  # state="readonly" jb koi value ko fix
        snu1_ent['value'] = ("1","2","3","4","5","6","7","8","9","10","11","12","13","14","15","16","17","18","19","20"
                             ,"21","22","23","24","25","26","27","28","29","30","31")
        snu1_ent.place(x=550, y=280)
        entry3 = ttk.Combobox(new_windows, font=('Arial', 10), width=20,
                                height=8)  # state="readonly" jb koi value ko fix
        entry3['value'] = ("red","orange","cyan","chocolate","royal blue","pink","blue","green","black","white","cyan",
                           "magenta","brown","violet","khaki","gray","silver","yellow")
        entry3.place(x=1070, y=100)


        #making button
        Button(new_windows, text="Submitted", bg="green", command=register, font="comicsansms 13 bold", height=3,width=13, bd=6).place(x=800, y=500)
        Button(new_windows, text="Clear", bg="red", command=clear, font="comicsansms 13 bold", height=3, width=13,bd=6).place(x=980, y=500)
        Button(new_windows, text="Change color", bg="orange red", command=change, font="comicsansms 13 bold", height=3, width=13,bd=6).place(x=1080, y=200)
        Button(new_windows, text="About This App", bg="green", command=about, font="comicsansms 13 bold", height=3, width=13,bd=6).place(x=1160, y=500)
        Button(new_windows, text="Go To Percentage Section", bg="goldenrod3", command=percentage,
               font="comicsansms 13 bold", height=3, width=22, bd=5).place(x=970, y=600)

        #making clock
        def clock():
            clock_time = time.strftime('%I:%M:%S %p - Date: %x')  # I is for 12 hours formate. #x is for date
            # M is for minutes
            # S is for seconds and # P is for Locale’s AM or PM.
            current_time.config(text=clock_time,bg="tan") #tan is a color
            current_time.after(1000, clock) #for run time
        current_time = Label(new_windows, font=("arial", 15, "bold"), text="", fg="#000", bg="#fff")
        current_time.place(x=139, y=70)
        clock()
    else:
        messagebox.showerror("Error","Error Wrong Password")
def del1():
    entry1.delete(0, END)
    entry2.delete(0, END)
root = Tk()
root.geometry("600x400") #making window 1
root.title("Login Form")
#root.wm_iconbitmap("login.ico")
root.configure(bg="black")
root.resizable(FALSE,FALSE)

heading = Label(root, text="WELLCOME TO SCHOOL OF RESEARCH AND TECHNOLOGY", font="arial 15 bold", bg="blue",
                fg="white")
heading.pack(fill=X)

global entry1
global entry2
Label(root,text= "User Name",bg="green",font="arial 15 bold ").place(x=90,y=80)
Label(root,text= "Password",bg="green",font="arial 15 bold ").place(x=90,y=160)
def show_pass():
    if entry2.cget('show') == '*':
        entry2.config(show='')
    else:
        entry2.config(show='*')
entry1=Entry(root,bd=5)
entry1.config(bg="yellow")
entry1.place(x=250,y=80)
entry2=Entry(root,bd=5,show='*')
entry2.config(bg="yellow")
entry2.place(x=250,y=160)
cheack_button = Checkbutton(root,text="Show Password",bg="orange",command=show_pass,bd=5)
cheack_button.place(x=90,y=200)

Button(root,text="Login",bg="green",command=login,height=3,width=13,bd=6).place(x=200,y=250)
Button(root,text="Clear",bg="red",command=del1,height=3,width=13,bd=6).place(x=200,y=330)
root.mainloop()
