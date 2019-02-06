## Context

The challenge of this project is 

The program was developed with the DDPG algorithm, based on the course code (https://github.com/udacity/deep-reinforcement-learning/tree/master/ddpg-pendulum).
In the project folder is the Unity environment (Tennis.app), the Jupyter file to run and four files with the Actor (Policy) Model, the Critic (Value) Model and the Agent. 
In the model use 2 fully connected hidden layers with ReLu activations for both the actor and the critic with a configuration of 256 nodes in each of them.

Tanh is used in the final layer that maps states to actions. Batch normalization is used for mini batch training. Mirar https://pytorch.org/docs/stable/nn.html#normalization-layers 

## Agent Hyper Parameters

	•	BUFFER_SIZE = int(5e5)  # replay buffer size
	•	BATCH_SIZE = 128        # minibatch size
	•	GAMMA = 0.99            # discount factor
	•	TAU = 5e-3              # for soft update of target parameters
	•	LR_ACTOR = 1e-3         # learning rate of the actor 
	•	LR_CRITIC = 1e-3        # learning rate of the critic
	•	WEIGHT_DECAY = 0        # L2 weight decay
	•	NU_PASS = 10            # number of passes
	•	EPSILON = 1.0           # epsilon for noise process
	•	EPSILON_DECAY = 1e-6    # decay rate for noise process

## Performance and Plot of Rewards

![alt text](https://github.com/rubenbet/continuous_control_p2/blob/master/Results.png)

https://github.com/rubenbet/continuous_control_p2/blob/master/Results.png

The Environment was solved in 1593 episodes.

## Improvements
