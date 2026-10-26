# Hi — I'm Benyamin Gidanian 👋

Applied ML/AI engineer in Los Angeles building end-to-end systems from raw data to deployed, tested inference services. I built my foundation through Harvard's CS50 and Stanford's Machine Learning Specialization, and I'm currently expanding into **NLP, LLMs, RAG, and MLOps** — shipping real projects at each step.

---

### 🔭 What I'm Working On

* **[Recipe Genome](https://github.com/ben-gid/recipe-genome)** — a RAG system with hybrid retrieval (BM25 + vector) over **522,517 recipes** in Weaviate, embedded with BAAI/bge-small-en-v1.5 through a GPU-backed sidecar so index-time and query-time vectors come from the same model. I audited the dataset and blanked ~196k copies of one boilerplate description so template text can't pull unrelated recipes together in embedding space. I also caught a silent failure where a capitalization mismatch left all 522k objects stored with no vectors. Next comes a retrieval eval harness (recall@10, MRR); I won't add a reranker until it shows the current setup falls short.

---

### 🛠️ Tech Stack

**ML/AI:** PyTorch · PyTorch Lightning · TensorFlow · Keras · CUDA · Hugging Face Transformers & Hub · Torchvision · timm · ConvNeXt · BERT · Sentence Transformers · Scikit-learn · Reinforcement Learning

**NLP/LLM:** LangChain · RAG Pipelines · Vector Databases (ChromaDB / Pinecone) · RAGAS Evaluation · Prompt Engineering

**MLOps:** W&B / MLflow · Evidently AI · Model Registry · Experiment Tracking · FastAPI · Docker · AWS (ECR · ECS Fargate · SSM Parameter Store) · Cloudflare · GitHub Actions (CI/CD) · Pytest · Ruff · Pyright · uv

**Data:** NumPy · Pandas · Feature Engineering · Data Preprocessing

**Web & Mobile:** Django · Flask · React · htmx · Alpine.js · REST APIs · PostgreSQL / SQLite · Flutter / Dart · Riverpod · Supabase

**Agentic Development:** Claude Code · Claude API · MCP

**Languages:** Python · SQL · JavaScript · C

**Tools:** Git · Linux / Bash · Jupyter Notebooks

---

### 🚀 Selected Projects

* **[PII Redaction API](https://github.com/ben-gid/pii_redaction)** — Fine-tuned three DeBERTa-v3 models (base/small/xsmall) on 27 PII entity types, achieving up to **0.9557 macro F1**. Deployed as a FastAPI service on **AWS ECS Fargate** with a custom domain, Cloudflare TLS, and a full GitHub Actions CI/CD pipeline (lint → type-check → test → build → deploy) triggered on every push. [Live demo](https://pii-redaction.bengid.dev/demo) · Models on [HuggingFace Hub](https://huggingface.co/bengid).

* **[Gravitational Lens Finding — ML4SCI DeepLense GSoC 2026](https://github.com/ben-gid/deeplense_tests)** — Achieved **0.9887 AUROC** on binary gravitational lens finding (16.6:1 class imbalance) with ConvNeXt-Tiny — within 0.006 of a purpose-built equivariant neural network (Parul et al., NeurIPS ML4PS 2024). Achieved **0.98 macro AUROC** on 3-class lensing substructure classification via two-phase EfficientNet-B0 fine-tuning with discriminative learning rates. Addressed severe class imbalance through WeightedRandomSampler and calibrated BCEWithLogitsLoss pos-weighting.

* **[Flower Classification API](https://github.com/ben-gid/flowers)** — PyTorch Lightning pipeline across 11 backbones tracked in MLflow (71 runs) on 102 flower classes; best model (**ViT-B/16**) reached **0.9837 accuracy / 0.9722 macro-F1**, with **ConvNeXt-Tiny** (0.9821 / 0.9694, a third of the weights) as the serving default. Found and fixed a data-leakage bug that had silently inflated every run's validation/test accuracy to ~1.0, re-evaluated both published models on genuinely held-out data, and added a regression test so it can't come back. Restructured into a v2 FastAPI service (`core`/`routers`/`utils`, `AppState` singleton, HuggingFace Hub weight loading) with a full CI pipeline: Ruff → Pyright → Pytest → Docker build.

* **[ML Fundamentals Library](https://github.com/ben-gid/ml_fundamentals)** — NumPy-only ML library built from scratch with manual backpropagation, covering Linear/Logistic Regression, K-Means, Decision Trees, and a multi-layer Neural Network. 100% Pytest coverage with a custom AST-based documentation generator.

* **[DQN for Autonomous Lunar Landing](https://github.com/ben-gid/LunarLander)** — Deep Q-Network agent in TensorFlow/Keras solving LunarLander-v3 (rolling average > 200). Includes Experience Replay, Target Networks with soft updates (τ=0.001), and `tf.function` graph-mode acceleration.

* **[AI Crossword Generator](https://github.com/ben-gid/Crossword)** — CSP solver generating dense crossword grids using backtracking search with AC-3 arc consistency (80%+ search space reduction), MRV, and LCV heuristics.

---

### 🤖 Agent-Built Applications

Built by directing **Claude Code**. I set the specs, architecture, invariants, and test requirements, and I reviewed and verified each change. Claude wrote the code.

* **Hybete** *(private)* — Hybrid running and lifting app for iOS and Android (Flutter · FastAPI · Supabase · Claude API · MCP · Google Cloud Run). It handles GPS run tracking, gym logging, and multi-week training plans, with a local-first store and optional Supabase sync isolated per user by row-level security. An AI coach (Claude Sonnet on Cloud Run) uses a read-and-propose tool layer, prompt caching, a per-user monthly spending cap, and RevenueCat subscription gating. The model never writes directly: its proposals land in an inbox where the user accepts or dismisses them. An MCP server secured with OAuth 2.1 lets users connect their own AI assistant. The project has **170+ tests**.

* **Invoicer** *(private)* — Multi-tenant B2B invoicing and inventory SaaS for small wholesalers (Django · PostgreSQL · htmx · Alpine.js · WeasyPrint · Playwright). It covers the full buy-and-sell loop: purchase orders, vendor bills, quotes, sales orders with backorders, invoices, credit notes, split payments, and AR/AP aging. Inventory uses FIFO costing on an append-only stock ledger with row locking, and voids and returns replay the original stock movements. I shaped the requirements by recovering a 1990s desktop ERP and six years of a real wholesaler's data (186k documents). The project has **327 tests**, including Playwright browser tests.

* **[Mise](https://github.com/ben-gid/mise)** — Schema-validated recipe app (Flutter · JSON Schema). It stores LLM-generated recipes as JSON validated against a JSON Schema before parsing. The import prompt embeds the live schema, so model output can't drift from what the validator accepts.

* **[Baker's Calculator](https://github.com/ben-gid/Baker-s-Calculator)** — Bread calculator (Flutter · Dart · Riverpod) rewritten around a pure-Dart domain layer. It handles baker's percentages, inverse flour solving for sourdough, scaling, and backward-scheduled bake timelines. Every output of my original hand-built version is kept as a golden regression test.

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