# LLM-Scratch-Python
 
Project Description: Classifier‑LLM System for Algorithm Selection

This project focuses on building a Classifier LLM from the ground up — a Python‑based system designed to analyze the structure and statistical properties of a dataset and then predict which classification algorithms are best suited for that dataset. Instead of manually testing dozens of models, the system learns patterns across datasets and maps them to algorithmic performance.
Core Idea

Different datasets favor different classifiers. For example, highly nonlinear data might benefit from kernel‑based methods, while linearly separable data might perform best with logistic regression. The goal of this project is to automate that reasoning process by training a model that can understand dataset characteristics and recommend the most effective classifier(s).

## To-do List Overview:
LLM‑From‑Scratch Workflow Checklist
# 1. Data Curation
1.1 Collect Data

    Gather large‑scale text sources

        Public web data (Common Crawl, C4, RefinedWeb)
        Curated datasets (The Pile, HuggingFace corpora)
        Private domain‑specific data
        Optional: LLM‑generated synthetic data (“self‑instruct” style)

1.2 Ensure Dataset Diversity

    --Include multiple domains:
        -Web pages
        -Books
        -Code
        --Scientific articles
        Conversational data
    --Verify diversity aligns with intended model capabilities.

1.3 Prepare the Data

    --Quality filtering
        Classifier‑based filtering
        Heuristic filtering (remove gibberish, toxicity, repeated tokens, etc.)
    --Deduplication
        Remove near‑duplicate documents
        Prevent train/test leakage
    --Privacy redaction
        Strip PII and sensitive content
    --Tokenization
        Train or adopt a BPE/SentencePiece tokenizer
        Generate vocabulary + token IDs

# 2. Model Architecture
2.1 Choose Transformer Type

    --Encoder‑only (classification/embeddings)
    --Decoder‑only (causal LM; most common)
    --Encoder‑decoder (translation, seq2seq)

2.2 Configure Architecture Details

    --Residual connections (pre‑norm or post‑norm)
    --Layer normalization (LayerNorm or RMSNorm)
    --Activation functions (GELU, SwiGLU, etc.)
    --Positional embeddings (absolute or relative)
    --Attention masking (causal mask for decoder‑only)

2.3 Determine Model Size
    Select parameter count (e.g., 1B, 7B, 70B)
    Apply scaling heuristics:
        ~20 tokens per parameter
        10× parameters → ~100× compute

# 3. Training at Scale
3.1 Use Training Optimizations

    Mixed‑precision training (FP16/BF16 + FP32)
    Parallelization strategies:
        Pipeline parallelism
        Tensor/model parallelism
        Data parallelism
    Use ZeRO (Zero Redundancy Optimizer) to reduce memory duplication

3.2 Maintain Training Stability
    Checkpoint frequently
    Apply weight decay
    Use gradient clipping
    Monitor for loss spikes or divergence

3.3 Tune Hyperparameters
    Batch size (static or gradually increased)
    Learning rate schedule:
        Warmup → peak LR → cosine decay
    Optimizer (AdamW or similar)

# 4. Evaluation
    Build evaluation suite (perplexity, downstream tasks, benchmarks)
    Test generalization across domains
    Compare against baseline models
    Validate safety, hallucination rate, and robustness
# Helpful resources:
https://www.youtube.com/@ShawhinTalebi/


