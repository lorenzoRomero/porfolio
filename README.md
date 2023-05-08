# porfolio
#this code makes an abstract art
#this code is usful to help understand abstract concepts
import simplegui
import math
a = 0
print("The theme is an abstract reprensintation on life, the cube gets slower over time with the eye always watching but sun rays of hope shine upon it, and a stick phases through the cube representing the obsticles humanity triumphs over")
def draw_handler(canvas):
    global a
   
    fruits = ["slow", "down", "cube"]
    for x in fruits:
        print(x)
    for x in fruits:
        print(x)
    canvas.draw_polygon([(50, 50),(350, 350)], 1, "white")
    canvas.draw_circle((300, 180), 600, 600, "red", "Black") 
    canvas.draw_circle((300, 180), 60, 60,"red", "Black") 
    canvas.draw_circle((300, 180), 60, 60, "red", "Black") 
    canvas.draw_polygon([(math.cos(a) * 100 + 300, math.sin(a) * 100 + 400), (math.cos(a - (math.pi / 2)) * 100 + 300, math.sin(a - (math.pi / 2)) * 100 + 400),(math.cos(a - math.pi) * 100 + 300, math.sin(a - math.pi) * 100 + 400),(math.cos(a - (3 * math.pi / 2)) * 100 + 300, math.sin(a - (3 * math.pi / 2)) * 100 + 400)], 2, "blue", "blue")
    canvas.draw_line((400- (1 * 10), 200), (200, 400- (1 * 10)), 5, "brown") 
    canvas.draw_line([math.cos(a) * 100 + 300, math.sin(a) * 100 + 400], [math.cos(a) * 100 + 300, math.sin(a) * 100 + 300], 5, "green")
    
    canvas.draw_line([math.cos(a - (math.pi / 2)) * 100 + 300, math.sin(a - (math.pi / 2)) * 100 + 400], [math.cos(a - (math.pi / 2)) * 100 + 300, math.sin(a - (math.pi / 2)) * 100 + 300], 5, "green")
    
    canvas.draw_line([math.cos(a - math.pi) * 100 + 300, math.sin(a - math.pi) * 100 + 400], [math.cos(a - math.pi) * 100 + 300, math.sin(a - math.pi) * 100 + 300], 5, "green")
    
    canvas.draw_line([math.cos(a - (3 * math.pi / 2)) * 100 + 300, math.sin(a - (3 * math.pi / 2)) * 100 + 400], [math.cos(a - (3 * math.pi / 2)) * 100 + 300, math.sin(a - (3 * math.pi / 2)) * 100 + 300], 5, "green")
    
    canvas.draw_polygon([(math.cos(a) * 100 + 300, math.sin(a) * 100 + 300), (math.cos(a - (math.pi / 2)) * 100 + 300, math.sin(a - (math.pi / 2)) * 100 + 300),(math.cos(a - math.pi) * 100 + 300, math.sin(a - math.pi) * 100 + 300),(math.cos(a - (3 * math.pi / 2)) * 100 + 300, math.sin(a - (3 * math.pi / 2)) * 100 + 300)], 2, "yellow", "yellow")
    a = a + math.pi / 94
    canvas.draw_circle((300, 180), 60, 30, "Yellow", "Black") 
    canvas.draw_circle((300, 180), 60, 30, "Yellow", "Black") 
    canvas.draw_circle((300, 180), 60, 30, "Yellow", "Black") 
    canvas.draw_polygon([(50, 50),(350, 350)], 1, "white")
    canvas.draw_polygon([(50, 50),(450, 350)], 1, "white")
    canvas.draw_polygon([(50, 50),(550, 350)], 1, "white")
frame = simplegui.create_frame('Testing', 1000, 1000)
frame.set_canvas_background("Black")
frame.set_draw_handler(draw_handler)
frame.start()
