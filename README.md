<div align="center">

<img src="https://img.shields.io/badge/Duration-45%20Days-blueviolet?style=for-the-badge" />
<img src="https://img.shields.io/badge/Level-Beginner%20to%20Advanced-orange?style=for-the-badge" />
<img src="https://img.shields.io/badge/Language-Python%203.10%2B-blue?style=for-the-badge&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/Framework-PyTorch%20%7C%20HuggingFace-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" />
<img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" />

# 🤖 ML to LLM — 45-Day AI/ML Series

**A structured, beginner-to-advanced journey through Machine Learning, Deep Learning, LLMs, and Generative AI.**  
Every concept explained. Every function justified. Every module ends with a real project.

[Getting Started](#-getting-started) · [Roadmap](#-series-roadmap) · [Projects](#-mini-projects) · [Resources](#-resources) · [Contributing](#-contributing)

</div>

---

## 📌 About This Series

This repository is a **complete self-contained learning path** for anyone who wants to go from zero knowledge to confidently building and deploying AI/ML systems.

Most tutorials either:
- Dump theory at you for weeks before you touch any code, or  
- Throw you into a project before you understand *why* any step exists

This series does neither. Every concept is taught in isolation first, then immediately applied to a real dataset. Every function is explained — not just *what* it does, but *why* it's used at that specific point in the pipeline. And every module ends with a mini project that forces you to combine everything you just learned.

### Who is this for?

| You are... | This series will... |
|---|---|
| A complete beginner to ML | Walk you from scratch — no assumptions |
| Someone who knows Python but not ML | Give you the theory and intuition behind the tools |
| A self-taught dev wanting to enter AI | Provide structured depth with interview prep built in |
| A CS student bridging theory to practice | Fill the "glue code" gap that textbooks skip |

### What makes this different?

- **One dataset per module** — you watch the same dataset get cleaned, explored, modeled, and evaluated over several days, so every new concept feels grounded
- **Every step is justified** — not just `df.fillna(df.mean())` but *why median and not mean here*
- **Mini project every 7–10 days** — you get a working result before motivation drops
- **Interview questions per day** — repo doubles as exam prep
- **Reproducible environments** — every notebook runs top to bottom, no mystery errors

---

## 🗂 Repository Structure

```
ml-to-llm-45days/
│
├── README.md                        ← You are here
├── requirements.txt                 ← All dependencies
├── environment.yml                  ← Conda environment
├── setup.py                         ← Optional package install
│
├── phase-1-classical-ml/            ← Days 01–14
│   ├── day-01-what-is-ml/
│   │   ├── README.md                ← Day-level notes
│   │   └── notebook.ipynb
│   ├── day-02-python-for-ml/
│   │   └── notebook.ipynb
│   ├── ...
│   └── day-14-mini-project-churn/
│       ├── README.md
│       ├── notebook.ipynb
│       └── dataset/
│
├── phase-2-unsupervised-ml/         ← Days 15–22
├── phase-3-deep-learning/           ← Days 23–32
├── phase-4-llm-finetuning/          ← Days 33–40
├── phase-5-genai-capstone/          ← Days 41–45
│
├── datasets/                        ← Shared datasets
│   ├── titanic.csv
│   ├── telco-churn.csv
│   └── imdb-sentiment/
│
└── assets/                          ← Images, diagrams
    └── roadmap.png
```

Each day folder follows this consistent structure:

```
day-XX-topic-name/
├── README.md          ← Concept notes, theory, interview questions
├── notebook.ipynb     ← Runnable code with inline explanations
└── practice.md        ← Practice task for the day
```

---

## ⚙️ Getting Started

### Prerequisites

- Python 3.10 or higher
- Basic Python familiarity (functions, loops, lists)
- A GPU is helpful for Phase 3+ but not required — CPU fallbacks are provided

### Installation

**Option 1 — Conda (recommended)**

```bash
git clone https://github.com/yourusername/ml-to-llm-45days.git
cd ml-to-llm-45days

conda env create -f environment.yml
conda activate ml45
jupyter lab
```

**Option 2 — pip + virtualenv**

```bash
git clone https://github.com/yourusername/ml-to-llm-45days.git
cd ml-to-llm-45days

python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate

pip install -r requirements.txt
jupyter lab
```

**Option 3 — Google Colab**  
Every notebook has a **"Open in Colab"** badge at the top. No local setup needed.

### Verify your setup

```bash
python -c "import numpy, pandas, sklearn, torch; print('All good ✓')"
```

---

## 🗺 Series Roadmap

```
Phase 1           Phase 2           Phase 3           Phase 4           Phase 5
Days 01–14        Days 15–22        Days 23–32        Days 33–40        Days 41–45
─────────────     ─────────────     ─────────────     ─────────────     ─────────────
Classical ML  →   Unsupervised  →   Deep Learning →   LLMs & PEFT   →   GenAI &
& Pipelines       & Advanced ML     & Transformers     & RAG             Capstone
```

---

## 📅 Day-by-Day Breakdown

---

### Phase 1 — Classical ML & Pipelines
> **Days 01–14 · Dataset: Titanic · Mini Project: Customer Churn Prediction**

The foundation phase. Every topic from data collection to model evaluation, taught on the same Titanic dataset so you can see the full pipeline emerge day by day.

---

#### Day 01 — What is AI / ML?

> *Set the stage before writing a single line of code.*

**Concepts covered:**
- The AI → ML → DL hierarchy — what each term actually means
- Supervised vs unsupervised vs reinforcement learning
- Where ML is used and where it isn't (and why that matters)
- The ML workflow overview: data → features → model → evaluate → deploy

**Why this day exists:**  
Most people jump into code before understanding the problem space. Day 1 gives you a mental map so every subsequent concept has a place to live.

**Interview questions:**
1. What is the difference between AI, ML, and Deep Learning?
2. Give three real-world examples each of supervised and unsupervised learning.
3. What is the general workflow of an ML project?

---

#### Day 02 — Python for ML

> *The three tools you will use every single day.*

**Concepts covered:**
- NumPy: arrays, vectorised operations, broadcasting
- Pandas: DataFrames, Series, `.loc` vs `.iloc`, groupby
- Matplotlib / Seaborn: line, scatter, histogram, heatmap

**Why NumPy over plain Python lists?**  
Vectorised operations run in C under the hood — a 10,000-element operation is 50–100× faster than a Python loop. This is not optional knowledge; it directly affects model training time.

**Interview questions:**
1. What is broadcasting in NumPy?
2. What is the difference between `.loc` and `.iloc` in Pandas?
3. When would you use `groupby` over a manual loop?

---

#### Day 03 — Data Collection & Types

> *What does real-world data actually look like before you clean it?*

**Concepts covered:**
- Structured vs unstructured vs semi-structured data
- Common sources: CSV, JSON, SQL databases, APIs, web scraping
- Loading datasets with Pandas — `read_csv`, `read_json`, `read_sql`
- First look at a dataset: `.head()`, `.info()`, `.describe()`, `.shape`

**Dataset introduced:** Titanic (`titanic.csv`) — this dataset will be used through Day 9.

**Interview questions:**
1. What is the difference between structured and unstructured data?
2. How do you handle a dataset that comes from an API vs a CSV file?

---

#### Day 04 — Data Cleaning

> *The step nobody shows you but everyone does.*

**Concepts covered:**
- What "dirty data" looks like: duplicates, wrong data types, inconsistent formatting
- Detecting and dropping duplicates with `.duplicated()` and `.drop_duplicates()`
- Fixing data types: `pd.to_datetime()`, `.astype()`
- Standardising string columns: `.str.lower()`, `.str.strip()`

**Key insight:**  
Garbage in → garbage out. A model trained on dirty data will confidently produce wrong predictions. Cleaning is not preprocessing — it is a prerequisite to preprocessing.

**Interview questions:**
1. How do you detect and handle duplicate rows in Pandas?
2. What does `.astype()` do and when would you use it?
3. What is the difference between data cleaning and data preprocessing?

---

#### Day 05 — Missing Values

> *Not all missing data is equal — the strategy depends on why it's missing.*

**Concepts covered:**
- MCAR (Missing Completely at Random), MAR, MNAR — the three types and why they matter
- Visualising missingness: `missingno` library, heatmaps
- Imputation strategies:
  - Mean imputation (continuous, no outliers)
  - Median imputation (continuous, with outliers)
  - Mode imputation (categorical)
  - KNN imputer (preserves relationships between features)
- When to drop rows vs columns

**Why median over mean?**  
Mean is pulled by outliers. If `Age` has a genuine missing value and also contains some ages of 95+, mean imputation inflates the fill value. Median is robust to this. The choice of imputation strategy is a modeling decision, not a default.

**Interview questions:**
1. What is the difference between MCAR, MAR, and MNAR?
2. When would you use KNN imputation over simple mean imputation?
3. What is the risk of dropping rows with missing values?

---

#### Day 06 — Outliers

> *Detecting extreme values and deciding what to do with them.*

**Concepts covered:**
- What is an outlier — and is it always wrong?
- IQR method: lower fence = Q1 − 1.5×IQR, upper fence = Q3 + 1.5×IQR
- Z-score method: flag values beyond ±3 standard deviations
- Box plots and scatter plots for visual detection
- Three options: remove, cap (winsorization), or keep with justification

**Key insight:**  
An outlier is not automatically an error. A person who is 210 cm tall is a genuine outlier in height data — removing them would harm your model if height is a real predictor. Always ask *is this an error or an extreme real value?* before removing.

**Interview questions:**
1. What is the IQR method for detecting outliers?
2. When would you keep an outlier rather than remove it?
3. What is winsorization?

---

#### Day 07 — Encoding & Feature Scaling

> *Converting categories and numbers into a form every ML algorithm can use.*

**Concepts covered:**
- Why ML algorithms cannot work with raw strings
- Label encoding vs one-hot encoding — when to use each
- `LabelEncoder`, `OrdinalEncoder`, `OneHotEncoder` from scikit-learn
- StandardScaler (zero mean, unit variance) vs MinMaxScaler (0–1 range)
- **Critical rule: always fit on training data only, then transform both train and test**

**Why do we scale after splitting?**  
If you scale the entire dataset before splitting, information from the test set leaks into the scaler's parameters (mean and std). This gives you artificially optimistic evaluation results — your model appears to generalise better than it actually does.

**Interview questions:**
1. What is the difference between label encoding and one-hot encoding?
2. Why must you fit the scaler on training data only?
3. When would you use StandardScaler vs MinMaxScaler?

---

#### Day 08 — EDA & Visualisation

> *Understand your data before you model it.*

**Concepts covered:**
- Univariate analysis: distributions, skewness, kurtosis
- Bivariate analysis: scatter plots, correlation, cross-tabulation
- Correlation heatmaps with `seaborn.heatmap()`
- The difference between correlation and causation
- Using EDA to generate feature engineering hypotheses

**Interview questions:**
1. What does a correlation coefficient of 0.9 mean?
2. Why is it dangerous to assume correlation implies causation?
3. How does EDA inform feature selection?

---

#### Day 09 — 🏗 Mini Project: Titanic Survival Analysis

> *Apply everything from Days 3–8 on one dataset, end to end.*

**Project goal:** Build a complete data analysis and cleaning pipeline on the Titanic dataset. No modeling yet — the deliverable is a clean, well-documented notebook that could be handed to a colleague.

**What you build:**
1. Load and inspect the raw dataset
2. Identify and document all data quality issues
3. Apply cleaning, imputation, encoding, and scaling
4. EDA: which features correlate with survival?
5. Write a one-page summary of findings with charts

**What you must document:** Every single decision — why median for Age, why one-hot for Embarked, why drop Cabin. The reasoning is the deliverable, not just the code.

---

#### Day 10 — Train/Test Split & Cross-Validation

> *The single most important rule in machine learning.*

**Concepts covered:**
- The hold-out split: `train_test_split()` and the `random_state` parameter
- Why shuffling matters (and when it doesn't — time series)
- K-fold cross-validation: the idea and `KFold`, `StratifiedKFold`
- What data leakage is and why it silently ruins models

**Interview questions:**
1. What is stratified k-fold and when do you need it?
2. What is data leakage? Give a concrete example.
3. Why does the test set need to be held out until the very end?

---

#### Day 11 — Linear & Logistic Regression

> *The baselines you always beat first.*

**Concepts covered:**
- Linear regression: OLS, the normal equation, gradient descent intuition
- Logistic regression: the sigmoid function, decision boundary, log-loss
- Implementing both from scratch (numpy) and with scikit-learn
- Interpreting coefficients

**Interview questions:**
1. What is the difference between linear and logistic regression?
2. Why do we use log-loss for classification and not MSE?
3. What does a coefficient of 2.4 mean in a logistic regression model?

---

#### Day 12 — Decision Trees & Ensemble Methods

> *Where most beginners get their first real wins.*

**Concepts covered:**
- Decision tree: Gini impurity vs entropy, recursive splitting
- Overfitting in trees and how `max_depth` controls it
- Bagging and Random Forest: why averaging reduces variance
- Gradient Boosting (XGBoost intro): boosting intuition
- The bias-variance tradeoff explained visually

**Interview questions:**
1. What is the difference between bagging and boosting?
2. Why does a Random Forest generalise better than a single decision tree?
3. Explain the bias-variance tradeoff in plain language.

---

#### Day 13 — Model Evaluation

> *Accuracy is not a metric. It's a trap.*

**Concepts covered:**
- Confusion matrix: TP, TN, FP, FN
- Precision, recall, F1-score — when each matters
- ROC curve and AUC — how to read and interpret them
- The precision-recall tradeoff
- When accuracy is misleading (imbalanced datasets)

**Key insight:**  
If 95% of your dataset is class 0, a model that predicts 0 for everything achieves 95% accuracy and is completely useless. Accuracy without context is meaningless on imbalanced data.

**Interview questions:**
1. When would you optimise for recall over precision?
2. What does an AUC of 0.5 mean?
3. How do you handle class imbalance at evaluation time?

---

#### Day 14 — 🏗 Mini Project: Customer Churn Prediction

> *End-to-end classification on the Telco Customer Churn dataset.*

**Project goal:** Predict whether a telecom customer will churn. Full pipeline from raw CSV to evaluated model.

**What you build:**
1. Load Telco churn dataset
2. Full cleaning and preprocessing pipeline
3. Train Logistic Regression and Random Forest
4. Evaluate both with precision, recall, F1, AUC
5. Interpret: which features drive churn most?
6. Write a business-readable summary: *"Customers who X are Y% more likely to churn"*

---

### Phase 2 — Unsupervised & Advanced ML
> **Days 15–22 · Dataset: Online Retail · Mini Project: Customer Segmentation**

---

#### Day 15 — K-Means Clustering

> *Finding hidden structure when you have no labels.*

**Concepts covered:**
- The K-Means algorithm: initialisation, assignment, update
- Choosing K: the elbow method and silhouette score
- K-Means++ for better initialisation
- Limitations of K-Means (spherical clusters, sensitivity to outliers)

**Interview questions:**
1. How does K-Means initialisation affect the result?
2. What is the silhouette score and what does a value near 1 mean?
3. When would K-Means fail?

---

#### Day 16 — Dimensionality Reduction (PCA & t-SNE)

> *Fewer features, more signal.*

**Concepts covered:**
- The curse of dimensionality
- PCA: principal components, explained variance ratio, choosing n_components
- t-SNE: when PCA isn't enough, perplexity parameter
- Visualising high-dimensional data in 2D

**Interview questions:**
1. What does "explained variance ratio" mean in PCA?
2. Why is t-SNE non-deterministic?
3. Can you use PCA output as features for a classifier? What are the tradeoffs?

---

#### Day 17 — Support Vector Machines

> *Maximum margin classifiers and the kernel trick.*

**Concepts covered:**
- The hyperplane and margin maximisation
- Hard vs soft margin (the C parameter)
- The kernel trick: RBF, polynomial
- When SVMs outperform tree-based models

**Interview questions:**
1. What is the kernel trick and why is it useful?
2. What does the C parameter control in an SVM?
3. When would you choose an SVM over a Random Forest?

---

#### Day 18 — Feature Engineering

> *The step where domain knowledge becomes competitive advantage.*

**Concepts covered:**
- Creating interaction features
- Polynomial features with `PolynomialFeatures`
- Decomposing datetime columns (hour, day of week, is_weekend)
- Binning continuous features
- Target encoding (and why you must do it inside cross-validation)

**Interview questions:**
1. What is target encoding and why is it prone to leakage?
2. Give an example of a feature interaction that could improve a model.
3. Why is feature engineering often more valuable than model selection?

---

#### Day 19 — Hyperparameter Tuning

> *Systematically improving your model — not just guessing.*

**Concepts covered:**
- Grid search vs random search: tradeoffs
- `GridSearchCV` and `RandomizedSearchCV`
- Bayesian optimisation intro (Optuna)
- The risk of overfitting during tuning — why you need a held-out test set even after CV

**Interview questions:**
1. What is the difference between a parameter and a hyperparameter?
2. Why does random search often outperform grid search?
3. What is the danger of tuning hyperparameters on the test set?

---

#### Day 20 — Pipelines & Production Readiness

> *Package your work so it can actually be deployed.*

**Concepts covered:**
- `sklearn.pipeline.Pipeline`: chaining preprocessors and models
- `ColumnTransformer`: applying different transformations to different columns
- Saving models with `joblib` and `pickle`
- Reproducibility: `random_state`, seeds, environment files

**Key insight:**  
A Pipeline is not a convenience — it prevents leakage. When you wrap your scaler and model in a Pipeline, `fit_transform` on training data and `transform` on test data happen automatically in the right order, every time.

**Interview questions:**
1. What problem does `sklearn.Pipeline` solve?
2. What is `ColumnTransformer` used for?
3. How do you ensure a model is reproducible?

---

#### Day 21 — 🏗 Mini Project: Customer Segmentation

> *Cluster customers and give each segment a business label.*

**Project goal:** Use K-Means + PCA on the Online Retail dataset to identify customer segments based on RFM (Recency, Frequency, Monetary) features.

**What you build:**
1. Feature engineering: compute R, F, M per customer
2. Scale features
3. K-Means with elbow + silhouette analysis
4. Reduce to 2D with PCA and visualise segments
5. Label each cluster with a business interpretation ("High-value dormant", "New active", etc.)

---

#### Day 22 — Recap & Classical ML Interview Prep

> *Consolidate everything before moving to Deep Learning.*

**What this day covers:**
- Top 25 classical ML interview questions (answered in the notebook)
- Common pipeline mistakes and how to catch them
- What a strong classical ML portfolio looks like
- Checklist: are you ready for Phase 3?

---

### Phase 3 — Deep Learning & Transformers
> **Days 23–32 · Tools: PyTorch · Mini Projects: Image Classifier, Sentiment Analysis**

---

#### Day 23 — Neural Network Foundations

> *From a single perceptron to a multi-layer network.*

**Concepts covered:**
- The perceptron: weights, bias, activation
- Multi-layer networks: hidden layers and capacity
- Activation functions: ReLU, Sigmoid, Tanh — when to use which
- Loss functions: MSE for regression, CrossEntropy for classification
- Forward pass step by step

**Interview questions:**
1. Why does a neural network with no activation functions reduce to linear regression?
2. What is the vanishing gradient problem and which activations cause it?
3. What is the purpose of bias in a neuron?

---

#### Day 24 — Backpropagation & PyTorch Basics

> *How neural networks actually learn — and the tools that automate it.*

**Concepts covered:**
- Backpropagation: chain rule, computing gradients layer by layer
- PyTorch autograd: `requires_grad`, `.backward()`, `.grad`
- Tensors: creation, operations, GPU transfer
- Writing a training loop from scratch: forward → loss → backward → step

**Interview questions:**
1. What does `optimizer.zero_grad()` do and why is it necessary?
2. Explain backpropagation to someone without a math background.
3. What is the difference between `torch.no_grad()` and `model.eval()`?

---

#### Day 25 — CNNs for Computer Vision

> *Why convolutions beat fully connected layers for images.*

**Concepts covered:**
- The convolution operation: filters, stride, padding
- Max pooling: spatial downsampling
- Feature map intuition: early layers detect edges, deep layers detect objects
- Building a CNN from scratch in PyTorch
- Training on CIFAR-10

**Interview questions:**
1. What is the receptive field of a convolutional layer?
2. Why is weight sharing in CNNs computationally efficient?
3. What does max pooling do and what information does it discard?

---

#### Day 26 — Transfer Learning

> *Don't train from scratch when someone already did the hard work.*

**Concepts covered:**
- Pretrained models: ResNet, EfficientNet, VGG
- Feature extraction vs fine-tuning
- When to freeze layers and when to unfreeze them
- `torchvision.models` and `model.parameters()`

**Key insight:**  
A ResNet-50 trained on ImageNet has already learned to detect edges, textures, shapes, and semantic objects. These features transfer — a model fine-tuned on 500 medical images outperforms a model trained from scratch on 50,000 of them.

**Interview questions:**
1. What is the difference between feature extraction and fine-tuning?
2. Why do you freeze early layers during fine-tuning?
3. When does transfer learning not work?

---

#### Day 27 — 🏗 Mini Project: Image Classifier

> *CIFAR-10 — custom CNN vs pretrained model.*

**What you build:**
1. Custom 4-layer CNN trained from scratch on CIFAR-10
2. Fine-tuned EfficientNet-B0 on the same task
3. Head-to-head comparison: accuracy, training time, parameter count
4. Grad-CAM visualisation: what does the model actually look at?

---

#### Day 28 — RNNs & LSTMs

> *Sequence modelling before transformers took over.*

**Concepts covered:**
- The recurrence equation: hidden state over time
- The vanishing gradient problem in RNNs
- LSTM gates: forget, input, output — what each controls
- When LSTMs are still the right choice (small datasets, long sequences)

**Interview questions:**
1. What problem do LSTMs solve that vanilla RNNs cannot?
2. Explain the forget gate in plain language.
3. Why did transformers largely replace LSTMs?

---

#### Day 29 — Attention Mechanism

> *The key idea behind every modern language model.*

**Concepts covered:**
- The intuition: which words should I look at to understand this word?
- Query, Key, Value: the three matrices and what they represent
- Scaled dot-product attention: the formula and why we scale
- Multi-head attention: multiple attention perspectives in parallel
- Attention visualisation

**Interview questions:**
1. What is the Query-Key-Value framework in attention?
2. Why do we divide by √d_k in scaled dot-product attention?
3. What does multi-head attention allow a model to learn that single-head cannot?

---

#### Day 30 — Transformer Architecture

> *"Attention Is All You Need" — what it actually means.*

**Concepts covered:**
- Encoder and decoder stacks
- Positional encoding: why and how
- Layer normalisation vs batch normalisation
- The full forward pass through a transformer block
- BERT (encoder-only) vs GPT (decoder-only) vs T5 (encoder-decoder)

**Interview questions:**
1. Why is positional encoding necessary in a transformer?
2. What is the difference between BERT and GPT architecturally?
3. What does the encoder do vs the decoder in a seq2seq transformer?

---

#### Day 31 — Training Tips & Regularisation

> *Make your models actually converge reliably.*

**Concepts covered:**
- Dropout: what it does, when to use it, and at what rate
- Batch normalisation: why it stabilises training
- Learning rate schedulers: cosine annealing, warmup, ReduceLROnPlateau
- Gradient clipping: preventing exploding gradients in deep networks
- Mixed precision training with `torch.cuda.amp`

**Interview questions:**
1. What does dropout do during training vs inference?
2. Why does learning rate warmup help transformer training?
3. What is gradient clipping and when is it necessary?

---

#### Day 32 — 🏗 Mini Project: Sentiment Analysis with Transformers

> *Fine-tune a small transformer on IMDb reviews.*

**What you build:**
1. Load IMDb dataset via HuggingFace Datasets
2. Tokenise with `DistilBERT` tokenizer
3. Fine-tune `distilbert-base-uncased` with HuggingFace Trainer
4. Evaluate: precision, recall, F1
5. Error analysis: which reviews does the model get wrong and why?

---

### Phase 4 — LLMs, Fine-Tuning & RAG
> **Days 33–40 · Tools: HuggingFace, PEFT, LangChain · Mini Project: RAG Chatbot**

---

#### Day 33 — The LLM Landscape

> *What exists, how it's different, and why it matters.*

**Concepts covered:**
- The model families: GPT, LLaMA, Mistral, Gemma, Phi
- Closed-weight (GPT-4, Claude) vs open-weight (LLaMA 3, Mistral)
- Context window, tokens, and why token count matters for cost
- Benchmarks: MMLU, HumanEval, MT-Bench — what they measure
- Responsible use: model cards, bias, hallucination

**Interview questions:**
1. What is the difference between a closed-weight and an open-weight model?
2. What is a context window and why does it limit LLM applications?
3. What is hallucination in LLMs and why does it happen?

---

#### Day 34 — Prompt Engineering

> *The fastest way to improve LLM output — no training required.*

**Concepts covered:**
- Zero-shot, one-shot, few-shot prompting
- Chain-of-thought (CoT) prompting
- System prompts and persona setting
- Structured output prompting (JSON, XML)
- Common failure modes: prompt injection, instruction following failures

**Interview questions:**
1. What is chain-of-thought prompting and why does it improve reasoning?
2. What is the difference between a system prompt and a user prompt?
3. How do you prompt an LLM to return structured JSON reliably?

---

#### Day 35 — Fine-Tuning Foundations

> *When prompting is not enough.*

**Concepts covered:**
- Why fine-tune: domain adaptation, consistent format, capability injection
- Full fine-tuning vs parameter-efficient fine-tuning (PEFT)
- Instruction tuning: Alpaca format, ShareGPT format
- Dataset preparation: prompt templates, tokenisation, padding strategy
- Catastrophic forgetting: what it is and how to mitigate it

**Interview questions:**
1. When would you fine-tune a model instead of prompting it?
2. What is instruction tuning?
3. What is catastrophic forgetting and how do you avoid it?

---

#### Day 36 — LoRA & QLoRA Deep Dive

> *The practical path to fine-tuning on consumer hardware.*

**Concepts covered:**
- The intrinsic dimensionality hypothesis: why most weight updates live in a low-rank subspace
- LoRA: decompose ΔW into A × B where rank(A,B) ≪ d
- Rank (r), alpha (α), and target modules — what each controls
- QLoRA's three innovations:
  - 4-bit NormalFloat (NF4): optimal quantisation for normally distributed weights
  - Double quantisation: quantising the quantisation constants
  - Paged optimisers: offloading optimizer states to CPU RAM to prevent OOM
- Adapter merging: combining LoRA weights back into the base model

**Key insight:**  
LoRA doesn't change what the model knows — it changes what it does with what it knows. The base model's 7B parameters stay frozen. Only ~0.1–1% of additional parameters are trained, making fine-tuning a 7B model possible on a single 16GB GPU.

**Interview questions:**
1. What is the mathematical idea behind LoRA?
2. What does the rank parameter r control in LoRA?
3. What are the three innovations in QLoRA that make it memory-efficient?

---

#### Day 37 — HuggingFace Fine-Tuning Lab

> *Code-first: build a working fine-tuning pipeline.*

**Concepts covered:**
- Full training script with `peft`, `bitsandbytes`, `trl`
- `BitsAndBytesConfig` for 4-bit loading
- `LoraConfig`: r, alpha, dropout, target_modules
- `SFTTrainer`: dataset, tokenisation, training arguments
- Saving adapters and merging back into base model
- Evaluating before and after fine-tuning

**What you build:**  
A complete, runnable fine-tuning script for TinyLlama-1.1B (or Llama 3.2 3B) on a custom instruction dataset.

**Interview questions:**
1. What does `target_modules` control in a LoRA config?
2. What is the difference between saving a LoRA adapter and saving a merged model?
3. What is `SFTTrainer` and how does it differ from HuggingFace's standard `Trainer`?

---

#### Day 38 — RAG Fundamentals

> *Give your LLM a knowledge base without retraining it.*

**Concepts covered:**
- The retrieval-augmented generation architecture
- Text embeddings: what they represent and how they capture meaning
- Chunking strategies: fixed-size, sentence-level, semantic
- Vector stores: Chroma, FAISS — indexing and querying
- The retrieval pipeline: query → embed → search → retrieve → prompt → generate

**Why RAG instead of fine-tuning?**  
Fine-tuning teaches a model to *behave* differently. RAG gives it access to *information* it didn't have. For knowledge that changes (company docs, product specs, recent events), RAG is almost always the right choice.

**Interview questions:**
1. What is the difference between RAG and fine-tuning?
2. What is chunking and why does chunk size matter?
3. How does a vector similarity search work?

---

#### Day 39 — Advanced RAG & Evaluation

> *Beyond naive retrieval — making RAG actually reliable.*

**Concepts covered:**
- Retrieval failures: why naive RAG hallucinates
- Hybrid search: dense + sparse (BM25) retrieval
- Reranking: cross-encoders for better relevance
- LangChain retrieval chain: end to end
- RAGAS evaluation framework: faithfulness, answer relevance, context precision

**Interview questions:**
1. What is the difference between dense and sparse retrieval?
2. What does the RAGAS faithfulness metric measure?
3. What is a reranker and when would you add one to a RAG pipeline?

---

#### Day 40 — 🏗 Mini Project: RAG Chatbot

> *Build a Q&A bot over your own document collection.*

**What you build:**
1. Ingest a set of PDFs or markdown files
2. Chunk, embed (sentence-transformers), and store in Chroma
3. Query pipeline with LangChain: retrieve → augment → generate
4. Evaluate with RAGAS: faithfulness and answer relevance
5. Gradio interface for live querying

---

### Phase 5 — Generative AI & Capstone
> **Days 41–45 · Final Project: Your Choice**

---

#### Day 41 — Generative AI Landscape

> *Beyond language — images, audio, multimodal.*

**Concepts covered:**
- Diffusion models: the forward and reverse process, DDPM intuition
- Stable Diffusion architecture: VAE + UNet + CLIP text encoder
- Vision-language models: CLIP, LLaVA, GPT-4V
- Audio generation: Whisper, MusicGen
- The state of multimodal AI as of 2024–2025

**Interview questions:**
1. What is the core idea behind diffusion models?
2. What does CLIP do and why is it used in Stable Diffusion?
3. What is the difference between a text-to-image model and a vision-language model?

---

#### Day 42 — Building & Deploying AI Products

> *Your model is useless until someone can use it.*

**Concepts covered:**
- FastAPI: wrapping a model as a REST endpoint
- Gradio and Streamlit: rapid demo UIs
- Dockerising an ML app: `Dockerfile`, `docker-compose`
- Environment management: `requirements.txt`, `environment.yml`
- Logging, monitoring, and versioning basics

**Interview questions:**
1. How do you serve a PyTorch model as a REST API?
2. What is a Dockerfile and why do you need one for ML deployment?
3. What is model versioning and why does it matter?

---

#### Day 43 — Evaluation & Responsible AI

> *How do you know your model is actually good — and safe?*

**Concepts covered:**
- LLM evaluation: BLEU, ROUGE, BERTScore, LLM-as-judge
- Hallucination detection techniques
- Bias in ML models: types, sources, measurement
- Safety considerations: refusals, jailbreaks, output filtering
- Model cards: what they are and why you should write one

**Interview questions:**
1. What is the difference between BLEU and BERTScore?
2. How do you measure bias in a classification model?
3. What is a model card and what should it contain?

---

#### Day 44–45 — 🏗 Capstone Project

> *Build, document, and present a complete AI/ML system.*

**Goal:** Design and build a full-stack AI project of your choosing. By this point you have the skills to tackle any of the following — or propose your own.

**Project options:**

| Project | Stack | Core Skills |
|---|---|---|
| AI Career Copilot | TinyLlama + LoRA + Gradio | Fine-tuning, PEFT, deployment |
| Document Intelligence System | LangChain + Chroma + FastAPI | RAG, embeddings, API serving |
| Real-time Sentiment Dashboard | DistilBERT + Streamlit | Transformers, classification, UI |
| Medical Image Classifier | ResNet + Docker | CNN, transfer learning, deployment |
| Generative Story Writer | Mistral 7B + LoRA | Instruction tuning, generation |

**Deliverables:**

- [ ] Working end-to-end system (data → model → interface)
- [ ] Clean, documented codebase
- [ ] `README.md` for the project (use this repo's structure as a template)
- [ ] 3-minute demo video or Loom recording
- [ ] One-page write-up: problem, approach, results, what you'd improve

---

## 🏗 Mini Projects Summary

| # | Day | Project | Dataset | Skills |
|---|---|---|---|---|
| 1 | Day 09 | Titanic Survival Analysis | Titanic | Cleaning, EDA, visualisation |
| 2 | Day 14 | Customer Churn Prediction | Telco Churn | Classification, evaluation, pipelines |
| 3 | Day 21 | Customer Segmentation | Online Retail | K-Means, PCA, RFM features |
| 4 | Day 27 | Image Classifier | CIFAR-10 | CNN, transfer learning, Grad-CAM |
| 5 | Day 32 | Sentiment Analysis | IMDb Reviews | Transformers, HuggingFace Trainer |
| 6 | Day 40 | RAG Chatbot | Custom docs | Embeddings, vector store, LangChain |
| 7 | Day 44–45 | Capstone | Your choice | Everything |

---

## 📦 Dependencies

Full environment files are in the repo root. Key packages by phase:

**Phase 1–2 (Classical ML)**
```
numpy>=1.24
pandas>=2.0
scikit-learn>=1.3
matplotlib>=3.7
seaborn>=0.12
missingno>=0.5
jupyter>=1.0
```

**Phase 3 (Deep Learning)**
```
torch>=2.1
torchvision>=0.16
torchaudio>=2.1
```

**Phase 4–5 (LLMs)**
```
transformers>=4.40
datasets>=2.18
peft>=0.10
trl>=0.8
bitsandbytes>=0.43
langchain>=0.1
langchain-community>=0.0.20
chromadb>=0.4
sentence-transformers>=2.6
gradio>=4.0
fastapi>=0.110
```

---

## 📚 Resources

### Core Reading

| Resource | Type | Covers |
|---|---|---|
| [Hands-On ML with Scikit-Learn & TensorFlow](https://www.oreilly.com/library/view/hands-on-machine-learning/9781492032632/) | Book | Phase 1–3 |
| [Deep Learning with PyTorch](https://www.manning.com/books/deep-learning-with-pytorch) | Book | Phase 3 |
| [Attention Is All You Need](https://arxiv.org/abs/1706.03762) | Paper | Day 30 |
| [LoRA: Low-Rank Adaptation](https://arxiv.org/abs/2106.09685) | Paper | Day 36 |
| [QLoRA paper](https://arxiv.org/abs/2305.14314) | Paper | Day 36 |
| [RAGAS evaluation framework](https://arxiv.org/abs/2309.15217) | Paper | Day 39 |

### Free Courses

| Course | Platform | Covers |
|---|---|---|
| fast.ai Practical Deep Learning | fast.ai | Phase 3 |
| Andrej Karpathy's Neural Networks: Zero to Hero | YouTube | Phase 3 |
| HuggingFace NLP Course | huggingface.co | Phase 4 |
| LangChain Academy | LangChain | Day 38–39 |

### Tools & Platforms

| Tool | Purpose |
|---|---|
| [Weights & Biases](https://wandb.ai) | Experiment tracking |
| [HuggingFace Hub](https://huggingface.co) | Models and datasets |
| [Kaggle](https://kaggle.com) | Datasets and competitions |
| [Google Colab](https://colab.research.google.com) | Free GPU (T4) |
| [Lightning AI Studios](https://lightning.ai) | Free GPU for training |

---

## 📐 Day Template

Every day in this series follows this exact structure:

```markdown
# Day XX — Topic Name

## What is it?
Plain language definition. No jargon without immediate explanation.

## Why do we need it?
The problem this concept solves. What breaks if you skip it.

## Mathematical intuition
The core math, explained visually where possible. No proof dumps.

## Code walkthrough
Fully annotated notebook. Every line has a comment explaining *why*, not just *what*.

## Common mistakes
The top 3 errors beginners make on this topic and how to avoid them.

## Practice task
One hands-on exercise to complete before Day N+1.

## Interview questions
3–5 questions you should be able to answer after today.
```

---

## 🤝 Contributing

Contributions are welcome — corrections, additional examples, better explanations, and translations.

**To contribute:**
1. Fork the repository
2. Create a branch: `git checkout -b fix/day-07-scaling-typo`
3. Make your changes
4. Open a pull request with a clear description

**Please do not:**
- Add content that skips the day template structure
- Submit notebooks that don't run top-to-bottom
- Add dependencies without updating `requirements.txt`

---

## ⭐ Support This Series

If this series helps you, consider:
- Starring the repo (it helps others find it)
- Sharing it with someone learning ML
- Opening an issue if you find an error or unclear explanation

---

## 📄 License

This project is licensed under the **MIT License** — see [LICENSE](LICENSE) for details.  
You are free to use, share, and adapt this material with attribution.

---

<div align="center">

**Built by [Lakshay](https://github.com/Lakshay1221-apple)**  
*From ML to LLM — one day at a time.*

</div>