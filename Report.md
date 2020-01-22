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

5. I have added workspace "keep alive" solution I have also added  [provided solution](https://github.com/udacity/workspaces-student-support/tree/master/jupyter) to keep workplace active as [suggested in QA](https://knowledge.udacity.com/questions/61260). It requires workspace_utils.py file provided in this repository.

## Plot of Rewards
![Plot](https://raw.githubusercontent.com/gkowalik/ContinousControl/master/plot.png "Plot")

Environment ended on 303 episode, as it was solved over 203-303 episode (having average from 203-303 episode above required 30.00)

More details and results per episode are avaliable in [Main project file](https://github.com/gkowalik/ContinousControl/blob/master/Continuous_Control.ipynb)


## Ideas for future work

I have read that normalization in neural network was common solution to increase training speed so that would be probably my next step. I have also noticed that even small changes in hyperparameters could increase or decrease number of required episodes a lot, so further hyper parameter tunning could improve the results.

Exploring and comparing different methods mentioned in course and papers REINFORCE, TNPG, RWR, REPS, TRPO, CEM, CMA-E could also bring better results, for that solution i did not tried other methods besides DDPG
