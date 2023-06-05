# Reinforcement Learning in Atari Games: DQN, DDQN and AAC
## Description
In this project we created our own implementation of Deep Q-Networks, Double Deep Q-Network and Advantage Actor Critic using pytorch. We managed to train our algorithms in two enviroments in CartPole and in Pacman. However, Our implementation of AAC was not working on the Pacman problem probably due to stability issues during training. DQN and DDQN was trained on just 10 milion steps and produced promising results, as agent was behaving in an inteligent way. 
## Methods
We tried three method DQN, DDQN and AAC. DDQN differs from DQN by one small modifications in loss funtion calculation. AAC is different algorithm that is not value optimization algorithm like DQN but rather policy optimization algorithm. Implemented methods below with short descriptions:
 - **Advantage actor critic** - two models that share input layers, one model is optimizing value function (critic) the other is optimizing policy (actor).
 - **Deep Q-networks** - Simliar to Q-learning however, have two models one optimizes value function, second model acts as target provider and is updated every C iterations. 
 - **Double Deep Q-networks** - basically DQN however has one modification in loss function that reduces its maximization bias.
## Problems
#### Cartpole
Enviroment provided by Open AI Gymnasium [link](https://gymnasium.farama.org/environments/classic_control/cart_pole/). Clasic control problem with inverted pendulum. Cartpole problem acts as a PoC for our implementations.
#### Pacman
Enviroment provided by Open AI Gymnasium [link](https://gymnasium.farama.org/environments/atari/pacman/#pacman). Classic atari game much more complicated than CartPole. Target problem of our work.
**Bug** with **Namespace not found** can be solved with ```pip install "gymnasium[atari, accept-rom-license]"```.

