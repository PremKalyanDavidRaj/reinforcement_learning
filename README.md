### Guidelines

1. **Get the codebase:**
   - Open a terminal utility (git-bash for Windows or terminal for MacOS/Linux).
   - Change directory to the home directory.
   - Create a folder named `comp841` or `comp741` if it doesn't exist already.
   - Navigate to the course root directory.
   - Clone lab6 from GitHub into a folder named `lab6`.
   ```
   git clone <URL of file> filename
   ```

2. **Configure Python Conda Environment:**
   - Open VS Code and open the lab6 folder.
   - Open the integrated terminal and switch the shell to git-bash (Windows) or bash (MacOS/Linux).
   - For MacOS/Linux users, disable "Intergrated InheritEnv" in VS Code preferences.
   - Configure the conda environment with the following commands:
   ```
   conda env list
   conda deactivate
   conda create --name rl_env python=3.11
   conda env list
   conda activate rl_env
   conda list
   conda install ipykernel numpy matplotlib
   conda list
   ```

3. **Run the Notebook:**
   - Open and read the `reinforcement_learning.ipynb` notebook in Jupyter.
   - Run each code cell one at a time.
   - To experiment with the initial notebook
        - Run the 'Testing the Agent' code block **five** times, before running 'Training the Agent' cell.
        - Observe the number of steps taken by the agent to move between the start and the goal, as well as the total reward achieved each time.
        - Calculate the average steps and average reward across all **five** test trials.
        - Run the "Training the Agent" cell and test the agent again.
        - Compare the efficiency of the untrained and trained agents in solving the maze.

### Requirements
- Create three new Jupyter Notebook files, one for each test case.

#### Test Case 1 - Single Path Scenario:
Construct a scenario where there is only one viable path leading from the start to the goal.
Investigate how the agent adapts to a straightforward navigation challenge with a singular solution.

- Create a new Jupyter Notebook file named `test_case_1.ipynb`.
- Implement the scenario for the single path.
- Include a markdown cell at the end with "### Observations" and record observations before and after training the agent.

#### Test Case 2 - Multiple Path Scenario:
Create a scenario that offers at least two distinct paths leading from the start to the goal.
Explore how the agent copes with the presence of alternative routes and whether it prioritizes the most efficient path.

- Create a new Jupyter Notebook file named `test_case_2.ipynb`.
- Implement the scenario for the multiple path.
- Include a markdown cell at the end with "### Observations" and record observations before and after training the agent.

#### Test Case 3 - No Path Scenario:
Construct a scenario where there are zero viable paths leading from the start to the goal.
Examine the agent's behavior in an environment without a feasible solution and assess its ability to recognize and handle such situations.

- Create a new Jupyter Notebook file named `test_case_3.ipynb`.
- Implement the scenario for the no path scenario.
- Include a markdown cell at the end with "### Observations" and record observations before and after training the agent.

##### EXPERIMENTS:
For each test case, perform the following experiments:

- **Experiment 1:** Experimenting with Agent Motion Dynamics
  - **Step Size Adjustment:** Modify code cell no. 4 to explore the impact of changing the number of steps the agent takes in each direction. Analyze how this modification affects learning speed and navigation efficiency.
  - **Motion Restriction:** Also, modify code cell no. 4 to investigate the effects of limiting the agent to three directions instead of four. Assess how this restriction influences the learned policy and adaptability.

- **Experiment 2:** Tuning Learning Parameters
  - Change the values of `learning_rate` and `discount_factor` in code cell no. 5 to observe their effects on the learning process. Investigate different combinations' impact on convergence speed and the quality of the learned policy.

- **Experiment 3:** Testing Exploration Settings
  - Adjust the exploration parameters `(exploration_start, exploration_end, and num_episodes)` in code cell no. 5 to observe changes in the agent's behavior. Compare learning curves and the final learned policy for different exploration strategies.
