## Learning Algorithm

As a base i have used Deep Deterministic Policy Gradient (DDPG) from the course: https://github.com/udacity/deep-reinforcement-learning/tree/master/ddpg-pendulum  

Then i have implemented some changes to achieve solution and speed up training (some ideas were thanks to student hub / knowledge base on Udacity): 

1. I have added epsilon parameter to reduce noise by some multipler (0.997) each episode.  I have also reduced initial sigma to sigma=0.18 
2. Instead of training every episode i have parametrized how often and how many times training happen. 
3. Following ideas from other participants i have reduced number of units for both actor and critic to fcs1_units=350, fc2_units=280  to avoid overfitting   
4.  I have tuned hyperaparemeters, most significant changes are increase on batch size and reducing gamma 

Final parameters, along with other hyperparameters:  

BUFFER_SIZE = int(1e6)  # replay buffer size  
BATCH_SIZE = 500        # minibatch size  
GAMMA = 0.90           # discount factor  
TAU = 1e-3              # for soft update of target parameters  
LR_ACTOR = 1e-4         # learning rate of the actor   
LR_CRITIC = 1e-4        # learning rate of the critic  
WEIGHT_DECAY = 0        # L2 weight decay  
EPSILON_DEC =0.997   #noise reduction  
TRAIN_FREQ=10     #how often train agent  
TRAIN_N=5      #how many times train agent  



## Plot of Rewards
![Plot](https://raw.githubusercontent.com/gkowalik/ContinousControl/master/plot.png "Plot")

Environment was solved over 203-303 episodes (having average from 203-303 episode above required 30.00)

More details and results per episode are avaliable in [Main project file](https://github.com/gkowalik/ContinousControl/blob/master/Continuous_Control.ipynb)


## Ideas for future work
