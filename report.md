[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/863984/83252793-c9774700-a1a3-11ea-8363-99022a9aece0.png "Plot of rewards"

# REPORT

This file contains a report of the project, and includes the design choices of the algorithm. 

## Learning Algorithm

The learning algorithm is a Deep Q Learning (DQN). 
The environment is reset and re-initialised after each episode. 
Then, each episode's states, actions and rewards are stored into a episode buffer of size 10K (`BUFFER_SIZE`). 
Every 4 steps (`UPDATE_EVERY` param) the deep network is updated, using 64 (`BATCH_SIZE`) random samples from the buffer.  
The deep net learns what's the expected reward, given a state and an action, approximing at every iteration the local Q table. 
The learning is performed with a discount factor of 0.99 (`GAMMA`), and the target table is "smootly" updated with a factor of 0.001 (`TAU`). This is done to avoid instability.
The learning rate (`RL` or `ALPHA` in the code) has been set to 0.0005.

These are the constant values used in the equation of the weights updates. While training the DQN, the following values has been used:
 - epsilon_start=1.0
 - epsilon_end=0.01 
 - epsilon_decay=0.99

The deep net used to estimate the Q table has 2 hidden layers, fully connected with Relu activation. No regularization was needed. The input layer has 37 units (as the state dimenionality); while the output has 4 (as the possible actions). The hidden layers have both 64 units. The loss to be minimized at every is the MSE.


## Plot of Rewards

Here's the plot of rewards.
More specifically, it reaches an average of reward of:

 - +13 in 412 episodes
 - +14 in 457 episodes

![Plot of rewards Agent][image1]



## Ideas for Future Work

Possible improvements:
 - double DQN
 - prioritized experience replay
 - dueling DQN