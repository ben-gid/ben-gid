# Hi — I'm Benyamin Gidanian 👋

Applied ML/AI engineer in Los Angeles building end-to-end systems from raw data to deployed, tested inference services. I built my foundation through Harvard's CS50 and Stanford's Machine Learning Specialization, and I'm currently expanding into **NLP, LLMs, RAG, and MLOps** — shipping real projects at each step.

---

### 🔭 What I'm Working On

* **Domain Intelligence Platform** *(in progress)* — fine-tuning a DistilBERT/DeBERTa model on domain-specific text, governed by a full MLOps pipeline (W&B experiment tracking, versioned model registry, Evidently drift detection, automated challenger/champion promotion), with a LangChain RAG layer for semantic querying over a document corpus — deployed on AWS ECS Fargate
* Deepening production ML skills: model versioning, drift monitoring, RAG evaluation with RAGAS, and cloud-native serving

---

### 🛠️ Tech Stack

**ML/AI:** PyTorch · TensorFlow · Keras · CUDA · Hugging Face Transformers & Hub · Torchvision · timm · ConvNeXt · BERT · Sentence Transformers · Scikit-learn · Reinforcement Learning

**NLP/LLM:** LangChain · RAG Pipelines · Vector Databases (ChromaDB / Pinecone) · RAGAS Evaluation · Prompt Engineering

**MLOps:** W&B / MLflow · Evidently AI · Model Registry · Experiment Tracking · FastAPI · Docker · ECR · ECS Fargate · GitHub Actions (CI/CD) · Pytest · Ruff · Pyright · uv

**Data:** NumPy · Pandas · Feature Engineering · Data Preprocessing

**Web:** Django · Flask · React · REST APIs · PostgreSQL / SQLite

**Languages:** Python · SQL · JavaScript · C

**Tools:** Git · Linux / Bash · Jupyter Notebooks

---

### 🚀 Selected Projects

* **[Domain Intelligence Platform](https://github.com/ben-gid/domain_intelligence_platform)** *(in progress)* — End-to-end NLP system fine-tuning DistilBERT/DeBERTa on domain-specific classification via HuggingFace Trainer API, with a full MLOps pipeline (W&B tracking, versioned registry, Evidently drift detection, automated challenger/champion promotion) and a LangChain RAG layer over a domain corpus using sentence-transformers and ChromaDB. Evaluated with RAGAS across faithfulness, answer relevancy, and context precision. Deployed as dual FastAPI services (inference + RAG) on AWS ECS Fargate via ECR, with model CI/CD in GitHub Actions.

* **[Gravitational Lens Finding — ML4SCI DeepLense GSoC 2026](https://github.com/ben-gid/deeplense_tests)** — Achieved **0.9887 AUROC** on binary gravitational lens finding (16.6:1 class imbalance) with ConvNeXt-Tiny — within 0.006 of a purpose-built equivariant neural network (Parul et al., NeurIPS ML4PS 2024). Achieved **0.98 macro AUROC** on 3-class lensing substructure classification via two-phase EfficientNet-B0 fine-tuning with discriminative learning rates. Addressed severe class imbalance through WeightedRandomSampler and calibrated BCEWithLogitsLoss pos-weighting.

* **[Flower Classification API](https://github.com/ben-gid/flowers)** — Production-ready CV service achieving **>93% accuracy** on 102 flower classes via two-stage EfficientNet-B0 fine-tuning with differential learning rates (+30 points over a custom CNN trained from scratch). Served via FastAPI with dual model endpoints, HuggingFace Hub weight hosting, and a full CI pipeline: Ruff → Pyright → Pytest → Docker build.

* **[ML Fundamentals Library](https://github.com/ben-gid/ml_fundamentals)** — NumPy-only ML library built from scratch with manual backpropagation, covering Linear/Logistic Regression, K-Means, Decision Trees, and a multi-layer Neural Network. 100% Pytest coverage with a custom AST-based documentation generator.

* **[DQN for Autonomous Lunar Landing](https://github.com/ben-gid/LunarLander)** — Deep Q-Network agent in TensorFlow/Keras solving LunarLander-v3 (rolling average > 200). Includes Experience Replay, Target Networks with soft updates (τ=0.001), and `tf.function` graph-mode acceleration.

* **[AI Crossword Generator](https://github.com/ben-gid/Crossword)** — CSP solver generating dense crossword grids using backtracking search with AC-3 arc consistency (80%+ search space reduction), MRV, and LCV heuristics.

---

### 🧠 How I Work

* **Understand first:** I break systems apart mentally before touching code — knowing *why* something works matters as much as *that* it works.
* **Build to learn:** Small, practical experiments teach me more than tutorials.
* **Ship it tested:** CI pipelines, typed code, and reproducible setups are part of the work, not afterthoughts.
* **Iterate on results:** I benchmark, measure, and go again — 63% → 93% doesn't happen in one shot.

---

### 📫 Contact

* **Email:** [bgidanian@gmail.com](mailto:bgidanian@gmail.com)
* **LinkedIn:** [linkedin.com/in/benyamin-gidanian](https://www.linkedin.com/in/benyamin-gidanian-46305a364/)