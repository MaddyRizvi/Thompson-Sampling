
# 🎯 Thompson Sampling - Reinforcement Learning on Ad Click Simulation

## 📌 Summary

This project demonstrates the use of **Thompson Sampling**, a reinforcement learning algorithm, to optimize ad selection in a simulated environment. By modeling ad click-through rates using **Bayesian inference**, Thompson Sampling efficiently balances **exploration** and **exploitation** to maximize the total number of ad clicks over time.

The algorithm is applied to a synthetic dataset representing user interactions with 10 ads over 10,000 rounds. Each ad selection is updated based on success (click) or failure (no click) using a Beta distribution, allowing the model to balance exploration and exploitation probabilistically. **Compared to UCB, Thompson Sampling adapts faster and performs better with early stage learning**

---

## 📂 Dataset

The dataset used is `Ads_CTR_Optimisation.csv`, where:
- Each row corresponds to a single user interaction (round)
- Each column represents a different ad (10 total)
- The values are binary: `1` (clicked) or `0` (not clicked)

---

## 🧱 Project Structure

```
thompson-sampling-ads/
│
├── thompson_sampling.py        # Main script implementing Thompson Sampling
├── Ads_CTR_Optimisation.csv    # Simulated dataset of ad click responses
├── README.md                   # Project overview and setup instructions
├── CONTRIBUTING.md             # Guidelines for contributing
└── requirements.txt            # Python dependencies
```

---

## 🛠 Requirements

- Python 3.x  
- pandas  
- numpy  
- matplotlib

Install dependencies with:

```bash
pip install -r requirements.txt
```

Or manually:

```bash
pip install pandas numpy matplotlib
```

---

## 🚀 How to Run

Ensure `Ads_CTR_Optimisation.csv` is in your project directory. Then run:

```bash
python thompson_sampling.py
```

---

## 📈 Output

- A histogram showing how many times each ad was selected
- Total reward (number of clicks) achieved by the algorithm
- A visual representation of how effectively the algorithm learns over time (10000 and 500 users)
  
  ![Image](https://github.com/user-attachments/assets/688c5f10-8260-46e5-ab80-77b54517d8a7)
  
  ![Image](https://github.com/user-attachments/assets/675dfcf8-414a-4ebe-9329-f5e053ea11a9)
---

✅ Key Observations
Histogram of Ads Selection
Thompson Sampling tends to focus faster on the best-performing ads by modeling uncertainty through probability distributions (Beta distribution), leading to smarter exploration.

✅ Total Reward (Clicks)
In simulations with both 10,000 and 500 users, Thompson Sampling consistently delivers a higher cumulative reward (more ad clicks) than UCB. This is because it uses a probabilistic approach to estimate the potential payoff of each ad, rather than relying solely on deterministic upper bounds.

✅ Fast Adaptation with Small Data
With only 500 rounds, UCB struggles to gather enough data to make confident decisions and tends to over-explore or under-exploit.
In contrast, Thompson Sampling adapts faster, making it far more efficient in environments with limited data or early-stage learning.

## ⚙️ Details

- **Algorithm**: Thompson Sampling (Bayesian approach)
- **Problem**: Multi-Armed Bandit
- **Exploration/Exploitation**: Modeled using the Beta distribution
- **Distribution Update**: Posterior updated per ad with observed click data

---

## 🧠 Understanding

Thompson Sampling is a probabilistic algorithm that:
- Samples from a beta distribution for each ad
- Selects the ad with the highest sampled value
- Updates its belief (distribution) based on the observed outcome (click or not)

This results in a natural and efficient balance between trying new ads and choosing known best-performers.

---

## 🤝 Contributing

We welcome contributions! See [CONTRIBUTING.md](./CONTRIBUTING.md) for instructions.

---

## 📜 License

This project is licensed under the MIT License.
