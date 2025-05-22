
# 🎯 Thompson Sampling - Reinforcement Learning on Ad Click Simulation

## 📌 Summary

This project demonstrates the use of **Thompson Sampling**, a reinforcement learning algorithm, to optimize ad selection in a simulated environment. By modeling ad click-through rates using **Bayesian inference**, Thompson Sampling efficiently balances **exploration** and **exploitation** to maximize the total number of ad clicks over time.

The algorithm is applied to a synthetic dataset representing user interactions with 10 ads over 10,000 rounds. Each ad selection is updated based on success (click) or failure (no click) using a beta distribution.

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
- A visual representation of how effectively the algorithm learns over time

---

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
