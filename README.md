# LLM-Scratch-Python
 
Project Description: Classifier‑LLM System for Algorithm Selection

This project focuses on building a Classifier LLM from the ground up — a Python‑based system designed to analyze the structure and statistical properties of a dataset and then predict which classification algorithms are best suited for that dataset. Instead of manually testing dozens of models, the system learns patterns across datasets and maps them to algorithmic performance.
Core Idea

Different datasets favor different classifiers. For example, highly nonlinear data might benefit from kernel‑based methods, while linearly separable data might perform best with logistic regression. The goal of this project is to automate that reasoning process by training a model that can understand dataset characteristics and recommend the most effective classifier(s).

## To-do List Overview:



LLM‑From‑Scratch Workflow
                    ┌────────────────────────┐
                    │   Raw Dataset (CSV)    │
                    └──────────┬────────────┘
                               │
                               ▼
                  ┌───────────────────────────┐
                  │ Dataset Profiling Module   │
                  │  (Deterministic)          │
                  │---------------------------│
                  │ - n_samples               │
                  │ - n_features              │
                  │ - feature types           │
                  │ - sparsity, missing %     │
                  │ - correlation/skewness    │
                  │ - class imbalance/entropy │
                  └──────────┬────────────────┘
                             │
                             ▼
               ┌─────────────────────────────┐
               │ Meta-Feature Vector         │
               │ (Structured Numerical Data)│
               └──────────┬──────────────────┘
                          │
                          ▼
       ┌─────────────────────────────┐
       │ Meta-Learning Model          │
       │ (Classical ML Classifier)    │
       │-----------------------------│
       │ Input: meta-features        │
       │ Output: algorithm ranking   │
       └──────────┬──────────────────┘
                  │
       ┌──────────┴───────────┐
       │                      │
       ▼                      ▼
┌───────────────┐     ┌──────────────────┐
│ Ranked Algorithm│     │ Optional LLM     │
│ Recommendations │     │ Explanation Layer│
│ (Top-1, Top-3) │     │  Converts ranking│
└───────────────┘     │  into natural text│
                      └──────────┬────────┘
                                 │
                                 ▼
                        ┌──────────────────┐
                        │ Evaluation Suite │
                        │-----------------│
                        │ Top-1 / Top-3    │
                        │ Accuracy         │
                        │ Performance Gap  │
                        │ Baseline Comparison │
                        └──────────────────┘

# Helpful resources:
https://www.youtube.com/@ShawhinTalebi/



