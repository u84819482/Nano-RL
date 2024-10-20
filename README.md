Minimal implemention of [Tabular TD control](https://nbviewer.org/github/u84819482/Nano-RL/blob/main/Tabular_TD_MAZE_solver.ipynb) using SARSA, Expected SARSA, and Q-Learning in a MAZE environment. 

The TD control algorithms are based on Bellman equations. SARSA and Expected SARSA use a sample-based version of the Bellman equation and learn q_pi. Q-Learning uses the Bellman optimality equation and it learns q*. The three learning algorithms are shown below, by highlighting their targets.

<p align="center">
<img src="https://github.com/user-attachments/assets/77eb6b3b-21d9-46f8-aaf0-960e7a0982c2" alt="TD_control_algorithms" width="450"/>

<br>When it comes to environment, the MAZE dimensions can be varied, as well as its cell content: standard 'Blocks' in black, 'Holes' in red with nominally high penalty, and 'Food' in green with nominally high reward. As an example, a 10x15 MAZE with B/H/F fractions of (0.3, 0.1, 0.1) is shown below. The cell placements can be randomly varied while keeping the same fractions. The example in the notebook focuses on a smaller maze to shorten the training.

<p align="center">
<img src="https://github.com/user-attachments/assets/9d87a18a-2e9a-4e4e-a3de-cf368c643f46" alt="Maze" width="350"/>

<br>The MAZE solver offers an opportunity to compare the three TD methods across a vast design space as a function of reward assignments, cell fractions, epsilon, gamma, and alpha. When the impact of 'Holes' and 'Food' is low, either due to their low fraction or low absolute reward, the three methods behave comparably. Otherwise, the training episodes get proportionally longer and the performance of the three methods tends to differ more.

To assist such investigations, the provided code offers several visualizations, e.g., average score vs. episodes: 

<p align="center">
<img src="https://github.com/user-attachments/assets/d1638a9e-005e-46ba-9715-f4fce4096be6" alt="Scores_vs_Episodes" width="350"/>

<br> Agent's trajectory for a specific episode before and after training: 

<p align="center">
<img src="https://github.com/user-attachments/assets/6c02f083-1098-4114-842e-9337ad6dbc37" alt="Example_trajectory" width="500"/>

<br> Animation of Agent's moves for a specific episode before and after training (more GIF examples in 'images' folder): 

<p align="center">
  <img src="https://github.com/user-attachments/assets/920d4330-ebeb-44e1-8cc8-751ddc0eaadd" alt="Expected SARSA_last_exp_episode_1" width="250" style="margin-right: 500">
  <img src="https://github.com/user-attachments/assets/64b47ab3-e186-4236-a4ea-8c6c955ecb87" alt="Expected SARSA_last_exp_episode_30" width="250">
</p>

<br>References:
- https://www.coursera.org/learn/sample-based-learning-methods?specialization=reinforcement-learning
- https://github.com/StrikingLoo/maze-solver?tab=readme-ov-file

