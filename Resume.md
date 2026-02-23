# Benyamin Gidanian

Los Angeles, CA 90034  
(310) 613-3655  
bgidanian@gmail.com  
GitHub: https://github.com/ben-gid  
LinkedIn: https://linkedin.com/in/benyamin-gidanian-46305a364  

---

## Summary

Machine Learning Engineer with a strong foundation in computer science and applied AI, trained through Harvard’s CS50 suite and Stanford’s Machine Learning Specialization. Experienced in designing, training, and optimizing machine learning models across supervised learning, deep learning, and reinforcement learning domains.

Focused on building efficient, reproducible, and well-validated ML systems with an emphasis on algorithmic correctness, training stability, and performance optimization. Passionate about translating theoretical ML concepts into high-quality, production-ready implementations.

---

## Technical Skills

**Languages:** Python, SQL, JavaScript, Dart (Flutter), C  

**Machine Learning:** Supervised Learning (Regression, Classification), Unsupervised Learning, Recommender Systems, Reinforcement Learning, Neural Networks, Decision Trees, XGBoost  

**Deep Learning:** PyTorch, TensorFlow, Keras, Torchvision, BERT, Attention Mechanisms  

**Reinforcement Learning:** DQN, Experience Replay, Target Networks, Soft Updates  

**Data & Experimentation:** NumPy, Pandas, Feature Engineering, Data Preprocessing, Model Evaluation (Precision, Recall, F1-Score), Hyperparameter Tuning  

**Backend & Integration:** FastAPI, Django, Flask, RESTful APIs  

**Tools:** Docker, Git, GitHub Actions (CI/CD), Linux, Bash, Pytest, Jupyter Notebooks  

---

# Technical Projects

## ML Fundamentals Library  
*Python, NumPy, Matplotlib, Pytest*  
GitHub: https://github.com/ben-gid/ml_fundamentals  

- Designed and implemented a modular machine learning library from scratch using NumPy, developing 6+ core algorithms including Linear/Logistic Regression, K-Means, Decision Trees, and Neural Networks without high-level frameworks.  
- Built a custom deep learning engine with manual backpropagation, enabling transparent gradient flow and improved conceptual control over training dynamics.  
- Optimized numerical computations through vectorization, significantly improving runtime performance and computational efficiency.  
- Achieved 100% unit test coverage using Pytest and developed an AST-based documentation generator to enforce reproducibility and code clarity.  

---

## Flower Classification Inference Service  
*Python, PyTorch, FastAPI, Docker*  
GitHub: https://github.com/ben-gid/flowers  

- Designed and trained a custom Convolutional Neural Network (CNN) in PyTorch on the Oxford-102 dataset with structured training loops and learning rate scheduling.  
- Leveraged CUDA acceleration to improve training efficiency and reduce epoch runtime.  
- Developed a real-time inference service using FastAPI to deploy and validate model predictions under low-latency constraints.  
- Implemented automated dataset ingestion and validation using Torchvision to ensure clean, consistent training data.  
- Built a comprehensive test suite validating model lifecycle, input constraints, and inference stability.  

---

## Deep Q-Network (DQN) for Autonomous Lunar Landing  
*Reinforcement Learning, TensorFlow, Gymnasium, Python*  
GitHub: https://github.com/ben-gid/LunarLander  

- Implemented a Deep Q-Network (DQN) agent from scratch using TensorFlow/Keras to solve the LunarLander-v3 environment, achieving a solved threshold with a rolling average score above 200.  
- Engineered stability mechanisms including Experience Replay (deque buffer) and Target Networks with soft updates (τ=0.001) to reduce Q-value divergence and improve convergence stability.  
- Optimized training execution using tf.function for graph-mode acceleration, reducing per-episode training time.  

---

## Crossword Puzzle Generator (Constraint Satisfaction Solver)  
*Python, Search Optimization*  
GitHub: https://github.com/ben-gid/Crossword  

- Implemented a Constraint Satisfaction Problem (CSP) solver to generate dense crossword grids.  
- Optimized backtracking search using AC-3 arc consistency, reducing the search space by over 80%.  
- Integrated MRV and LCV heuristics to improve constraint propagation efficiency and solution speed.  

---

## Full-Stack Social Networking Platform  
*Django, React*  
GitHub: https://github.com/ben-gid/network  

- Designed a relational schema using Django ORM to manage complex user relationships.  
- Built RESTful APIs enabling asynchronous frontend interactions.  
- Optimized database queries using select_related and prefetch_related to improve performance.  

---

# Professional Experience

## Talmud Tutor (One-on-One Mentor)  
Mesivta Bircas Yitzchok | Sept 2023 – March 2025  

- Analyzed complex logical structures and formal arguments with precision.  
- Applied structured reasoning to identify edge cases and logical inconsistencies.  
- Developed individualized curricula to accelerate comprehension and retention.  
- Maintained consistent performance and reliability over a 1.5-year engagement.  

---

# Education & Certifications

## Machine Learning Specialization  
Stanford University & DeepLearning.AI (Coursera)  
- Supervised Learning, Neural Networks, Decision Trees, Unsupervised Learning, Recommender Systems  

## CS50 Computer Science Suite  
Harvard University (EdX)  
- CS50x: Computer Science (C, Python, SQL, Data Structures, Algorithms)  
- CS50p: Python (OOP, Unit Testing, Regular Expressions)  
- CS50ai: Artificial Intelligence (Search, Logic, Probability, Optimization)  
- CS50w: Web Programming (Django, React, CI/CD)  