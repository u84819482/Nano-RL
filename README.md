Minimal implemention of tabular TD control using Q-Learning, SARSA, and Expected SARSA in a MAZE environment. 

The TD control algorithms are based on Bellman equations. SARSA and Expected SARSA use a sample-based version of the Bellman equation and learn q_pi. Q-Learning uses the Bellman optimality equation and it learns q*. The three learning algorithms are shown below, by highlighting their targets.

<img src="https://github.com/user-attachments/assets/77eb6b3b-21d9-46f8-aaf0-960e7a0982c2" alt="TD_control_algorithms" width="500"/>

MAZE dimensions can be varied, as well as its cell content: standard 'Blocks' in black, 'Holes' in red with nominally high penalty, and 'Food' in green with nominally high reward). As an example, a 10x15 MAZE with B/H/F fractions of (0.3, 0.1, 0.1) looks like this:  
<img src="https://github.com/user-attachments/assets/9d87a18a-2e9a-4e4e-a3de-cf368c643f46" alt="Maze" width="500"/>


This environment offers an opportunity to compare the three TD methods across a vast design space as a function of reward assignments,   

![Expected SARSA_last_exp_episode_1](https://github.com/user-attachments/assets/fe5c4af1-22a0-4401-b93c-9d433c33f279)            ![Expected SARSA_last_exp_episode_30](https://github.com/user-attachments/assets/27cd18fa-23d8-420e-a39f-62889091f29c)


