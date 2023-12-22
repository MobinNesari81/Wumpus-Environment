# Wumpus World Environment Documentation

## Introduction
Welcome to the Wumpus World Environment! This environment is designed to simulate a simple yet challenging grid-based game, where an agent navigates through a world containing dangers such as a Wumpus and pits while trying to find gold.

## Environment Overview
The Wumpus World is a grid-based environment with the following key components:

- **Agent**: Represented by an icon, the agent explores the grid and makes decisions to avoid dangers and reach the gold.
  
- **Wumpus**: A dangerous creature that emits a stench. The agent must avoid encountering the Wumpus.

- **Gold**: The ultimate goal for the agent is to find and grab the gold.

- **Pits**: Perilous locations that emit breezes. Falling into a pit results in a penalty for the agent.

- **Arrows**: The agent has a limited number of arrows that can be used to shoot the Wumpus in a specific direction.

## Actions
The agent can take the following actions:

- Move Up
- Move Down
- Move Right
- Move Left
- Shoot Up
- Shoot Down
- Shoot Right
- Shoot Left

The shooting actions consume arrows and eliminate the Wumpus if it is in the targeted direction.

## State Representation
The state is represented as a tuple containing the following information:

- Agent's x-position
- Agent's y-position
- Breeze indicator (boolean)
- Stench indicator (boolean)
- Remaining arrows

## Rewards
The agent receives rewards and penalties based on its actions and interactions with the environment:

- **-10**: Penalty for falling into a pit or encountering the Wumpus.
- **+10**: Reward for grabbing the gold.
- **-1**: Small penalty for each step taken.

## Usage Instructions for Students
1. **Environment Creation:**
   ```python
   env = WumpusWorldEnv(size=4, number_of_pits=3)
   ```
2. **State Representation:**
    - The state is a tuple containing the agent's position, breeze and stench indicators, and remaining arrows.

3. **Actions:**

    - The agent can take actions using integers from 0 to 7, each corresponding to a specific move or shooting direction.
4. **Resetting the Environment:**

    - Call env.reset() to start a new episode. This resets the agent's position, remaining arrows, and other parameters.
5. **Taking Actions:**

    - Use env.step(action) to perform an action in the environment. It returns the next state, reward, episode completion status, and additional information.
6. **Rendering:**

    - The environment supports rendering using Pygame. Call env.render() to visualize the current state of the grid.
7. **Creating an Agent:**

    - Students should implement an intelligent agent that decides the next action based on the current state.
8. **Exploration and Decision Making:**

    - The agent needs to explore the environment, consider the breeze and stench indicators, and decide on the best actions to avoid dangers and reach the gold.
9. **Implement Intelligence Approach:**

    - Implement an algorithm or strategy for the agent to make decisions. Consider using techniques like Q-learning, reinforcement learning, or other intelligent approaches.

10. **Iterative Improvement:**

    - Experiment with different intelligent approaches, tune parameters, and iterate to improve the agent's performance in the Wumpus World.