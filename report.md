[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/863984/83252793-c9774700-a1a3-11ea-8363-99022a9aece0.png "Plot of rewards"


# Learning Algorithm
The learnig algo is a Deep Q Learning. The params are in the `model.py` file:
 - BUFFER_SIZE = int(1e5)  # replay buffer size
 - BATCH_SIZE = 64         # minibatch size
 - GAMMA = 0.99            # discount factor
 - TAU = 1e-3              # for soft update of target parameters
 - LR = 5e-4               # learning rate 
 - UPDATE_EVERY = 4        # how often to update the network

While training the DQN, the following values has been used:
 - eps_start=1.0
 - eps_end=0.01 
 - eps_decay=0.99

The deep net used to estimate the Q table has 2 hidden layers, fully connected with Relu activation. No regularization was needed. The input layer has 37 units (as the state dimenionality); while the output has 4 (as the possible actions). The hidden layers have both 64 units.


# Plot of Rewards

Here's the plot of rewards.
More specifically, it reaches an average of reward of:

 - +13 in 412 episodes
 - +14 in 457 episodes

![Plot of rewards Agent][image1]



# Ideas for Future Work

Possible improvements:
 - dauble DQN
 - prioritized experience replay
 - dueling DQN