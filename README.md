# 🏎️ Car Racing RL Agent - AI and Machine Learning Exam Project

This repository showcases the development of a **reinforcement learning (RL) agent** designed to solve the **Gymnasium ‘CarRacing-v2’** environment. It was developed as part of the **AI and Machine Learning** course exam at **La Sapienza University**. The project serves as a hands-on exercise to explore **Q-learning** and **Deep Q-Networks (DQN)**, applying these techniques to solve the challenging task of navigating a car racing track.

## 🎯 Project Objective

The objective of this project was to train an agent capable of solving the **CarRacing-v2** task using **reinforcement learning (RL)**. The specific goals was to implement both **Q-learning** and **Deep Q-Networks (DQN)** to train the agent.

## 🔑 Key Features

### 1. **Environment and State Representation**
The **CarRacing-v2** environment is highly complex, requiring effective state representation techniques:
- **Computer Vision**: Utilized to simplify image-based state representations. 
  - **Edge Detection** to highlight important features of the track.
  - **Track Direction Computation** to help the agent understand the track layout and steer accordingly.

### 2. **Reinforcement Learning Algorithms**
- **Q-learning** was implemented as the baseline approach for discrete action spaces. [Q-learning](ML_QTable_car.ipynb)
- **Deep Q-Networks (DQN)** were introduced for more complex state spaces, where a neural network approximates Q-values. [Q-learning](ML_DQN_car.ipynb)
  - **Policy Network vs. Target Network**: A dual-network structure to stabilize training by periodically updating the target network.
  - **Replay Buffer**: Stored previous experiences to improve training efficiency through batch updates.

## 🔧 Technical Approach

- **Q-learning**: Used for simpler, discrete action spaces where the Q-values were stored in a table and updated iteratively.
- **DQN**: A neural network model was used to approximate the Q-values for more complex, continuous state spaces.
- **State Simplification**: Preprocessing steps like **edge detection** and **track direction computation** helped reduce the image complexity and made the learning process more efficient.
- **Policy and Target Networks**: To ensure stable learning, a policy network (for action selection) was paired with a target network (for stable Q-value updates).
- **Replay Buffer**: Allowed for batch updates and improved learning efficiency by sampling from past experiences.
- **Early Stopping**: Terminated episodes if the agent strayed too far from the track, enhancing training efficiency.

## 📈 Results
[report](report.pdf)
In summary, DQN proved more effective than Q-learning for the CarRacing-v2 environment, thanks to its ability to process complex state representations with CNNs. While Q-learning was feasible, it required more effort and delivered less robust results, highlighting DQN's advantages in high-dimensional environments.


