# Benyamin Gidanian

Los Angeles, CA 90034 · (310) 613-3655 · bgidanian@gmail.com  
[GitHub](https://github.com/ben-gid) · [LinkedIn](https://linkedin.com/in/benyamin-gidanian-46305a364)

---

## Summary

Applied ML/AI engineer with hands-on experience building end-to-end systems in PyTorch and TensorFlow — from custom CNN architectures and training pipelines to FastAPI inference services and Dockerized deployments. Expanding into NLP, LLMs, and multimodal systems with a focus on production-quality, reproducible implementations. Strong foundations in algorithmic correctness, training stability, and GPU-accelerated computation.

---

## Technical Skills

**Core ML/AI:** PyTorch, TensorFlow, Keras, CUDA, Torchvision, BERT, Attention Mechanisms, Hugging Face Transformers  
**Algorithms:** Supervised & Unsupervised Learning, CNNs, Neural Networks, Decision Trees, XGBoost, Recommender Systems, Reinforcement Learning (DQN)  
**ML Engineering:** FastAPI, Docker, RESTful APIs, CI/CD (GitHub Actions), Transfer Learning, Hyperparameter Tuning, Model Evaluation (Precision, Recall, F1)  
**Data:** NumPy, Pandas, Feature Engineering, Data Preprocessing  
**Languages:** Python, SQL, JavaScript, C  
**Tools:** Git, Linux, Bash, Pytest, Ruff, Pyright, uv, Jupyter Notebooks, HuggingFace Hub  

---

## Projects

### Flower Classification Inference Service
*PyTorch · EfficientNet · FastAPI · Docker · HuggingFace Hub · GitHub Actions*  
[GitHub](https://github.com/ben-gid/flowers) · [Model](https://huggingface.co/bengid/flower-classifier)

- Achieved **>93% test accuracy** on the 102-class Oxford Flowers dataset via two-stage fine-tuning of EfficientNet-B0 — a 30-point improvement over a custom CNN (63%) trained from scratch on the same data.
- Implemented a two-stage transfer learning pipeline: classifier-only warm-up (20 epochs) followed by partial backbone unfreeze with **differential learning rates** per layer group (1e-5 → 1e-3), preserving low-level ImageNet features while adapting high-level representations.
- Applied class-balanced sample weighting via `sklearn.utils.compute_class_weight` to handle Oxford-102's uneven class distribution, combined with CosineAnnealingLR scheduling and AdamW optimization.
- Built a custom `FlowerDataset` class (parsing MATLAB `.mat` label files via `scipy.io`) and a `SubsetWithTransform` wrapper enabling per-split augmentation pipelines on shared dataset objects — filling a gap in native `torchvision` tooling.
- Served both models simultaneously via a FastAPI service with a shared lifespan context (`/predict`, `/predict/scratch`, `/health`), enforcing file-type, size (≤ 5 MB), and minimum dimension (224×224) validation.
- Integrated HuggingFace Hub for automatic weight download on cold start; containerized with Docker for reproducible deployment.
- Enforced code quality with a full CI pipeline (GitHub Actions): Ruff linting, Pyright type checking, Pytest suite (model-mocked for GPU-free CI), and Docker build verification on every push.

---

### ML Fundamentals Library
*Python · NumPy · Matplotlib · Pytest*  
[GitHub](https://github.com/ben-gid/ml_fundamentals)

- Built a fully-tested, NumPy-only ML library from scratch spanning 6+ core algorithms including Linear/Logistic Regression, K-Means, Decision Trees, and a multi-layer Neural Network with manual backpropagation.
- Implemented gradient computation by hand, enabling transparent insight into forward/backward pass dynamics and training stability.
- Optimized numerical routines through vectorization for significant runtime performance gains over naive loop-based approaches.
- Enforced reproducibility and documentation quality with 100% Pytest coverage and a custom AST-based documentation generator.

---

### Deep Q-Network (DQN) for Autonomous Lunar Landing
*TensorFlow · Keras · Gymnasium · Python*  
[GitHub](https://github.com/ben-gid/LunarLander)

- Implemented a DQN agent from scratch to solve the LunarLander-v3 environment, reaching the solved threshold with a sustained rolling average score above 200.
- Engineered training stability via Experience Replay (deque buffer) and Target Networks with soft updates (τ=0.001) to reduce Q-value divergence.
- Accelerated training with `tf.function` graph-mode compilation, reducing per-episode compute time.

---

### Multimodal E-Commerce Recommendation System *(In Progress)*
*PyTorch · Hugging Face Transformers · FastAPI*  
[GitHub](https://github.com/ben-gid)

- Building a multimodal ML pipeline combining image classification, NLP embeddings, and a collaborative filtering recommender on the Amazon Reviews / UCSD dataset.
- Architecture integrates a CNN-based visual encoder, sentence-transformer text encoder, and a learned similarity model to improve product recommendations across modalities.

---

### Crossword Puzzle Generator (Constraint Satisfaction Solver)
*Python*  
[GitHub](https://github.com/ben-gid/Crossword)

- Implemented a CSP solver to generate dense crossword grids, reducing the backtracking search space by over 80% using AC-3 arc consistency.
- Integrated MRV and LCV heuristics for improved constraint propagation speed and solution quality.

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