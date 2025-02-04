import turtle
import math

# Set up the screen
turtle.bgcolor("black") 
t = turtle.Turtle()
t.speed(0)
t.width(2)

colors = ["red", "orange", "yellow", "green", "blue", "purple"]

def draw_spiral(radius, angle_step):
    for i in range(100):
        t.color(colors[i % len(colors)])  # Cycle through colors
        t.forward(radius + i * 2)
        t.right(angle_step)

# Draw the spiral pattern
draw_spiral(5, 59)
t.hideturtle()

# Move to bottom of the screen to add text
t.penup()
t.goto(0, -300)
t.color("white")
t.write("Turtle Spiral!", align="center", font=("Arial", 24, "bold"))

turtle.done()
