Here's the direct **README.md** content you can use for your repository:

```markdown
# Autonomous Driving in CARLA using Deep Reinforcement Learning

This project implements an autonomous driving agent using Deep Reinforcement Learning (DRL) in the CARLA simulator. The agent is trained using **Proximal Policy Optimization (PPO)** with a **Variational Autoencoder (VAE)** to process sensory input efficiently.

## 🚀 Project Overview

- **Simulator**: CARLA 0.9.8
- **Deep RL Algorithm**: PPO (Proximal Policy Optimization)
- **Feature Extraction**: Variational Autoencoder (VAE)
- **Training Mode**: Continuous Action Space for smooth driving

---

## 📦 Installation

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/GowhithGandem46/Autonomous-Driving-in-Carla-using-Deep-Reinforcement-Learning.git
cd Autonomous-Driving-in-Carla-using-Deep-Reinforcement-Learning
```

 2️⃣ Set Up a Virtual Environment
```bash
python -m venv venv
source venv/bin/activate  # On Windows, use venv\Scripts\activate
```

### 3️⃣ Install Dependencies
```bash
pip install -r requirements.txt
cd poetry/
poetry update
```

### 4️⃣ Set Up CARLA
- Download CARLA 0.9.8 and the **Additional Maps** package.
- Copy the additional maps into the main CARLA directory.
- Run the CARLA server **before** starting the agent.

---

## 🎮 Running the Agent

To test a pre-trained agent:**
```bash
python continuous_driver.py --exp-name=ppo --train=False
```

To train a new agent:**
```bash
python continuous_driver.py --exp-name=ppo --train=True
```

🔹 By default, the agent operates in **Town 07**. To switch to **Town 02**, add `--town Town02`.

---

## 📁 Project Structure

```
📦 Autonomous-Driving-in-Carla
├── 📝 README.md              # Project Documentation
├── 📂 autoencoder/           # Variational Autoencoder (VAE) model
├── 📂 checkpoints/           # Saved model checkpoints
├── 📂 logs/                  # Training logs
├── 📂 networks/              # RL Model architectures (PPO, CNN, etc.)
├── 📂 preTrained_models/     # Pre-trained models
├── 📂 simulation/            # CARLA environment setup
├── 🔹 continuous_driver.py   # RL Training and Testing script
├── 🔹 discrete_driver.py     # Dueling DQN-based driver (alternative)
├── 🔹 encoder_init.py        # Loads trained VAE for observations
├── 🔹 parameters.py          # Hyperparameters for training
└── 🔹 requirements.txt       # Dependencies
```

---

## 📊 Monitoring Training

To visualize training progress in **TensorBoard**:
```bash
tensorboard --logdir runs/
```

---
