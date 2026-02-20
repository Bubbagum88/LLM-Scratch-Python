# LLM-Scratch-Python
 
Project Description: Classifier‑LLM System for Algorithm Selection

This project focuses on building a Classifier LLM from the ground up — a Python‑based system designed to analyze 
the structure and statistical properties of a dataset and then predict which classification algorithms are best suited for that dataset. 
Instead of manually testing dozens of models, the system learns patterns across datasets and maps them to algorithmic performance.
Core Idea

Different datasets favor different classifiers. For example, highly nonlinear data might benefit from kernel‑based methods, while 
linearly separable data might perform best with logistic regression. The goal of this project is to automate that reasoning process 
by training a model that can understand dataset characteristics and recommend the most effective classifier(s).

## To-do List Overview:



LLM‑From‑Scratch Workflow

Raw Dataset (CSV)
        │
        ▼
Dataset Profiling Module (Deterministic)
        │
        ▼
Meta-Feature Vector (Structured Numerical Data)
        │
        ▼
Meta-Learning Model (Classical ML Classifier)
        │
        ▼
Ranked Algorithm Recommendations
        │
        ▼
Optional LLM Explanation Layer (Generates textual reasoning)
        │
        ▼
Evaluation Suite (Top-1/Top-3 Accuracy, Performance Gap, Baselines)

# Helpful resources:
https://www.youtube.com/@ShawhinTalebi/





