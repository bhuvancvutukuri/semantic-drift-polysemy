# Predicting Semantic Drift from Polysemy Density

This project investigates whether polysemous words (words with multiple senses) are more prone to semantic drift over time. Using WordNet and diachronic word embeddings (HistWords), we compute polysemy density and track semantic movement across decades from 1800 to 1990.

## 🔍 Key Steps

- Load top 5000 words from each decade using HistWords
- Filter to words appearing in all decades with ≤10 noun senses
- Compute polysemy density using WordNet
- Measure semantic drift as average cosine distance across decade embeddings
- Analyze correlation between density and drift

## 📁 Repo Contents

- `data/` — CSVs for targets, density, and drift
- `figures/` — Final scatter plot
- `notebooks/` — Analysis notebook (`pro.ipynb`)
- `environment.yml` — Conda environment for reproducibility

## 📈 Key Result

> Pearson r = –0.188 (p < 0.00001), indicating a weak but significant negative correlation between polysemy and semantic drift.

## 📦 How to Run

```bash
conda env create -f environment.yml
conda activate drift-env
jupyter notebook notebooks/pro.ipynb
