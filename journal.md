# This is my journal

   What are some ways in which Computer Science can help the fight against Covid-19?

   There are many ways in which Computer Science can help the fight against Covid-19. The most obvious benefit I can think of is creating digital models to simulate the progression of the virus, however there are also other possibilities. Ideas of note include games to teach children about social distancing, an app that senses other phones and can tell you if you're closer than 6 feet to someone holding a digital device, and moving struggling buisnesses from brick-and-mortar stores online. There are, of course, an almost infinete set of possibilities, however, these are the first ones that came to mind.

   In your opinion, should people enable access to the resources of their personal computers as tools for research? Are there any risks?

   I don't believe that people either should or shouldn't enable access to the resources of their personal computers as tools for research, however I believe that there should be an option avaliable for people to volunteer their services if they would like too. The risks involve people having their information stolen, or corrupting the data, or a bunch of other issues that essentially boil down to people attempting to undermine other people. 
   
   What should be some behaviours (at least 3) that we will need to include in our simulation to be a realistic approximation of the current situation in the world? Explain.
   
   1. People quarantining themselves. As the virus spreads, people will be isolating themselves in the hope of preventing themselves from catching the virus. 
   2. People going to gatherings. The virus's reach increases exponentially when large social gathering's take place.
   3. Remenants. People also leave the virus on the items they touch. Since this is the case, the virus should be left behind in the area's the simulated people have just been.
   
   What did we do?
   
First, we read an article on how Computer Science can help fight Coronavirus. Then we answered 2 questions adressing our thoughts on the role of computer science in fighting Coronavirus. We were then shown the lessons plan for the next few weeks. We were then given a tutorial on how to begin a simulation of the epidemiological affects of the Coronavirus, along with two challanges and another question about our thoughts on the simulation. The code and the completed challange code can be seen below.
```py
# definition of variables
x = [100,150,200,250,240,260,300,350,400,450]
y= [100,150,200,250,240,260,300,350,400,450]
    

def setup():
    size(500,500)
    for x in range (10):
        x = random (500, 500)

        y = random (500,500)
    
def draw():
    global x, y
    background(255)
    strokeWeight(2)
    
    #create 1st individual
    for i in range(10):
        circle(x[i], y[i], 40)
        x[i] = x[i] + random(-10, 10)
        y[i] = y[i] + random(-10, 10)
        
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
    delay(100)
```

  Q2. What did I learn?
    
  I learned that brackets are used to create lists. I learned how to make a forward loop. I learned what the lesson plan for the next few weeks is. I gained a better understanding of the global command. I learned how to set boundaries.
    
  Q3. What questions do I have?
  
  What is the final product going to look like? Are we going to be building off the same code for the next few weeks? What are epidemiologists doing to simulate the potential path of the Coronavirus?
