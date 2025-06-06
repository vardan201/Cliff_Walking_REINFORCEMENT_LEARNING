# 🧠 Cliff Walking Reinforcement Learning Agent with Visualization

This repository contains a complete implementation of a **Q-learning agent** that learns to solve the **Cliff Walking** environment from OpenAI Gym. The project is structured in two Jupyter notebooks:

- `agent.ipynb`: for training the agent
- `visualization.ipynb`: for visualizing the learned policy and behavior

The implementation is simple, educational, and designed to run smoothly in **Google Colab**.

---

## 🧩 Environment Overview

- Environment: `CliffWalking-v0` from `gym`
- Grid Size: 4 rows × 12 columns
- Start State: Bottom-left corner (S)
- Goal State: Bottom-right corner (G)
- Cliff: Cells between S and G — stepping on these gives a reward of **-100**
- Rewards:
  - Step: **-1**
  - Cliff: **-100**
  - Goal: **0**

---

## 🧠 Algorithm - Q-learning

The agent uses the Q-learning algorithm to learn the optimal path while avoiding the cliff.

### 🔧 Q-learning Formula:


### 🔍 Hyperparameters:
- `episodes`: Number of training episodes (e.g., 500)
- `alpha`: Learning rate (e.g., 0.1)
- `gamma`: Discount factor (e.g., 0.99)
- `epsilon`: Exploration rate (starts at 1.0 and decays)

---

## 📁 Repository Structure

| File                 | Description                                                                 |
|----------------------|-----------------------------------------------------------------------------|
| `agent.ipynb`        | Implements Q-learning, trains the agent, and saves the learned Q-table.     |
| `visualization.ipynb`| Loads the Q-table and visualizes the policy, value map, and optimal path.   |

---

## 🧪 Google Colab Usage

Both notebooks are tested and run-ready on **Google Colab**.

### ➤ To get started:
1. Upload both notebooks to [Google Colab](https://colab.research.google.com/).
2. Run `agent.ipynb` to train the model.
3. Save the resulting `q_table.npy`.
4. Upload the `q_table.npy` file into Colab.
5. Run `visualization.ipynb` to visualize the learned policy.

---

## 🛠 Installation (For Local Setup)

To run locally, install the required Python packages:

```bash
pip install gym numpy matplotlib
🚀 How to Use
Step 1️⃣: Train the Agent
Open agent.ipynb and run all the cells:

The environment is initialized.

The Q-table is updated using Q-learning.

Exploration is reduced over time using an epsilon decay strategy.

The final Q-table is saved using NumPy.

Step 2️⃣: Visualize the Learned Policy
Open visualization.ipynb:

Load the saved q_table.npy file.

Convert Q-values to a deterministic policy.

Visualize:

Arrows showing best action in each state.

Value heatmap (how good each state is).

Optimal path from start to goal avoiding the cliff
