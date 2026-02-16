GAFR-Net: A Graph Attention and Fuzzy-Rule Network for Interpretable Breast Cancer Image Classification

Introduction
This repository is the official implementation of the paper: "GAFR-Net: A Graph Attention and Fuzzy-Rule Network for Interpretable Breast Cancer Image Classification".

GAFR-Net is an intrinsically interpretable deep learning framework specifically engineered for histopathology image classification under limited supervision (where less than 10% of samples are labeled). By synergizing Multi-head Graph Attention Networks (GAT) with a Trainable Fuzzy-Rule Module, the model establishes transparent "IF-THEN" diagnostic logic that mimics the heuristic deduction process of medical experts.

Workflow
The framework follows an end-to-end relational learning and reasoning pipeline:

Environment Setup: Install dependencies via requirements.txt (Recommended: Python 3.10, PyTorch 2.0.1).
Graph Construction: Builds a similarity-driven graph based on cosine similarity between image features. The sparsity is controlled by a threshold τ = 0.75.
Topological Feature Extraction: Computes three key descriptors for each node: Clustering Coefficient, Node Degree, and Two-hop Label Agreement.
Model Training: The architecture integrates 4 attention heads and a differentiable fuzzy-rule layer.
Run main.py to start training with a default learning rate of 0.0001 for 50 epochs.
Interpretable Inference: The model outputs a classification (e.g., Malignant/Benign) alongside a traceable "IF-THEN" reasoning path grounded in graph topology.

Datasets
The datasets used in this research are publicly available and can be found on Kaggle or their respective official repositories:

BreakHis: Breast cancer histopathology images at 40x, 100x, 200x, and 400x magnifications.
Mini-DDSM: Annotated mammography images for lesion diagnosis.
ICIAR2018 (BACH): HE-stained images categorized into Normal, Benign, In-situ, and Invasive carcinoma.

Development Status & Update Plan
Notice: Due to current time constraints, this repository currently contains the core logic and skeleton of GAFR-Net.
A comprehensive update is scheduled for release in two weeks, which will include:

Full data preprocessing pipelines for whole-slide images.
Complete ablation study scripts.
Pre-trained model weights for all three benchmark datasets.
Advanced visualization tools for fuzzy rule activation maps.

Citation
If you find this work useful for your research, please cite our paper:

Gao, L-G.; Liu, S. GAFR-Net: A Graph Attention and Fuzzy-Rule Network for Interpretable Breast Cancer Image Classification. Preprints 2022.
