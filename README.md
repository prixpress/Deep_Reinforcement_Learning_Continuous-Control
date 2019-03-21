[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/43851024-320ba930-9aff-11e8-8493-ee547c6af349.gif "Trained Agent"


# Continuous Control

### Project Details
For this project, the target of the agent is to control a single double-jointed arm that follows a goal location (which is a moving target) and keeps its hand within this location. The environment is providing a reward of +0.1. To conclude, the agent should keep its "hand" as long as possible within the target area to maximize the reward.

The state space has **33 dimensions** and corresponds to
* position
* rotation
* velocity
* angular velocities
of the arm.

Given this information, the agent has to learn how to best select actions. Each **continuous action** (consisting of a vector of four entries) corresponds to the torque applicable to two joints. Each entry in the action vector should be a number between -1 and +1.

The task is episodic, and in order to solve the environment, the agent must get an **average score of +30 over 100 consecutive episodes**.

Note: The project environment is similar to, but not identical to the Reacher environment on the [Unity ML-Agents GitHub page](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#reacher).

### Getting Started
The following instructions assume you are running on an Ubuntu 16.04 x64 distribution, with an [Anaconda](https://www.anaconda.com/download/#linux) installation. If you have installed Anaconda, please run following commands in order to execute the **Continuous_Control** notebook:

Note: the python folder within this repository and the link to the pre-build Unity Environment for Linux are copied from the [Udacity DRLND course](https://github.com/udacity/deep-reinforcement-learning)
```bash
$ conda create --name drlnd python=3.6
$ source activate drlnd

$ git clone https://github.com/shelbyi/drlnd.git
$ cd drlnd/python
$ pip install .

$ python -m ipykernel install --user --name drlnd --display-name "drlnd"
```
Next, download the pre-build Unity Environment for your Linux system.
<br>Linux visual: [Click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux.zip)
<br>Linux headless: [Click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux_NoVis.zip)
<br>Place the file in the **p2_continuous-control** folder within the repository and unzip it.

Now, you should be set up to run the notebook on your system.

### Instructions
Before you run the notebook, be sure to change the kernel to **drlnd**. Execute cell after cell to get some information of the environment and to train the agent to keep its "hand" within the target location. At the end, the neural networks of the actor-critic model and the **model weight** are stored to disk under **https://github.com/udacity/deep-reinforcement-learning/tree/master/p2_continuous-control/**.

Start the notebook and execute the cells.
```
$ cd [path to the repo]deep-reinforcement-learning/p2_continuous-control/
$ jupyter-notebook Continuous_Control.ipynb
``` 

Follow the instructions in `Continuous_Control.ipynb` to get started with training your own agent!  
