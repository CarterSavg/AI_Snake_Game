Snake AI README \
Author: Carter Savage

# Snake Game
This program is broken into two files. One is the deep q-learning model and the other is the double deep q-learning model named respectfully. These programs use pygame to visualize the game and pytorch for the NN models. 
The NN models are used to simulate a quality table as the program uses reinforcement learning to learn how to play snake. It then graphs the output to compare the learning speed and efficiency of deep-q learning vs double deep-q learning.

## Setup
In order to run these programs you must have Pytorch as well as Pygame installed

In the anaconda prompt simply type
```
conda install pytorch
```
```
conda install pygame
```

## Description
The code can be broken down into three main components the Agent, the Game, and the Model. Each component is a class in the program.

### Agent
The agent receives an input array of 11 boolean values. 
* The first three values indicate if there is a wall ahead, right and, left of the, 
* The next 4 indicate the current direction the snake is moving (Left, Right, Up, Down)
* The last 4 are where the food is relative to the head of the snake(Left, Right, Up, Down)

### The Game
The game contains a function called play_step. When this function is called it iterates one stage of the game. This means it will move the snake one block, check if the game is over, increase the snake's length if it ate food, and update the display. The snake itself is 
in a child class of Game which contains all of the data for the snake including its position. The game also has a variable named game_step. This variable tracks the number of iterations since the last time the snake has eaten food. If the snake moves a hundred times its length without eating food the game ends. This is to prevent the snake from moving in a circle endlessly. 
#### Rewards & Punishments
When the snake eats food it receives a reward of 15 and when the snake dies it receives a negative reward of 10. If neither of these things happens a reward of 0 is returned.
### The Model
The model is a neural network with one layer for deep learning and two layers for double deep learning. The number of hidden nodes is 256. The model receives the data from the agent before inputting it into the NN and outputting the direction that the snake should turn. (Left, Right, Straight) The model is then trained for each step with the reward it received for its action.
<br/><br/>
Enjoy having an AI play snake for you!
