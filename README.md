
# NLP_SEM_EVAL


## Overview
NLP_SEM_EVAL is an evaluation project for SemEval-style natural language processing tasks. The repository centralizes datasets, baselines, training/evaluation scripts, and submission guidelines. It is designed for reproducible experiments across languages and models.

Version history (brief)
- V1: Starter kit configuration.
- V2: 10 epochs training.
- V3: 20 epochs + early stopping; LR 2e-5.
- V4: 20 epochs + early stopping; LR 1e-5.
- V5: 20 epochs + early stopping; planned LR 3e-5 experiments.
- V6: mdeBERTa-v3 with V3 hyperparameters.
- V7: Auto Bayesian optimization and grid search.

## Project summary
Lightweight repository for running baseline experiments and producing SemEval-style submissions for dimensional aspect-based sentiment (valence–arousal) tasks. Focus is on reproducible training / prediction pipelines and the starter-kit baselines.

## What is here
- scripts/ : training, inference, evaluation helpers (baseline code)
- data/ : datasets used for experiments (train/dev/test per task)
- models/ : checkpoints and config for experiments
- requirements.txt : python deps (install PyTorch with CUDA manually if needed)

## Quick start
1. Install dependencies: python -m pip install -r requirements.txt (install CUDA-enabled torch manually if you want GPU).

## Version log (V1 → V7)
- V1 — Starter kit baseline and repo layout (minimal config).
- V2 — Training runs set to 10 epochs (baseline evaluation).
- V3 — 20 epochs + early stopping; LR increased to 2e-5 for quick ablation.
- V4 — 20 epochs + early stopping; LR reverted to 1e-5 after validation.
- V5 — 20 epochs + early stopping; plan to test LR = 3e-5 after observing faster learning.
- V6 — Swap model to mDeBERTa-v3 while keeping V3 hyperparams for comparison.
- V7 — Automated hyperparameter search (Bayesian / grid) across languages and domains.

Each version corresponds to an experiment branch and (when applicable) a model checkpoint stored under models/.

## Datasets (brief)
The repo uses the shared-task datasets for DimABSA / DimStance. Main data highlights used in experiments:
- English: Restaurant, Laptop domains
- Chinese: Restaurant, Laptop, Finance
- Additional languages / domains available in data/ (see filenames for language/domain)
