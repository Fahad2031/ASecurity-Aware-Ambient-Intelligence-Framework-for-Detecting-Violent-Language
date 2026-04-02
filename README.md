# 📘 ASecurity-Aware Ambient Intelligence Framework for Detecting Violent Language in Airline Customer Reviews

## 🔍 Overview
This repository provides the official implementation accompanying our MDPI submission on a **security-aware ambient intelligence framework** for detecting violent and threatening language in airline customer reviews.  

The framework leverages natural language processing (NLP) and supervised machine learning to identify safety-critical signals in user-generated content, supporting **proactive risk monitoring** in aviation service environments.  

Unlike traditional sentiment analysis systems, this work focuses on **rare but high-impact threatening expressions**, addressing challenges such as **class imbalance**, **context ambiguity**, and **synthetic data augmentation**.


## ❓ Problem Statement
Airline customer reviews may contain implicit or explicit threats that can indicate safety risks. However, such instances are:

- Rare (severe class imbalance)  
- Context-dependent  
- Often misclassified by standard sentiment models  

This creates a need for **security-aware intelligent systems** capable of detecting harmful intent beyond polarity analysis.


## 🎯 Research Objectives
- Develop a multi-class classification framework for detecting violent language  
- Evaluate model robustness under **imbalanced and partially synthetic datasets**  
- Analyze model behavior through **systematic error analysis**  
- Assess applicability in **real-world operational settings**


## 🧠 Contributions
- A **security-aware ambient intelligence framework** tailored to airline review analysis  
- A **multi-class classification scheme** (non-harmful, negative, threatening)  
- A full **experimental pipeline** including preprocessing, training, and evaluation  
- A detailed **error analysis with taxonomy and real examples**  
- An empirical study on **class imbalance and synthetic data effects**  
- A **reproducible implementation** for research and deployment  


## 📊 Dataset Description

| Attribute | Description |
|----------|------------|
| Domain | Airline customer reviews |
| Classes | 0: Non-harmful, 1: Negative, 2: Threatening |
| Data Sources | Real reviews + synthetically generated threatening samples |
| Key Challenge | Severe class imbalance |

### ⚠️ Important Note on Synthetic Data
To address the scarcity of threatening content, synthetic samples were introduced.  

To ensure evaluation integrity:

- Synthetic data is **restricted to training (where applicable)**  
- Test data is **carefully controlled to avoid leakage**  

## ⚙️ Methodology

### Pipeline
1. Data preprocessing and cleaning  
2. Feature extraction (e.g., TF-IDF / embeddings)  
3. Model training  
4. Performance evaluation  
5. Error analysis  

### Models Evaluated
- Logistic Regression (baseline)  
- (Optional extension) Transformer-based models (e.g., BERT)

## 📈 Experimental Setup

### Evaluation Metrics
- Accuracy  
- Precision, Recall, F1-score (per class)  
- Confusion Matrix  

### Key Focus
Special emphasis is placed on:

- **Recall of the threatening class (minority class)**  
- Trade-offs between precision and recall  


## ⚖️ Handling Class Imbalance

To mitigate imbalance effects, the following strategies are explored:

- Class weighting  
- Threshold tuning  
- (Optional) Oversampling techniques (e.g., SMOTE)


## 🧪 Results Summary
The results indicate that:

- The model performs well on majority classes  
- Detection of threatening content remains challenging due to:
  - Data scarcity  
  - Linguistic ambiguity  

This highlights the importance of **imbalance-aware learning strategies**.


## 🔍 Error Analysis

A structured error analysis was conducted using confusion matrices and manual inspection.

### Key Error Types

| Error Type | Example | Explanation |
|-----------|--------|------------|
| False Negative (Threat missed) | “You will regret this” | Implicit threat, lacks explicit keywords |
| False Positive | “This delay is killing me” | Figurative expression misclassified |
| Ambiguous Context | “I’ll take action” | Requires contextual interpretation |

### Insights
- The model struggles with **implicit and sarcastic threats**  
- Threshold tuning can improve minority class detection  
- Context-aware models may further enhance performance  


## 🌍 Operational Validation Scenario

To approximate real-world deployment:

- Class distributions were analyzed under **imbalanced conditions**  
- The framework is designed for:
  - Real-time monitoring  
  - Integration with airline feedback systems  
  - Alert generation for high-risk content  

## 🔁 Reproducibility

To ensure full reproducibility:

- Fixed random seeds are used  
- All preprocessing steps are documented  
- Configuration files are provided  

