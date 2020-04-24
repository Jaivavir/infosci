# This is my journal

What did we do?

We expanded on our knowledge of the append function, and added a recovered stage for the simulated patients. We learned about strings, and how they can be utilized inside of code. Below is the updated infection code.

```py
# definition of variables
x = []
y= []
per = ["Sick", "Healthy"] #Sick=>infected
inf = 0
hel = 25
rec = 0
con = 0
bar = 0
days = [200, -1]

def setup():
    size(500,500)
    for n in range (25):
        x.append(random(0, 500))
        per.append("Healthy") #All Healthy
        y.append(random(0, 500))
        days.append(200)
        barGraph()
        

        
def distance(x1, x2, y1, y2):
    a = (x1 - x2)
    b = (y1 - y2)
    c = sqrt(a**2 + b**2)
    return c


    
    
def draw():
    global x, y, inf, hel, con, l, days, rec
    background(255)
    strokeWeight(2)
    barGraph()
    con += 1
    if inf == 25:
        con -= 1


    
    #create 1st individual
    for i in range(len(x)):
        if per[i] == "Healthy":
            fill(255) #healthy
        elif per[i] == "Recovered":
            fill(0,255,255)
        else:
            fill (0, 200, 0) #infected
                
        if per[i] == "Sick":
            days[i] -= 1
            if days[i] == 0:
                per[i] = "Recovered"

            
            
        circle(x[i], y[i], 40)
        
        x[i] = x[i] + random(-10, 10)
        y[i] = y[i] + random(-10, 10)

        
        for g in range(len(x)):
            if g == i:
                continue
            d = distance(x[i], x[g], y[i], y[g])
            if d < 40 and (per[g] == "Sick" or per[i]== "Sick"):
                if per[i] == "Healthy":
                    #infection happens
                    per[i] = "Sick"
                    days[i] = 200
                if per[g] == "Healthy":        
                    per[g] = "Sick"
                    days[g] = 200

        
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
    hel = 0
    rec = 0
    for bar in range (len(x)):
        if per[bar] == "Sick":
            inf += 1
        elif per[bar] == "Healthy":
            hel += 1
        elif per[bar] == "Recovered":
            rec += 1

            

            
            
    textSize(10)
    fill(0)
    text("Infected", 445, 478)
    text("Healthy", 445, 458)
    text ("Recovered", 445, 496)
    text (con, 80, 470)
    text("Iteration #:", 20, 470)

            
    

def barGraph():
    strokeWeight(1)
    stroke(0)
    fill(255, 0, 0)
    rect (440, 469, -inf*2, 8)
    fill (255)
    rect (440, 450, -hel*2, 8)
    fill (0, 255, 255)
    rect (440, 488, -rec*2, 8)
    
```
This code almost exactly follows the lesson plan, however one innovation I made was switching the days required for recovery to 200, as this would allow the infection to actually spread among the population before being completely wiped out. Here is a [link to pictures of the working code.](https://drive.google.com/open?id=1J7tl9ffKzvNyveKxM9PaXMxpejUCu1CM)

What did I learn?
I learned more about the different utilizations of the append function. I learned about strings. I learned how to use Github Markdown Images, which I will be using in my journal entries from now on. I learned the a majority of infections die out after making contact with just a single, or maybe a few patients. 

What questions do I have?
Will the Information Science class be continuing into May? Will we be continuing work on the infection simulation? If we start a new simulation, what is it going to be about?
