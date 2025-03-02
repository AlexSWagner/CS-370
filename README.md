# Pirate Intelligent Agent Project

This repository contains my Jupyter Notebook for the Pirate Intelligent Agent project, completed as part of my class. The project demonstrates how key concepts in reinforcement learning and neural networks can be applied to a real-world problem—teaching a pirate agent to navigate a maze and locate treasure before a human competitor.

## Overview

The core objective of this project was to develop a deep Q-learning system capable of guiding an agent through an 8×8 maze. The project involved designing a custom neural network, implementing an experience replay mechanism, and optimizing the training process through dynamic starting positions and an epsilon-greedy exploration strategy.

## Implementation Details

- **Neural Network Architecture**:  
  The agent’s network consists of:
  - An input layer with 64 nodes (representing the 8×8 maze).
  - Two hidden layers with PReLU activation functions to capture complex patterns.
  - An output layer with four nodes corresponding to possible moves: up, down, left, and right.  
  The network is optimized using the Adam optimizer with a mean squared error (MSE) loss function.

- **Experience Replay**:  
  To ensure stable training and mitigate the risk of overfitting to sequential data, an experience replay buffer was implemented. This mechanism stores up to 8,000 experiences (state, action, reward, next state, and terminal flag) and randomly samples mini-batches during training.

- **Training Optimization**:  
  The training process was refined by:
  - Utilizing dynamic starting positions to expose the agent to varied maze configurations.
  - Implementing an epsilon-greedy strategy that starts with high exploration (ε = 1.0) and gradually reduces to a minimum of 0.1 as the agent’s performance improves.  
  As a result, the agent achieved a 100% win rate after 264 epochs, with a final loss of 0.0045 and an average of 89.4 episodes processed per epoch. The entire training process was completed in roughly 12 minutes.

## Reflection on Project Work

### What Code Was Provided vs. Code I Created

- **Provided Code**:  
  The initial Jupyter Notebook framework included the basic setup for the maze environment and core game mechanics for the pirate agent.

- **My Contributions**:  
  - Developed the deep Q-learning algorithm.
  - Designed and implemented a custom neural network architecture.
  - Created the experience replay system to stabilize training.
  - Optimized the training process by incorporating dynamic starting positions and an adaptive epsilon-greedy exploration strategy.

### What Do Computer Scientists Do and Why Does It Matter?

Computer scientists use both theory and practical methods to solve complex problems that affect our daily lives. Their work drives technological innovation, improves efficiency, and has a wide-ranging impact on society. By developing new algorithms and building smarter systems, they create solutions that help tackle challenges across various industries, making technology more effective and accessible.

### How Do I Approach a Problem as a Computer Scientist?

When I face a problem, I break it down into smaller, manageable parts to understand each component thoroughly. I analyze the underlying principles and design algorithms that address these specific issues. Then, through an iterative process of development, testing, and refinement, I work to build a robust solution. This systematic approach allows me to adapt and improve my methods based on practical feedback and measurable results.

### What Are My Ethical Responsibilities?

I believe that ethical considerations are an important part of computer science. It is important to design algorithms with transparency and fairness, ensuring that all decisions are made clearly and without bias. Protecting user privacy and complying with data protection standards, such as GDPR, is also essential. By keeping these ethical responsibilities at the forefront of my work, I strive to create technology that benefits both the end users and the organizations I work with, while maintaining trust and social responsibility.
