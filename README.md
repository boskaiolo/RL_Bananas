[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/42135619-d90f2f28-7d12-11e8-8823-82b970a54d7e.gif "Trained Agent"


# RL_Bananas

## Introduction

For this project, you will train an agent to navigate (and collect bananas!) in a large, square world.

![Trained Agent][image1]


A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana.  Thus, the goal of your agent is to collect as many yellow bananas as possible while avoiding blue bananas.  

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around agent's forward direction.  Given this information, the agent has to learn how to best select actions.  Four discrete actions are available, corresponding to:
- **`0`** - move forward.
- **`1`** - move backward.
- **`2`** - turn left.
- **`3`** - turn right.

The task is episodic, and in order to solve the environment, your agent must get an average score of +13 over 100 consecutive episodes. In the notebook, the pre-trained weights has been set when the train reaches +14, so there's more chance that in a test run, it will reach at least +13.

## Getting Started

1. Download the environment from one of the links below.  You need only select the environment that matches your operating system:
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)
    
    (_For Windows users_) Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

    (_For AWS_) If you'd like to train the agent on AWS (and have not [enabled a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md)), then please use [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux_NoVis.zip) to obtain the environment.

2. Place the file in this GitHub repository, in your HOME folder, and unzip (or decompress) the file. Then, change the path in the `Navigation.ipynb`b file, in order to point it to the correct file.

 - *In the `Navigation` notebook avilable in this repo, we'll use the AWS Headless version. Feel free to change it!*

## Instructions

1. Be sure you're running a Python 3.6+ jupyter notebook
2. Install the following libraries (see next point if you have problems with the environment):

 - gym
 - torch (better if you're using CUDA/GPU)
 - numpy
 - matplotlib
 - unityagents

3. Follow the instructions in `Navigation.ipynb` to get started with training your own agent. The last cell uses a pretrained set of weights; hopefully, you'll get a score of at least +13!

## Python dependencies (Conda env)

To set up your python environment to run the code in this repository, follow the instructions below.

1. Create (and activate) a new environment with Python 3.6.

	- __Linux__ or __Mac__: 
	```bash
	conda create --name rl_torch_36 python=3.6
	source activate rl_torch_36
	```
	- __Windows__: 
	```bash
	conda create --name rl_torch_36 python=3.6 
	activate rl_torch_36
	```
	
2. Follow the instructions in [this repository](https://github.com/openai/gym) to perform a minimal install of OpenAI gym.  
	- Next, install the **classic control** environment group by following the instructions [here](https://github.com/openai/gym#classic-control).
	- Then, install the **box2d** environment group by following the instructions [here](https://github.com/openai/gym#box2d).
	
3. Clone the Udacity repository, and navigate to the `python/` folder.  Then, install several dependencies.
```bash
git clone https://github.com/udacity/deep-reinforcement-learning.git
cd deep-reinforcement-learning/python
pip install .
cd ..
```

4. Clone the repository for the exercise
```bash
git clone https://github.com/boskaiolo/RL_Bananas.git
cd RL_Bananas
```

5. Create an [IPython kernel](http://ipython.readthedocs.io/en/stable/install/kernel_install.html) for the `rl_torch_36` environment.  
```bash
python -m ipykernel install --user --name rl_torch_36 --display-name "rl_torch_36"
```

6. Before running code in a notebook, change the kernel to match the `rl_torch_36` environment by using the drop-down `Kernel` menu. 


## Want to learn more on Reinforcement Learning?

Try the Deep Reinforcement Learning Nanodegree program at Udacity!