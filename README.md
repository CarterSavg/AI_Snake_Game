Snake AI README
Author: Carter Savage

# Snake Game
This program is broken into two files. One is the deep q-learning model and the other is the double deep q-learning model named respectfully. These programs use pygame to visualize the game and pytorch for the NN models

## Setup
In order to run these programs you must have Pytorch as well as Pygame installed

In the anaconda prompt simply type
```
conda install pytorch
```
```
conda install pygame
```

### Description
The code can be broken down into three main components the Agent, the Game, and the Model. Each component is a class in the program.

#### Agent
The agent receives an input array of 11 boolean values. 
* The first three values indicate if there is a wall ahead, right and, left of the, 
* The next 4 indicate the current direction the snake is moving (Left, Right, Up, Down)
* The last 4 are where the food is relative to the head of the snake(Left, Right, Up, Down)
#### Agent
The agent receives an input array of 11 boolean values. 
* The first three values indicate if there is a wall ahead, right and, left of the, 
* The next 4 indicate the current direction the snake is moving (Left, Right, Up, Down)
* The last 4 are where the food is relative to the head of the snake(Left, Right, Up, Down)
