[//]: # (Image References)

[image]: ./FigurePlot.png "Rewards Plot"

# Continuous Control - Report

### Solution

#### Approach

This is the signle agent approach with a simple DDPG learning algorithm described in Lectures. The training code (adapted from the lectures/Udacity's Deep Reinforcement Learning Github Repository) is contained in `Continuous_Control.ipynb` and the agent and network model in `ddpg_agent.py` and `model.py` accordingly.

#### Neural Network Architecture

##### Actor
The Actor network is a 4-layer fully connected neural network (with ReLu activations for the hidden layers and a Tanh activation for the output layer) with 33 units in the input layer, 128 units in first of the hidden layer, 64 units in second of the hidden layer and 4 units in the output layer. The output of the first hidden layer is batch-normalized for performance and stability improvement.

##### Critic
The Critic network is a 4-layer fully connected neural network (with ReLu activations) with 33 units in the input layer, 256 units in first of the hidden layer, 128 units in second of the hidden layer and 1 unit in the output layer. The output of the first hidden layer is batch-normalized for performance and stability improvement.

#### Hyperparameters
The initial approach used the following hyperparameters:

DDPG:
- n_episodes (int): maximum number of training episodes: *1000*
- max_t (int): maximum number of timesteps per episode: *3000*

Agent:
- BUFFER_SIZE = *int(1e5)*  # replay buffer size
- BATCH_SIZE minibatch size: *128*
- GAMMA: discount factor: *0.99*
- TAU: for soft update of target parameters: *1e-3*
- LR_ACTOR: learning rate of the actor: *2e-4*
- LR_CRITIC: learning rate of the critic: *2e-4*
- WEIGHT_DECAY: L2 weight decay: *0*

#### Results

After some experiments with the structure of actor and critic networks and learning rates, the basic DDPG with parameters described above performed adequately and trained the agent to solve the environment with average score of +30 in 222 episodes.

See the rewards plot below:

![Rewards Plot][image]

### Future work
As mentioned before, it seems that even a standard DDPG performs adequately. However, we should evaluate the model on the second version of this project, when we have to control 20 identical agents, each with its own copy of the environment.

After it, a further idea would be to compare solutions of different algorithms like PPO, AC3 or D4PG.

We can also try to transfer the algorithm to other problems like the Crawler and see how it will perform there.