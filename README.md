import colorsys
import turtle

screen = turtle.Screen()
screen.bgcolor("black")
screen.setup(width=800, height=800)

t = turtle.Turtle()
t.speed(0)
t.width(1)
t.hideturtle()

n = 36
h = 0

for i in range(400):
    c = colorsys.hsv_to_rgb(h, 1, 1)
    t.color(c)

    h += 1 / n

    t.forward(i)
    t.left(140)
    t.forward(i)
    t.left(35)
    t.circle(i, 50)

turtle.done()