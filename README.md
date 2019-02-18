# CxSy-Challenge-Ona-Pena

### Background of the study

For the modified CxSy challenge, the team decided to implement three (3) agent strategies that modeled real life decision making behaviors. Among the total number of agents present in the simulation, a maximum of 33% of these agents can be chosen to model one (1) of the three available strategies while the remaining agents behave randomly. This study aims to evaluate the effectivity of these strategies in terms of how much the agents earn and how these agents decide which pool to move to.

The first available strategy is a modified greedy strategy wherein an agent moves to the pool with the highest average payoff from the last N timesteps where N is a value chosen by the user that is >= 1 and <= 10. This strategy aims to model a type of behavior wherein individuals look at the financial history of a certain pool and evaluate its capacity to generate income based on said history. 
The second available strategy is a trend-following strategy wherein an agent moves to the pool with the highest number of new agents from the previous time step. This strategy models a bandwagon type of behavior where the agent follows the most ‘popular’ choice regardless of its potential payoff.

The last strategy is a semi-random strategy wherein an agent decides randomly but always returns to stable every N timesteps, wherein N is >= 1 and N <= 100. This option aims to model a behavior wherein an agent erratically makes investment decisions but always returns to the stable pool for the purpose of compensating for any losses.

### Methodology

For the modified greedy strategy, a slider for memory indicates the number of previous timesteps an agent will consider when calculating average payoff. Payoffs per timestep are then stored in a list that is accessed by the agent when it is time to switch pools. The agent looks at the last N (memory) entries in the array and calculates the average to choose which pool to move to.

For the trendy strategy, the most popular pool choice is updated at every timestep once all agents have made a move. This becomes the reference for whenever this type of agent has to switch pools. Lastly, for the semi-random strategy, a slider indicates the interval for when the agent returns to stable. At every other turn outside that interval, the agent will behave randomly.

### Limitations

The study is limited to only evaluating the 3 aforementioned strategies with a certain percentage of agents modeling a particular behavior. The remaining agents model a random behavior that can otherwise affect the overall results depending on the number of these random agents. The study is also limited to the capacities of NetLogo with some implementations not utilizing the appropriate data structure due to its absence within the program. The study also does not employ any predictive algorithm that considers possible future payoffs and only considers past payoffs and past behavior when making decisions. 

### Results & Analysis
![assumptions](https://user-images.githubusercontent.com/25882838/52959244-b2f31500-33d0-11e9-9dba-1d34a995bc35.PNG)
The first configuration tested was seeing how much the semi-random agents affected the simulations. This was done by changing the value of the random value of the Semi-random agents. By changing this, we change when they go back to the stable pool. So in this first configuration, we tested if the value of the random-variable would affect the outcome if the value was less than 50 time steps. 
![config1](https://user-images.githubusercontent.com/25882838/52959270-c69e7b80-33d0-11e9-9e85-f2d882f11372.PNG)
Figure 2. Testing the for values less 50 for *random-variable*

The figures above all show the time table of the simulation and how many agents were left at each pool during the course of the simulations. The times that the value of the random-variable was closer to 1, just like the top left simulation of Figure 1, the more consistent the agents were in staying at the random pool. When the random-variable would approach 50, the results of the simulation would start to vary and become more erratic. This just means that there is less time for that semi-random agent to go back to the stable pool This means having a value of 100 in the random-variable would basically make the agent act like the default agent of random behavior all throughout the simulation. It was worthy to note that this behavior was seen regardless if the tau was any value between 0 and 1.

In the next configuration, we tested how much the greedy-modified agents would affect the simulations. 
![config2](https://user-images.githubusercontent.com/25882838/52959422-19783300-33d1-11e9-89da-6f904cd19dfa.PNG)
Figure 2. Behavior of the Greedy-Modified Agents

We noticed a behavior with the agents with the modified-greedy strategy. It seems that the more there were agents that had this behavior, the more times agents would hop from one pool to another every 10 time steps since the switch interval is 10. This would cause very erratic results of agents jumping from pool to pool all the time. The less these agents existed, the agents would stay at more stable pools. This behavior was noticeable as well regardless of tau cost. 

In the next configuration, we play around with the trendy strategy agents. 
![config3](https://user-images.githubusercontent.com/25882838/52959532-5cd2a180-33d1-11e9-84a1-29de1d20935d.PNG)
Figure 3. Testing Trendy Agents Alongside Other Agents

One noticeable behavior these trendy following agents do is enhance the effect of a certain strategy. If there are trendy strategy agents alongside modified-greedy agents, the would seem to follow these agents jumping from pool to pool every 10 ticks. In the case of semi-random, a higher random variable would result in a high amount of agents staying at a certain pool at the end of the simulation while a lower random variable would follow the first configuration where everyone stayed at the stable pool. This behavior was noticeable as well regardless of tau cost. 

### Conclusion & Recommendations

In conclusion, the simulations are not as realistic due to its predictability. Nothing that would spark interesting detail would arise with these behaviors. The behaviors implemented on the agents may have had rigid rules to the point they dictated the simulations. We would recommend maybe adding more agents that did simple behaviors and strategies. Similar to the ants model, the only thing the ants agents did was smell for a scent unlike ours where the agents had a set of rigid rules. So adding more simple agents could result in interesting results for the complex system as a whole. 
