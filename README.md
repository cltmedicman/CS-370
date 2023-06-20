# README

## Project Description

This project involves the development of an artificial intelligence (AI) for a treasure hunt game. In the game, the player must find a treasure before a pirate does. While the entire game isn't developed within this project, the intelligent agent, represented by the pirate, is brought to life. This agent aims to find the optimal path to the treasure by using a deep Q-learning model. The agent's learning is driven by "exploration," learning from various states that exist between the initial and terminal state.

## Code Given

I was provided with starter code that includes two Python classes (`TreasureMaze.py` and `GameExperience.py`) and a Jupyter Notebook that serves as a guide to playing the game. `TreasureMaze.py` represents the game environment as a matrix, and `GameExperience.py` is responsible for storing the agent's experiences. The starter code also includes parts of the implementation of a deep Q-learning algorithm, marked with `#TODO` headers, where I was expected to fill in the gaps.

Additionally, helper functions were provided to visualize the maze, define the agent's actions (i.e., moving left, right, up, and down), and simulate a full game. Another provided function, `completion_check(model, qmaze)`, ensures that the maze is well-designed, and the pirate can win some games, making training viable. 

The starter code also built the foundation of the neural network model used for training, including the number of layers, the activation, optimizer, and loss functions.

## Code Created

I completed the implementation of the deep Q-learning model, based on the framework provided. I worked on the `qtrain` function, which defines the number of epochs, maximum memory to store episodes, maximum data size for training, and initializes the TreasureMaze and GameExperience objects.

For each epoch, I set the agent's location to a randomly selected free cell and reset the maze. While the game isn't over, the agent chooses an action (left, right, up, or down) either by exploration or by exploitation. Then, the agent performs the action, and the resulting new state, reward, and game status are observed. The episode, including previous state, action, reward, new state, and game status, is stored in the GameExperience object.

I trained the neural network model with the data retrieved from the GameExperience object and evaluated the loss. If the win rate is above a certain threshold, and the model passes the completion check, that is the epoch used.

## Connection to Computer Science

Computer scientists, like what was done in this project, often build and develop systems or models to solve complex problems. They utilize a variety of tools and methodologies to accomplish these tasks, such as machine learning and deep Q-learning algorithms, which were used in this project.

As a computer scientist, I approach a problem by first understanding the problem's domain. I then develop a plan or model to address the problem, implement the plan, and test and refine it to ensure that it effectively solves the problem. This approach was followed in this project.

From an ethical standpoint, as a computer scientist, I have a responsibility to ensure that the end user's data is protected, that the system does not unfairly disadvantage any users, and that the system behaves as intended without causing harm. For organizations, I am responsible for creating efficient, effective solutions that meet the organization's needs without unnecessary complexity or cost.

## Code

You can find the completed code for this project in the Jupyter Notebook file, `Treasure Hunt Game Notebook`.

## Running the Project

Ensure you have a Python environment with necessary libraries (such as Keras, Numpy, and Matplotlib) installed. Open the provided Jupyter Notebook and run the program
