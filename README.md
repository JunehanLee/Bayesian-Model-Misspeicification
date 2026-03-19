# Bayesian Model Robustness under Misspecification (PyMC)

## 📌 Overview
This project investigates how different Bayesian inference methods behave under **model misspecification**, a common issue in real-world marketing and consumer data.

Traditional Bayesian models rely on correctly specified likelihoods, which often fail in practice due to:
- unobserved heterogeneity  
- non-linear relationships  
- heavy-tailed noise  

To address this, this project compares:
- Classical Bayesian inference  
- Quasi-Bayesian methods (BCE, SPH loss)  
- Generalized Bayesian inference (KSD-Bayes)  

The focus is on **model robustness and reliability under realistic data conditions**.

---

## 🚀 Key Contributions

- Built **hierarchical Bayesian models in PyMC** to simulate real-world marketing scenarios  
- Designed **5 misspecification scenarios** including:
  - utility misspecification (missing interactions / non-linearities)
  - heavy-tailed and contaminated error distributions  
- Benchmarked **multiple inference approaches** across controlled simulations  
- Evaluated performance using:
  - Log-loss (predictive accuracy)
  - Brier score (calibration)
  - Accuracy (decision performance)  

---

## 🧠 Why This Matters

In real-world applications, models are almost always **misspecified**.

This project shows that:
- Classical Bayesian methods degrade significantly under misspecification  
- Quasi-Bayesian methods (especially SPH) provide **more stable performance**  
- Generalized Bayesian (KSD) can be robust to heavy-tailed noise but struggles in complex models  

👉 This highlights the importance of **robust probabilistic modelling for decision-making systems**

---

## ⚙️ Methodology

### Data Simulation
A synthetic CRM / e-commerce environment was created to reflect real-world data:

- Customer segments (heterogeneity)
- Purchase history (non-linear effects)
- Discount interactions
- Heavy-tailed noise (Cauchy, t-distribution, contaminated normal)

👉 Designed to mimic real marketing datasets where assumptions often fail :contentReference[oaicite:0]{index=0}

---

### Model Setup

- Hierarchical Bayesian models with partial pooling  
- Implemented in **PyMC (NUTS sampling)**  
- Compared:
  - Likelihood-based Bayesian  
  - Loss-based quasi-Bayesian  
  - KSD-based generalized Bayesian  

---

### Evaluation

Models were evaluated on:

- **Log-loss** → predictive performance  
- **Brier score** → calibration  
- **Accuracy** → decision-level outcomes  

---

## 📊 Results

### 1. Utility Misspecification
- Classical and BCE-based methods behave similarly  
- SPH improves accuracy but slightly worsens calibration  
- KSD remains insensitive to model improvements and underperforms in complex settings  

📈 See figures in `/figures` (e.g., performance comparison across model variants)

---

### 2. Error Distribution Misspecification
- Classical Bayesian degrades under heavy-tailed noise  
- SPH shows **strong overall robustness**  
- KSD performs well in simple models but degrades in high-complexity settings  

---

## 🧪 Experiments

- All experiments are implemented in **Jupyter notebooks**  
- Fully reproducible simulation pipeline  
- Includes:
  - data generation
  - model fitting
  - evaluation
  - visualisation  

👉 See `/experiments` for full workflow

---

## 📁 Repository Structure

'''text
├── README.md
├── docs/
│ └── paper.pdf
├── experiments/
│ └── notebooks (full pipeline)
├── src/
│ └── model implementations
├── figures/
│ └── result visualisations
└── results/
---
## 🛠 Tech Stack

- Python  
- PyMC  
- NumPy / Pandas  
- Bayesian inference (MCMC, NUTS)  
- Simulation-based evaluation  

---

## 📄 Full Paper

Full dissertation available here:  
👉 `/docs/paper.pdf`

---

## 🔍 Key Takeaway

👉 **Model correctness cannot be assumed in real-world data**

This project demonstrates that:
- Robust Bayesian approaches are critical for reliable decision-making  
- Loss-based and generalized Bayesian methods offer practical alternatives  
- The choice of method should depend on **data complexity and noise structure**

---

## 📬 Contact

If you're interested in Bayesian modelling or this work, feel free to reach out.
