#Connect3 Q-Learning Agent#

This repository contains the code for a Connect3 game playing agent, developed using the Q-Learning reinforcement learning algorithm. The purpose of this software is to train an intelligent agent that can play Connect3 competently.

#Project Structure#

src/ : Contains the source code for the game logic and the Q-Learning agent.
models/ : Contains the saved Q-Table models from previous training runs.
tests/ : Contains unit tests for the game logic and the learning agent.
utils/ : Contains utility functions used throughout the project.

How it Works
This software uses the Q-Learning algorithm for reinforcement learning to create a game playing agent. The process loop forever following these steps:

Select a state, S ∈ S, and an action, A ∈ A(S), at random.
Send state S and action A to a sample model, and obtain a sample next reward, R, and a sample next state, S'.
Apply one-step tabular Q-learning to state S, action A, reward R, and the next state S':
Q(S, A) ← Q(S, A) + α * [R + γ * maxa Q(S', a) − Q(S, A)]

where:

Q(S,A) represents the Q-value of the current state-action pair.
α is the learning rate.
γ is the discount factor.
maxa Q(S', a) represents the maximum Q-value for the next state across all possible actions.
R represents the immediate reward received after performing the action A.


#Dependencies#

The project has been implemented in Python and has the following dependencies:

Python 3.8+
numpy
pandas

#Installation & Setup#

Clone the repository to your local machine.
bash

git clone https://github.com/yourusername/connect3-qlearning.git
Navigate to the project directory.
bash

cd connect3-qlearning
Install the necessary dependencies.

pip install -r requirements.txt
Running the Code
You can run the main script in the project root directory:

python main.py
Testing

To run the tests, you can use the following command:


python -m unittest discover tests

Contributing
If you find any bugs or issues, feel free to create an issue or open a pull request.

License
