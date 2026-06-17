# Benyamin Gidanian

Los Angeles, CA 90034 · (310) 613-3655 · bgidanian@gmail.com  
[GitHub](https://github.com/ben-gid) · [LinkedIn](https://linkedin.com/in/benyamin-gidanian-46305a364)

---

## Summary

Applied AI/ML engineer who builds and ships systems end-to-end — from fine-tuning and evaluating models to packaging them into production-ready services. Comfortable across the full stack: PyTorch model development, Python backend services (FastAPI, Django), Docker containerization, and CI. Background spans NLP (transformer fine-tuning, token classification), computer vision (transfer learning, class imbalance), and full-stack web development. Moves fast, experiments with new tools and approaches, and focuses on shipping things that work.

---

## Technical Skills

**Core ML/AI:** PyTorch, TensorFlow, Keras, CUDA, Torchvision, BERT, Attention Mechanisms, Hugging Face Transformers, timm, ConvNeXt  
**Algorithms:** Supervised & Unsupervised Learning, CNNs, Neural Networks, Decision Trees, XGBoost, Recommender Systems, Reinforcement Learning (DQN)  
**ML Engineering:** FastAPI, Docker, RESTful APIs, CI, (GitHub Actions), Transfer Learning, Hyperparameter Tuning, Model Evaluation (ROC/AUC, Precision, Recall, F1)  
**Full-Stack / Web:** Django, React, REST API design, SQL (SQLite)  
**Data:** NumPy, Pandas, Feature Engineering, Data Preprocessing  
**Languages:** Python, SQL, JavaScript, C  
**Tools:** Git, Linux, Bash, Pytest, Ruff, Pyright, uv, Jupyter Notebooks, HuggingFace Hub  

---

## Projects

### PII Redaction Toolkit
*PyTorch · DeBERTa-v3 · HuggingFace Trainer/Hub · CLI*
[GitHub](https://github.com/ben-gid/pii_redaction)

- Fine-tuned three DeBERTa-v3 models (base, small, xsmall) on the `ai4privacy/pii-masking-300k` dataset for PII named entity recognition (names, emails, SSNs, phone numbers, etc.) using BIO token classification with subword-aligned labels.
- Built a custom `WeightedTrainer` with class-weighted cross-entropy loss to address label imbalance, and evaluated all models via seqeval entity-level F1.
- Implemented a post-processing layer that aggregates per-token predictions into character-level spans and replaces detected PII with typed placeholders (`[NAME]`, `[EMAIL]`, etc.) at a configurable confidence threshold.
- Built a production CLI for both retraining and redaction; benchmarked GPU inference latency across model sizes and documented distribution-shift behavior and per-model tradeoffs in published model cards on HuggingFace Hub.
- Training tracked end-to-end with Weights & Biases; in progress: FastAPI service + Docker/AWS deployment.

---

### Flower Classification Inference Service
*PyTorch · EfficientNet · FastAPI · Docker · HuggingFace Hub · GitHub Actions*  
[GitHub](https://github.com/ben-gid/flowers) · [Model](https://huggingface.co/bengid/flower-classifier)

- Achieved **>93% test accuracy** on the 102-class Oxford Flowers dataset via two-stage transfer learning of EfficientNet-B0 (classifier-only warm-up, then partial backbone unfreeze with differential learning rates).
- Served the model via a FastAPI service (`/predict`, `/health`) with file-type, size, and image-dimension validation; integrated automatic weight download from HuggingFace Hub on cold start.
- Containerized with Docker with a full CI pipeline (GitHub Actions): Ruff, Pyright, Pytest (model-mocked for GPU-free CI), and Docker build verification on every push.

---

### Network — Full-Stack Social Platform
*Django · React · SQLite · JavaScript*
[GitHub](https://github.com/ben-gid/Network)

- Built a Twitter-style social platform with a Django backend (custom User, Post, Like, and Follow models, including many-to-many relations via through-models) and a React-powered frontend.
- Designed RESTful endpoints for authentication, posting, following, and liking, with server-side validation and Fetch API calls for asynchronous, no-reload post editing, liking, and pagination.

---

### Gravitational Lens Finding — ML4SCI DeepLense (GSoC 2026 Evaluation)
*PyTorch · ConvNeXt-Tiny · EfficientNet-B0 · timm*
[GitHub](https://github.com/ben-gid/deeplense_tests)

- Achieved **0.9887 AUROC** on binary gravitational lens classification (16.6:1 class imbalance) using ConvNeXt-Tiny, and **0.98 macro AUROC** on 3-class substructure classification via two-phase fine-tuning of EfficientNet-B0.
- Addressed severe class imbalance with combined `WeightedRandomSampler` oversampling and calibrated `BCEWithLogitsLoss` pos-weighting.

---

### Additional Projects

- **ML Fundamentals Library** *(Python, NumPy, Pytest)* — Built a from-scratch ML library (Linear/Logistic Regression, K-Means, Decision Trees, multi-layer NN with manual backprop) with 100% test coverage and a custom AST-based doc generator. [GitHub](https://github.com/ben-gid/ml_fundamentals)
- **DQN for Autonomous Lunar Landing** *(TensorFlow, Keras, Gymnasium)* — Implemented a DQN agent with experience replay and soft-update target networks, solving LunarLander-v3 with a rolling average score above 200. [GitHub](https://github.com/ben-gid/LunarLander)
- **Crossword Generator** *(Python, CSP/AC-3)* — Built a constraint satisfaction solver using AC-3 arc consistency plus MRV/LCV heuristics, reducing backtracking search space by over 80%. [GitHub](https://github.com/ben-gid/Crossword)

---

## Professional Experience

### One-on-One Talmud Tutor
**Mesivta Bircas Yitzchok** · Sept 2023 – March 2025

- Delivered individualized instruction over a 1.5-year engagement, developing structured curricula to accelerate comprehension and long-term retention.

---

## Education & Certifications

**Machine Learning Specialization** — Stanford University & DeepLearning.AI (Coursera)  
Supervised Learning, Neural Networks, Decision Trees, Unsupervised Learning, Recommender Systems

**Harvard CS50 Suite** — Harvard University (EdX)  
CS50x (C, Python, SQL, Algorithms) · CS50p (OOP, Testing) · CS50ai (Search, Logic, Optimization) · CS50w (Django, React, CI/CD)