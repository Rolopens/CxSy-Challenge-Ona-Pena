# CxSy-Challenge-Ona-Pena

### Setup and Assumptions

The complex system was setup using NetLogo. The system contains 50 agents that start at any random pool. The pools are represented by the color of the patches in Netlogo. Pink patches represent the high pool wherein agents in this pool have a 25% chance to earn up to 80$ split among all the agents found in that pool and have 75% chance to earn nothing per round. Blue patches represent the stable pool wherein agents always earn 1$ each per round. Lastly, the green patches represent the low pool wherein agents in this pool have a 50% chance to earn 40$ evenly split among all the agents in that pool and a 50% chance to earn nothing per round. 

### Strategy

The strategy  implemented was a basic strategy of determining whether agents playing aggressive after a certain period of time would yield interesting or noteworthy results such. Aggressive in this context means going for the pool with the highest overall average income of agents. Several factors contribute as to why this strategy was used. Such factors include the idea of waiting to save costs since there is a tau (cost) when transferring pools. The strategy was then further tested by changing when the agents start changing pools. The test consists of allowing agents to join every 10, 20, 30, 40, or 50 rounds. Then, the experiment further tested the strategy by changing the value of tau from values in between 0 to 1 inclusive to see the behavior of the model. Agents with random behavior were also added to the model to see if the agents following the strategy would be affected by these agents acting in a random behavior. 

### Analysis

Upon running the model, there are several things worthy to take note off. Regardless of the number of random agents and switch interval that the model uses, the tau variable plays a major role in determining what pool each agent will be in at the end. One noteworthy behavior that we were able to observe from the agents was that, when the tau was less or equal to 0.5, the agents would most likely end up in either the high or low pools, but, when the tau was above 0.5, the agents would most likely be in the stable pool at the end of simulation. This shows that the agents choose to do the less risky move by in moving into other pools when there is a high tau (cost). When there is a low tau, the agents then go for that chance to get more money by either staying in the high or low pool. 
