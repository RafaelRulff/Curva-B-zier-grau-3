# Curva-B-zier-grau-3
# Exercício Curva de Bézier grau 3

import tkinter

from tkinter import*

master=Tk()

w=Canvas(master,width=800,height=800)


w.pack()

def kriva():

        P0=[]
        P1=[]
        P2=[]
        P3=[]
        P0.append (float(input(" x for P0")))  #HERE IS THE PLACE FOR INPUT COORDINATES OF CONTROL POINTS
        P0.append (float(input(" y for P0")))
        P1.append(float(input(" x for P1")))
        P1.append(float(input(" yfor P1")))    
        P2.append(float(input(" x for za P2")))
        P2.append(float(input(" y for za P2")))

        P3.append(float(input(" x for P3")))
        P3.append(float(input(" y for P3")))


        for u  in range (0,1000,1):
            u=(u/1000) # PARAMETAR FOR CURVE
               x=(P0[0]*(1-u)**3+P1[0]*3*u*(1-u)**2+P2[0]*3*u**2*(1-u)+P3[0])*u**3#BERNSTAIN    POLYNOMS FOR X AND Y         
               y=(P0[1]*(1-u)**3+P1[1]*3*u*(1-u)**2+P2[1]*3*u**2*(1-u)+P3[1]*u**3)
            x1=x+1 #THIS IS END OF THE LINE
            y1=y+1
            print (x)
            print (y)
            w.create_line(x,y,x1,y1) 

kriva()
mainloop()
