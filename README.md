# Deep Q-Learning for Lunar Lander

## Project Overview
This project implements a Deep Q-Learning agent to successfully land a lunar module using the OpenAI Gym environment `LunarLander-v3`. The agent is trained to optimize its landing strategy through reinforcement learning, specifically using the Deep Q-Network (DQN) approach.

## Table of Contents
- [Introduction](#introduction)
- [Environment](#environment)
- [Deep Q-Learning Overview](#deep-q-learning-overview)
- [Project Structure](#project-structure)
- [Requirements](#requirements)
- [How to Run](#how-to-run)
- [Results](#results)
- [Demonstration Video](#demonstration-video)
- [Google Colab Notebook](#google-colab-notebook)
- [Conclusion](#conclusion)

## Introduction
In the Lunar Lander environment, the agent controls a lander that needs to safely touch down on the landing pad. The agent receives rewards based on its performance, such as staying upright, reducing velocity, and avoiding crashes.

## Environment
`LunarLander-v3` is a classic control problem in OpenAI Gym. The state space consists of 8 variables, and the action space includes 4 discrete actions:
1. Do nothing
2. Fire left orientation engine
3. Fire main engine
4. Fire right orientation engine

## Deep Q-Learning Overview
Deep Q-Learning combines Q-Learning, a model-free reinforcement learning algorithm, with deep neural networks to handle large state spaces. In this project:
- A neural network approximates the Q-function, predicting Q-values for each action given a state.
- Two networks are used: the **local Q-network** for selecting actions and the **target Q-network** for stable Q-value updates.
- Experience replay is utilized to break the correlation between consecutive experiences and improve learning stability.

## Project Structure
```
.
├── deep_q_learning_lunar_lander.ipynb   # Google Colab notebook
├── video.mp4                            # Demonstration video
├── README.md                            # Project documentation
└── requirements.txt                     # List of dependencies
```

## Requirements
- Python 3.x
- `torch`
- `numpy`
- `gym`
- `imageio`
- `IPython`

To install the dependencies, use:
```bash
pip install -r requirements.txt
```

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/deep-q-learning-lunar-lander.git
   ```
2. Navigate to the project directory:
   ```bash
   cd deep-q-learning-lunar-lander
   ```
3. Open the Colab notebook (`deep_q_learning_lunar_lander.ipynb`) and run the cells step by step to train the agent and generate the demonstration video.

## Results
The agent is trained over 2000 episodes, with the average score computed over the last 100 episodes. The environment is considered solved when the average score reaches 200. The training progress is dynamically printed in the notebook, showing the episode number and the average score.

## Demonstration Video
Below is a video demonstrating the trained agent's performance in landing the lunar module:
https://github.com/user-attachments/assets/1c474f2b-dac4-46f4-8d85-edf58fb9c2cb

## Google Colab Notebook
The Google Colab notebook containing the full implementation and training process can be found [here](deep_q_learning_lunar_lander.ipynb).

## Conclusion
This project demonstrates the application of Deep Q-Learning in a continuous control environment, providing insights into reinforcement learning techniques and their practical implementation using PyTorch and OpenAI Gym.

Feel free to fork the repository and experiment with different hyperparameters or improvements to the DQN architecture.

