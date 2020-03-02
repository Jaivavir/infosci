# This is my journal

Q1. What did we do

The lesson itself was not of much consequence, as it simply involved copying the code on the board, and there was no originality involved. Rather, the lesson's value came from the assignment that we were given. We were assigned the task of creating our own optical illusion. Once being given this task, I remembered how I used to draw a series of straight lines in math class and do it in such a way that they appeared to be a curve. After a brief foray into how how this illusion is created, I began work on the code. First, I just wanted to create the full illusion. This was just a matter of creating a square, then creating a series of lines on different points of the square. Then, in order to convert it to mouseClicked, I used an offset value of 10 and replaced the coordinates of the line with the values for x and y. This creates a series of straight lines that 
appear to be a curved lined. The coding can be seen below.

```py
offset = 10
def mouseClicked():
    global offset
    offset += 10
    
def setup():
    size (500, 500)
    background (255)
    stroke (0)


def draw():
    x = 450
    y = 50
    for n in range (45):
        x+=10
        y+=10
    global offset
    for n in range (45):
        x = 450 - offset
        y = 50 + offset
    line (50, 450, 50, 50)
    line (450, 450, 50, 450)
    line ( 450, 50, 50, 50)
    line (450, 50, 450, 450)
    line (50, x, x, 450)
    line (450, y, y, 50)
   ```
   
Q2. What did I learn

I learned/became more familliar with the offset command and am now able to code faster/more accurately. The optical illusion project helped me get into the mindset of a problem-solver, as I was not just copying code; I was making it.

Q3. What questions do I have

What is the future of this unit? Will I be able to attend classes remotely? Is learning to code similar to learning a language?


Thank you
    
