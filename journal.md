# This is my journal

Bears:
```py
x = ()

for x in range (1):
    print 'bears', (x)
for x in range (1,2):
    print 'bear', (x)
for x in range (2, 101):
    print 'bears', (x)
```
The year is code
```py
x = ()

for x in range (1900, 2001):
    print 'The year is', (x)
```
Celcius to Farenheit
```py
for C in range (100):
    F = C * 1.8 + 32
    print C,'C are', 'F', F
```
3. Complete the table below for 5 different simulation where the number of people moving changes 

Case Number 1: 
   Number of people moving: 1
   Population Size: 25
   Iterations until complete infection: 2597
Case Number 2:
   Number of people moving: 3
   Population Size: 25
   Iterations until complete infection: 860
Case Number 3:
   Number of people moving: 8
   Population Size: 25
   Iterations until complete infection: 153
Case Number 4:
   Number of people moving: 12
   Population Size: 25
   Iterations until complete infection: 91
Case Number 5:
   Number of people moving: 17
   Population Size: 25
   Iterations until complete infection: 98
   
   
4. What conclusion can you draw from the simulations you run in step 3. Explain.

The more people move, the faster everyone gets infected. To vizualize this let us take the example of only 1 person moving. This means that this 1 moving person needs to visit every other person. If we move on to two people, once this second person gets infected and starts moving, now there are two people who not only have the infection, but can spread it. So this simulation represents the duality of an infection. It's not only about who have you infected; It's about who they can spread it to.

5. Propose another table of simulations. Variables we can change include: population size, distance of infection, movement size, number of people moving.  

Distance if infection: 10
Population Size: Varies 
Number of people moving: 10
Area: (2000, 2000)


What did we do?
We learned about forward loops, and did mini coding segments in order to familiarize ourselves with them. We updated the infection code so the infection could spread between people, and we ran trial simulations to see how the spread of the infection changed when the number of people moving changed. We then answered some questions about the trial. Below is the updated infection code.
```py
# definition of variables
x = []
y= []
per = [False, True] #False=>infected
inf = 0
hel = 25
con = 0
bar = 0

def setup():
    size(500,500)
    for n in range (25):
        x.append(random(0, 500))
        per.append(True) #All Healthy
        y.append(random(0, 500))
        barGraph()
        

        
def distance(x1, x2, y1, y2):
    a = (x1 - x2)
    b = (y1 - y2)
    c = sqrt(a**2 + b**2)
    return c


    
    
def draw():
    global x, y, inf, hel, con, l
    background(255)
    strokeWeight(2)
    barGraph()
    con += 1
    if inf == 25:
        con -= 1


    
    #create 1st individual
    for i in range(0, 25):
        if per[i] == True:
            fill(255) #healthy
        else:
            fill (0, 200, 0) #infected

            
            
        circle(x[i], y[i], 40)
        
        x[0] = x[0] + random(-10, 10)
        y[0] = y[0] + random(-10, 10)

        
        for g in range(len(x)):
            if g == i:
                continue
            d = distance(x[i], x[g], y[i], y[g])
            if d < 40 and (per[g] == False or per[i]== False):
                #infection happens
                per[i] = False
                per[g] = False

        
        #boundaries conditions
        if x[i] > 500:
            x[i] = 500
    
        # add three more extentions
        
        if x[i] < 0:
            x[i] = 0
            
        if y[i] > 500:
            y[i] = 500
    
        if y[i] < 0:
            y[i] = 0
            
    inf = 0
    hel = 25
    for bar in range (25):
        if per[bar] == False:
            inf += 1
            hel -= 1
            
    textSize(10)
    fill(0)
    text("Infected", 445, 478)
    text("Healthy", 445, 458)
    text (con, 80, 470)
    text("Iteration #:", 20, 470)
    

def barGraph():
    strokeWeight(1)
    stroke(0)
    fill(255, 0, 0)
    rect (440, 470, -inf*2, 8)
    fill (255)
    rect (440, 450, -hel*2, 8)
```
This code almost exactly follows the lesson plan, however one innovation I made was making the counter stop after every single circle was infeted. This made it so that I could tell on exactly what iteration every person was infected. This made filling out the simulation table much easier.

What did I learn?
I learned about forward loops. I learned how to use different operators. I learned how the movement of individuals contributes to the spread of an infection. 

What questions do I have?
What is the next task going to be? What different kinds of operators are there? 
