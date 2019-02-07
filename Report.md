## Context

The challenge of this project is that the agents must get an average score of +0.5 (over 100 consecutive episodes, after taking the maximum over both agents

The program was developed with the DDPG algorithm, based on the course code (https://github.com/udacity/deep-reinforcement-learning/tree/master/ddpg-pendulum). The starting point was the code developed for the continuous control with the Reacher.app. In the project folder is the Unity environment (Tennis.app). Adapt part of the code to work with two agents, and activate in Jupyter a part for training that performs training in up to 5,000 episodes or when it exceeds 0.5 and generates the Actor (Policy) Model and the Critic (Value) Model for each agent. Then there is a test mode, where the agent loads the training models, achieving an ideal performance. 

Tanh is used in the final layer that maps states to actions. Batch normalization is used for mini batch training. Look https://pytorch.org/docs/stable/nn.html#normalization-layers 

## State and Action Space
The observation space consists of 8 variables corresponding to the position and velocity of the ball and racket. Each agent receives its own, local observation. Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping.

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

![alt text](https://github.com/rubenbet/collab-compet-tennis/blob/master/ResultsCollab.png)

https://github.com/rubenbet/collab-compet-tennis/blob/master/ResultsCollab.png

The Environment was solved in 1593 episodes.

In test mode, loading the trained models, the following results were achieved in two episodes:

Episode 2	Agent1 Score: 2.60	Agent2 Score: 2.60

## Ideas for future

Use different Agent Hyper Parameters. 
 
Try other models such as PPO. 
