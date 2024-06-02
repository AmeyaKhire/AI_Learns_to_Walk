# AI Agent Learns To Walk

## Project Overview

This project demonstrates the process of training a reinforcement learning agent to walk using the `BipedalWalker-v3` environment from OpenAI Gym. The agent employs the Soft Actor-Critic (SAC) algorithm, a model-free, off-policy actor-critic method, to learn how to navigate and balance in a simulated environment.

## Environment Setup

The project utilizes several libraries and tools to set up the environment, manage virtual displays, and facilitate rendering. Key libraries include `gymnasium`, `pybullet`, `pyvirtualdisplay`, and `tf-agents`. The environment setup involves installing dependencies and creating a virtual display for rendering purposes in headless systems.

## Training the Agent

The agent is trained using the SAC algorithm, which is implemented using TensorFlow Agents (`tf-agents`). The training process involves:

1. **Initializing the Environment**: The `BipedalWalker-v3` environment is loaded, and its specifications (actions, observations, rewards) are obtained.

2. **Defining the Model**: The actor and critic networks are defined, specifying the architecture and parameters for each. The SAC agent is then initialized with these networks.

3. **Data Collection**: A random policy is used to collect initial experiences, which are stored in a replay buffer managed by Reverb.

4. **Training Loop**: The agent is trained over a specified number of iterations. During each iteration, the agent collects new experiences, updates its policy based on these experiences, and evaluates its performance periodically.

5. **Evaluation**: The agent's performance is evaluated periodically, and metrics such as average return are logged to track progress.

6. **Saving the Model**: The trained policy is saved at regular intervals for future use or deployment.

## Evaluation and Visualization

After training, the agent's performance is evaluated by running several episodes in the environment. A video is generated to visually demonstrate the agent's walking behavior. The video is embedded in the project documentation to provide an illustrative example of the agent's capabilities.

## Results and Metrics

The performance of the agent is measured using metrics such as average return over multiple episodes. These metrics are logged and plotted to visualize the agent's learning progress over time. The training and evaluation results are crucial for understanding the effectiveness of the reinforcement learning algorithm and the improvements made by the agent.

## How to Run the Project

1. **Clone the Repository**: Clone the project repository from GitHub to your local machine.
   
   ```bash
   git clone https://github.com/your-username/ai-agent-learns-to-walk.git
   ```

2. **Install Dependencies**: Navigate to the project directory and install the required dependencies using pip.
   
   ```bash
   cd ai-agent-learns-to-walk
   pip install -r requirements.txt
   ```

3. **Run the Training Script**: Execute the training script to start the training process.
   
   ```bash
   python train.py
   ```

4. **Evaluate the Agent**: After training, run the evaluation script to generate performance metrics and visualize the agent's behavior.
   
   ```bash
   python evaluate.py
   ```

## Conclusion

This project demonstrates the application of the SAC algorithm to train a bipedal walker agent in a simulated environment. By leveraging reinforcement learning techniques, the agent learns to navigate and balance, showcasing the potential of AI in solving complex control tasks.

## References

- [Gymnasium](https://gymnasium.farama.org/)
- [PyBullet](https://pybullet.org/)
- [TensorFlow Agents](https://www.tensorflow.org/agents)
- [Soft Actor-Critic (SAC)](https://arxiv.org/abs/1812.05905)
