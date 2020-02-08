# This is my journal

Q1. What did we do

Over the course of our second infoscience lesson we were introduced to "Processing." After switching the programing language from JAVA to Python, we began to experiment with circles. First, we had to define the area in which the circles would be housed. This required us to set the size and set the background colour. Then we had to indlude a draw command. This was so the circles would appear randomly, however soon afterward we switched to an action being performed through mouse-clicks. This is why the main portion of the code is underneath def mouseClicked. In order to get the circles to appear in a random location, we assigned each numerical value a corresponding varible, with a value set between 0 and 1000 for the coordinates, 10 and 100 for the size, and 0 and 255 for the colour. In order to correctly mark and indentify our colours, we renamed the varibles myred, myblue, and mygreen respectively. Then, we informed the computer of our intent to make a circle every time we clicked the mouse by including a circles command and the randomized variables we included earlier. Then, in order to get a variety of colors, we used the fill command to mix and match the 3 different primary colours. We then made it so a second cirlce would appear in the exact same place, and inside that circle would be my intials. We then discussed possibly variations and were challanged to add lines from circle to circle and add lines from the circles to the middle, both of which will be covered later.

```py
def setup():
    size (1000,1000)
    background(255)
    
def draw():
    print (" ")
    

def mouseClicked():
    x = random (0,1000)
    y = random (0,1000)
    z = random (10, 100)
    r = random (0, 255)
    g = random (0, 255)
    b = random (0, 255)
    myred = r
    myblue = b
    mygreen  = g
    circle (x ,y ,z)
    fill (myred, mygreen, myblue)
    print (x)

    
    circle (x,y,z)
    fill (0)
    text ("J S", x, y)
   ```
   
Q2. What did I learn

I learned how to add colours to circles, how to perform mouseClicked functions, how to set a background, how to add text, how to make multiple circles appear at once, and how to randomize variables.

Q3. What questions do I have

Can other shapes be made? Can we manipulate the position of the circles in program with arrow keys? How would a calming drug such as Baclofen or Valium affect optiokinetic eye movement?

For the challanges, the following code was added.

ADD LINES FROM CIRCLE TO CIRCLE
```py
 line (500,500, x, y)
 ```

ADD LINES FROM MIDDLE TO CIRCLE
```py
a = random (0,1000)
c = random (0,1000)
d = random (10,100)
circle (a ,c,d)
fill (myred, mygreen, myblue)

    
circle (a,c,d)
fill (0)
text ("J S", a, c)
line (x,y,a,c)
```   
Thank you
    
