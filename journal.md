# This is my journal

Q1. What did we do

Over the course of our third infoscience lesson we furthered our exploration and understanding of "Processing." After switching the programing language from JAVA to Python, we began to create a die. First, we set the size and set the background colour. Then we had to indlude a draw command. This was so we could set the stroke command to O, thereby making the default line colour white. However, the rest of the code was placed under MouseClicked. First, we set a rectangle that appears once the mouse is clicked. Then, we included a command that chose a number between one and six. Then, after a number is picked, a corresponding number of circles would appear inside the rectangle, with the circles being in the position of a traditional die. Afterwards, we were given a random number to "load." Essentially, we set the number from 6 to 7 and changed the value of our number from a 1 in 6 chance to a 2 in 7. We were then issued two challenges, which will be solved below. The code can also be previewed below.

```py
def setup():
    size (600,600)
    background(255)
    strokeWeight(10)
    
def draw():
    stroke (0)
    

    
def mouseClicked():
    stroke(0)
    rect(100, 100, 400, 400, 50)
    stroke(255, 0, 0)
    n = random(0,7)
    
    if 0<=n<1:
        # number one
         circle (300, 300, 50) # centre
    if 1<=n<2:
        # number two
         circle (200, 200, 50) # top left
         circle (400, 400, 50) # bottom right
    if 2<=n<4:
        # number three
        circle (200, 200, 50) # top left
        circle (300, 300, 50) # centre
        circle (400, 400, 50) # bottom right
    if 3<=n<5:
        # number four
         circle (200, 200, 50) # top left
         circle (400, 400, 50) # bottom right
         circle (400, 200, 50) # top  right
         circle (200, 400, 50) # bottom left
    if 4<=n<6:
        # number five
        circle (200, 200, 50) # top left
        circle (400, 400, 50) # bottom right
        circle (400, 200, 50) # top  right
        circle (200, 400, 50) # bottom left
        circle (300, 300, 50) # centre
        
    if 5<=n<7:
        # number six
        circle (200, 200, 50) # top left
        circle (400, 400, 50) # bottom right
        circle (400, 300, 50) # centre right
        circle (400, 200, 50) # top  right
        circle (200, 300, 50) # centre left
        circle (200, 400, 50) # bottom left
   ```
   
Q2. What did I learn

I learned how to use the stroke and rectangle command. I learned how to add random numbers. I learned that hashtags cause the text placed after to not count as code.

Q3. What questions do I have

What is the size limit for Processing? How would this have been different if it was attempted in JAVA? What is the end goal of this unit? 

For the challanges, the following code was added.

KEEP TRACK OF NUMBER OF TIMES ROLLED/NUMBER OF TIMES EACH SIDE WAS SHOWN WITH BAR GRAPH

```py
ones=0
twos=0
threes=0
fours=0
fives=0
six=0
x=0


def setup():
    size (600,600)
    background(255)
    strokeWeight(10)
    
def draw():
    stroke (0)
    barGraph()
    Total()
    
def barGraph():
    fill(0)
    textSize(20)
    for x in range(6):
        text(x+1,(50+50*x),580) 
        
    strokeWeight(1)    
    stroke(0)
    fill(0)
    rect(50,550 - ones, 14, ones)
    
    stroke(0)
    fill(0)
    rect(100,550 - twos, 14, twos)
    
    stroke(0)
    fill(0)
    rect(150,550 - threes, 14, threes)
    
    stroke(0)
    fill(0)
    rect(200,550 - fours, 14, fours)
    
    stroke(0)
    fill(0)
    rect(250,550 - fives, 14, fives)
    
    stroke(0)
    fill(0)
    rect(300,550 - six, 14, six)
    
def Total():
    textSize(18)
    fill(0)
    text("Rolls:", 400, 570)
    text(x, 500, 570)
    
def click():
    fill(0)
    


    
def mouseClicked():
    global ones, twos, threes, fours, fives, six, x
    stroke(0)
    fill(255)
    rect(100, 100, 400, 400, 50)
    stroke(255, 0, 0)
    n = random(0,6)
    x = x + 1
    
    

    if 0<=n<1:
        # number one
         circle (300, 300, 50) # centre
         ones += 1
         print("Number of times 1 has been rolled:", ones) 
    if 1<=n<2:
        # number two
         circle (200, 200, 50) # top left
         circle (400, 400, 50) # bottom right
         twos +=1 
         print("Number of times 2 has been rolled:", twos)
    if 2<=n<3:
        # number three
        circle (200, 200, 50) # top left
        circle (300, 300, 50) # centre
        circle (400, 400, 50) # bottom right
        threes = threes + 1
        print("Number of times 3 has been rolled:", threes)
    if 3<=n<4:
        # number four
         circle (200, 200, 50) # top left
         circle (400, 400, 50) # bottom right
         circle (400, 200, 50) # top  right
         circle (200, 400, 50) # bottom left
         fours = fours + 1
         print("Number of times 4 has been rolled:", fours) 
    if 4<=n<5:
        # number five
        circle (200, 200, 50) # top left
        circle (400, 400, 50) # bottom right
        circle (400, 200, 50) # top  right
        circle (200, 400, 50) # bottom left
        circle (300, 300, 50) # centre
        fives += 1
        print("Number of times 5 has been rolled:", fives) 
        
        
    if 5<=n<6:
        # number six
        circle (200, 200, 50) # top left
        circle (400, 400, 50) # bottom right
        circle (400, 300, 50) # centre right
        circle (400, 200, 50) # top right
        circle (200, 300, 50) # centre left
        circle (200, 400, 50) # bottom left
        six = six + 1
        print("Number of times 6 has been rolled:", six)
```
Unfortunately, I was not able to figure out how to replace the previous roll with the current one, so at the moment, they overlap. However, I tried my hardest and believe I got something out of the experience.


Thank you
    
