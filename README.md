**Building a SARSA Agent**

It involves developing a SARSA (State-Action-Reward-State-Action) agent for the Frozen Lake environment in OpenAI Gym. 

**Action Plan:**

**Setup Environment:**
- Instantiate the Frozen Lake environment using gym.make("FrozenLake-v1", desc=desc).unwrapped.
- Seed the random number generators for both Gym and Numpy with the provided seed.
**Initialize Parameters:**
- Initialize the Q-table to zeros with dimensions matching the state and action space of the environment.
- Set the parameters: gamma (discount rate), alpha (learning rate), epsilon (epsilon for epsilon-greedy policy), number of episodes, and the frozen lake map (amap).
**Implement Epsilon-Greedy Policy:**
- Define the epsilon-greedy policy for action selection. If a random number between 0 and 1 is less than epsilon, select an action uniformly at random; otherwise, select the action with the highest Q-value for the current state.
**SARSA Training Loop:**
- For each episode:
  - Initialize the state.
  - Select an action using the epsilon-greedy policy.
  - Loop until the episode ends:
  - Take the selected action, observe the reward and next state.
  - Select the next action using the epsilon-greedy policy.
  - Update the state and action to the next state and action.
