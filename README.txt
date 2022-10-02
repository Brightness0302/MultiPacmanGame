Rules of Capture the Flag:

Layout: 
The Pacman map is divided into two halves: blue (right) and red (left). 
Red agents (which all have even indices, e.g., gameState.getAgentState(index)) must defend the red food while trying to eat the blue food. 
When on the red side, a red agent is a ghost. When crossing into enemy territory, the agent becomes a Pacman.

Scoring: 
When a Pacman eats a food dot, the food is stored in the Pacman. 
When the Pacman returns to home territory, one point is scored for each food item in the Pacman. 
Red team scores are positive, while Blue team scores are negative.

Eating Pacman: 
When a Pacman is eaten by an opposing ghost, the Pacman returns to its starting position (as a ghost). 
No points are awarded for eating an opponent. Ghosts can only be eaten if they are scared (agent.scaredTimer > 0).
Ghosts are 'scared' for 40 seconds when the opposing team has eaten a power capsule.

Winning: 
A game ends when either one team eats all but two of the opponents' dots. 
Games are also limited to 1200 agent moves. If this move limit is reached, whichever team has eaten the most food wins.

Computation Time: 
In online play, each agent will have only 1 second to choose an action. 
If an action is not returned in this amount of time, the server will move the agent randomly.

Observations: 
Agents can only observe an opponent's configuration (position and direction) if they or their teammate is within 5 squares (Manhattan distance). 
In addition, an agent always gets a noisy distance reading for each agent on the board, which can be used to approximately locate unobserved opponents.

For a demo of how the game works, you can try run the baseline agent on both teams using:
py capture.py -r baselineTeam -b baselineTeam

*************************************************
Your goal in this project is to apply VALUE ITERATION as well as ONE or more of the following techniques to the problem:
1. Classical Planning (PDDL and calling a classical planner)
2. Monte Carlo Search Tree or UCT (Model-Free MDP)
3. Reinforcement Learning - classical, approximate or deep Q-learning (Modle-Free MDP)
4. Goal Recognition Techniques (to infer intentions of opponents)
5. Game Theoretic Methods
6. Bayesian Interface
****************************************************
