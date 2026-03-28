# CCPL: Context-Conditioned Parameter Learning  
### Multimodal Time Series Forecasting

Code and pre-processed datasets for paper:  
**"Beyond Fusion: Context-Conditioned Parameter Learning for Multimodal Time Series Forecasting"**   

---

## Overview

We propose **CCPL**, a Transformer-based forecasting framework where contextual text **modulates model parameters** instead of being fused at the representation level. This enables the model to adapt to contextual signals and capture regime shifts in time series. This allows contextual information to **change the forecasting function itself**, not just the inputs.

---

## Method


### 1. Context Encoding
Textual data (facts, preds) is encoded using:
- **Sentence Transformer (all-MiniLM-L6-v2)**

### 2. Context-Conditioned Transformer

Context embeddings modulate:
- Attention projections (Q, K, V)
- Feed-forward layers

---

## Datasets

Evaluated on **Time-MMD benchmark**:
- Agriculture, Social Good, Energy, Traffic, Economy  
- Inputs: numerical time series + text (facts, preds)
- The datasets are obtained from the Time-MMD benchmark (https://github.com/AdityaLab/Time-MMD). The numerical time series and textual data are preprocessed and aligned based on timestamps (dates) to ensure temporal consistency across modalities.
---

## Results

- CCPL achieves **best or competitive performance in 4/5 domains**
- Outperforms fusion and alignment baselines

---

