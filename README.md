# Bipedal Walker 🚀

This project presents a comparative study of three major reinforcement learning algorithms:

* **PPO** (Proximal Policy Optimization) 🟢
* **SAC** (Soft Actor-Critic) 🔵
* **TD3** (Twin Delayed Deep Deterministic Policy Gradient) 🟠

All agents are trained on the continuous control environment:

**BipedalWalker-v3 (Gymnasium)** 🦾

The objective is to analyze training stability, convergence behavior, and overall performance across different RL paradigms (on-policy vs off-policy).

---

## Project Structure 📂

```
Bipedal_Walker/
│
├── bipedal_walker.ipynb
├── Bipedal_Walker.pdf
├── bipedalwalker_algorithms_comparison.png
├── bipedalwalker_ppo.gif
├── bipedalwalker_sac.gif
├── bipedalwalker_td3.gif
│
├── ppo_logs/
├── sac_logs/
└── td3_logs/
```

---

## Environment 🌳

* **Environment:** BipedalWalker-v3
* **Library:** Gymnasium
* **Framework:** Stable-Baselines3
* **Training timesteps per algorithm:** 100,000

This is a continuous control task where the agent must learn to walk using a 4-joint robot.

---

## Algorithms Overview 🧠

### PPO 🟢

* On-policy actor-critic method
* Uses clipped objective to stabilize updates
* Parallel environments (8) used for faster experience collection

### SAC 🔵

* Off-policy method
* Maximizes entropy for better exploration
* Automatic entropy tuning

### TD3 🟠

* Off-policy deterministic algorithm
* Twin critics to reduce overestimation bias
* Delayed policy updates
* Target policy smoothing
* Gaussian action noise

---

## Evaluation Metrics 📊

Training performance is analyzed using:

* Episode reward (raw)
* Episode reward (rolling mean over 50 episodes)
* Episode length (raw)
* Episode length (rolling mean over 50 episodes)

The rolling mean smooths noisy reward signals and reveals convergence trends more clearly.

---

## Results 🎯

The generated comparison plot includes:

1. Raw episode rewards
2. Smoothed episode rewards
3. Raw episode lengths
4. Smoothed episode lengths

The visualization highlights differences in:

* Stability
* Convergence speed
* Sample efficiency

Additionally, GIFs of the trained agents are generated to qualitatively compare learned behaviors.

---

## Key Observations ✨

* **PPO** learns relatively fast but may exhibit instability.
* **SAC** provides smoother and more stable learning.
* **TD3** improves more gradually but remains stable.

This comparison illustrates trade-offs between exploration strategy, stability, and policy update mechanisms.
Complete details can be found on `Bipedal_Walker.pdf`.

---

## How to Run 🏃‍♂️

Install dependencies:

```bash
pip install gymnasium stable-baselines3 matplotlib pandas imageio
```

Then run the notebook:

```bash
jupyter notebook bipedal_walker.ipynb
```

---

## Outputs Generated 🖼️

* `bipedalwalker_algorithms_comparison.png`
* `bipedalwalker_ppo.gif`
* `bipedalwalker_sac.gif`
* `bipedalwalker_td3.gif`

---

## 📜 License

This project is released under the [MIT](https://github.com/sepanta007/Bipedal_Walker/blob/master/LICENSE) License. 