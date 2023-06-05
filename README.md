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

#### Results
Belwo we present results of our trainings, first for CartPole then for Pacman.
#### CartPole
![losses_dqn_ddqn](https://github.com/knowosadko/NCML_project/assets/40035342/12bb127c-450f-47d9-8955-a106f23b7505)
![dqn_ddqn_after](https://github.com/knowosadko/NCML_project/assets/40035342/29a7f591-6b47-4fb0-a33d-7333f048d5e4)
![aac_cartpole](https://github.com/knowosadko/NCML_project/assets/40035342/85b81caa-6da6-494f-bc80-b2bb9d2a2838)
Above plots show loss and reward for each of the algorithm trained on CartPole problem.
Moreover we have videos with performance of each algorithm.
DQN                        |          DDQN              |   AAC
:-------------------------:|:-------------------------: | :-------------------------:              
![rl-video-episode-399](https://github.com/knowosadko/NCML_project/assets/40035342/7f3094ae-dbb1-481e-89a1-ea1d0f57d154) |                 ![rl-video-episode-399 (1)](https://github.com/knowosadko/NCML_project/assets/40035342/567c192c-111d-4ff2-8d70-b1830b57c8db) | ![rl-video-episode-499](https://github.com/knowosadko/NCML_project/assets/40035342/eb77b6cc-a0f5-4105-8ec9-3d4030ffd734)

#### Pacman
Belwo we present training results on the Pacman problem.


![dqn_reward](https://github.com/knowosadko/NCML_project/assets/40035342/dbf96366-c2be-41a4-b90e-7b36f115e746)

![dqn_ddqn_output](https://github.com/knowosadko/NCML_project/assets/40035342/98a165c6-0835-4fa7-92e0-09854b17fe8a)


DQN                        |          DDQN              
:-------------------------:|:-------------------------: 
![dqn](https://github.com/knowosadko/NCML_project/assets/40035342/edaf14a2-169d-4434-96c9-0a6466aade03) | ![rl-video-episode-1299](https://github.com/knowosadko/NCML_project/assets/40035342/dc1da948-6452-4411-a5a1-76e92a0423e4)
                   

