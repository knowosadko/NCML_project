# Reinforcement Learning in Atari Games: DQN, DDQN and AAC
## Description
In this project we created our own implementation of Deep Q-Networks, Double Deep Q-Network and Advantage Actor Critic using pytorch. We managed to train our algorithms in two enviroments in CartPole and in Pacman. However, Our implementation of AAC was not working on the Pacman problem probably due to stability issues during training. DQN and DDQN was trained on just 10 milion steps and produced promising results, as agent was behaving in an inteligent way. 
## Methods
We tried three method DQN, DDQN and AAC. DDQN differs from DQN by one small modifications in loss funtion calculation. AAC is different algorithm that is not value optimization algorithm like DQN but rather policy optimization algorithm. MethodsListed methodsbelow with short descriptions
## Game
#### Pacman
Enviroment provided by Open AI Gymnasium [link](https://gymnasium.farama.org/environments/atari/pacman/#pacman).
**Bug** with **Namespace not found** can be solved with ```pip install "gymnasium[atari, accept-rom-license]"```.
## Resources
Report: [here](https://www.overleaf.com/9679698641rbttmysfpqqc)
Google drive: [here](https://drive.google.com/drive/folders/1PvpYXdNtiZo-MlEE25LgSPYPdH4xnQT5?usp=sharing)

