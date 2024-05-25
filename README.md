# Chess-Board

import turtle
from turtle import *

s=Screen()
t=Turtle()
t.speed('fastest')
t.hideturtle()
t.up()
t.goto(-200,-200)
t.down()
t.fd(400)
t.lt(90)
t.fd(400)
t.lt(90)
t.fd(400)
t.lt(90)
t.fd(400)
t.lt(90)

def position(event):
    a, b = event.x, event.y
    return a,b
def small_square():
    for k in range(8):
        for j in range(8):
            if k%2==0:
                if j%2==0:
                    t.fillcolor('black')
                else:
                    t.fillcolor('white')
            else:
                if j%2==0:
                    t.fillcolor('white')
                else:
                    t.fillcolor('black')
            t.begin_fill()
            t.seth(90)
            for i in range(3):
                t.fd(50)
                t.rt(90)
            t.seth(90)
            a,b=t.pos()
            t.end_fill()
        t.up()
        t.goto(a-400,b+50)
        t.down()
small_square()

s.mainloop()
