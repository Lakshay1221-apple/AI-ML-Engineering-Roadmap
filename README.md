<div align="center">


<br/>

<img src="https://img.shields.io/badge/Duration-45%20Days-blueviolet?style=for-the-badge" />
<img src="https://img.shields.io/badge/Level-Beginner%20to%20Advanced-orange?style=for-the-badge" />
<img src="https://img.shields.io/badge/Python-3.10%2B-blue?style=for-the-badge&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/PyTorch%20%7C%20HuggingFace-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" />
<img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" />

<br/><br/>

# ML to LLM — 45-Day AI/ML Series

### A structured, beginner-to-advanced journey through Machine Learning,<br/>Deep Learning, LLMs, and Generative AI.

**Every concept explained. Every function justified. Every module ends with a real project.**

<br/>

[**Start Here →**](#getting-started) &nbsp;·&nbsp; [Roadmap](#series-roadmap) &nbsp;·&nbsp; [Projects](#mini-projects-summary) &nbsp;·&nbsp; [Resources](#resources) &nbsp;·&nbsp; [Contribute](#contributing)

</div>

---

## What is this?

Most learning resources make a choice you shouldn't have to live with:

> *"Learn theory for 3 weeks, then maybe touch code."*
> *"Jump straight into a project, copy-paste the parts you don't understand."*

This series does neither.

Every concept is taught in isolation first — then immediately applied to a real dataset. Every function is explained: not just *what* it does, but *why* it's used at that exact point in the pipeline. Every module ends with a mini project that forces you to combine everything you just learned.

The result: you finish this series with **8 working portfolio projects**, **100+ interview questions answered**, and a clear mental model of how every layer of the modern AI stack connects — from a pandas DataFrame all the way to a fine-tuned LLM serving real users.

---

## Who is this for?

| You are... | This series will... |
|---|---|
| A **complete beginner** to ML | Walk you from scratch — zero assumptions |
| A **Python developer** who hasn't touched ML | Give you the intuition behind the tools, not just the syntax |
| A **self-taught dev** trying to enter AI | Provide structured depth with interview prep built in |
| A **CS student** bridging theory to practice | Fill the "glue code" gap that textbooks skip |
| Someone who **finished a course but feels lost** | Bridge the gap between tutorial land and real project work |

> **Not designed for:** people who want to use AI tools without understanding what's under the hood, or people looking for a passive reading experience. Every module has code to write and tasks to complete.

---

## What makes this different?

**🎯 One dataset per module**  
You watch the same dataset get cleaned, explored, modelled, and evaluated over several days — so every new concept feels grounded in something familiar, not abstract.

**📖 Every step is justified**  
Not just `df.fillna(df.mean())` — but *why median here, not mean, and what breaks if you get it wrong*.

**🛠️ Mini project every 7–10 days**  
You get a working, explainable result before motivation has a chance to drop. Eight portfolio-worthy projects by the end.

**🎤 Interview questions per day**  
The repo doubles as exam prep. Every notebook ends with 3–5 questions you should be able to answer cold.

**✅ Reproducible environments**  
Every notebook runs top-to-bottom. No mystery "works on my machine" errors. CPU fallbacks provided for every GPU step.

---

## Series Roadmap

```
┌─────────────────────────────────────────────────────────────────────┐
│                                                                     │
│   PHASE 1 · FOUNDATIONS        PHASE 2 · CLASSICAL ML               │
│   Modules 1–4                  Modules 5–9                          │
│   ──────────────────────       ──────────────────────               │
│   Programming & Python     →   Core ML Algorithms              →    │
│   Math & Statistics            Evaluation & Pipelines               │
│   Data Engineering                                                  │
│                                                                     │
│                                         │                           │
│                                         ▼                           │
│                                                                     │
│   PHASE 3 · DEEP LEARNING      PHASE 4 · LLMs & GEN AI              │
│   Modules 10–16                Modules 17–21                        │
│   ──────────────────────       ──────────────────────               │
│   Neural Networks          ←   LLM Engineering                      │
│   CNNs & Vision                RAG Systems                          │
│   Transformers & NLP           Generative AI                        │
│                                RL & Alignment                       │
│                                                                     │
│                                         │                           │
│                                         ▼                           │
│                                                                     │
│   PHASE 5 · MLOps & CLOUD      PHASE 6 · CAPSTONE                   │
│   Modules 22–27                Modules 28–31                        │
│   ──────────────────────       ──────────────────────               │
│   Data Engineering         →   Paper Implementation                 │
│   Model Deployment             AI System Design                     │
│   Cloud & Scaling              Enterprise Capstone                  │
│   Monitoring & Drift           AGI & Frontier Research              │
│                                                                     │
└─────────────────────────────────────────────────────────────────────┘
```

> **Self-paced by design.** "45 days" is the structured sequence — not a countdown. Go at whatever speed lets you actually understand before moving on. See [How to Follow Along](#how-to-follow-along) for pacing suggestions.

---

## Getting Started

### Prerequisites

- Python 3.10 or higher
- Basic Python familiarity (functions, loops, lists) — Module 1 covers the rest
- A GPU helps for Phase 3+ but is **not required** — CPU fallbacks are provided everywhere

### Option 1 — Conda (recommended)

```bash
git clone https://github.com/yourusername/ml-to-llm-45days.git
cd ml-to-llm-45days

conda env create -f environment.yml
conda activate ml45
jupyter lab
```

### Option 2 — pip + virtualenv

```bash
git clone https://github.com/yourusername/ml-to-llm-45days.git
cd ml-to-llm-45days

python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate

pip install -r requirements.txt
jupyter lab
```

### Option 3 — Google Colab (no setup)

Every notebook has an **"Open in Colab"** badge at the top. Free T4 GPU included. No local installation needed.

### Verify your setup

```bash
python -c "import numpy, pandas, sklearn, torch; print('All systems go ✓')"
```

---

## Repository Structure

```
ml-to-llm-45days/
│
├── README.md                            ← You are here
├── requirements.txt                     ← All dependencies
├── environment.yml                      ← Conda environment
│
├── module-01-python-engineering/
│   ├── README.md                        ← Module overview, syllabus & interview questions
│   ├── 01-python-internals.ipynb
│   ├── 02-oop-and-design-patterns.ipynb
│   ├── 03-file-io-and-apis.ipynb
│   └── mini-project/
│       ├── README.md                    ← Problem statement & deliverables
│       └── notebook.ipynb
│
├── module-02-math-for-ai/
├── module-03-statistics-probability/
├── ...
├── module-17-llm-engineering-finetuning/
├── module-18-rag-ai-product-engineering/
├── ...
└── module-31-agi-frontier-models/
│
├── datasets/                            ← Shared datasets used across modules
│   ├── titanic.csv
│   ├── telco-churn.csv
│   └── imdb-reviews/
│
└── assets/                              ← Diagrams, roadmap images
    └── roadmap.png
```

Every module follows this consistent internal structure:

```
module-XX-topic-name/
├── README.md            ← Syllabus, concepts covered, interview questions
├── 01-concept-a.ipynb   ← One notebook per major concept
├── 02-concept-b.ipynb
├── 03-concept-c.ipynb
└── mini-project/
    ├── README.md         ← Problem statement, deliverables, grading rubric
    ├── notebook.ipynb    ← Fully worked solution
    └── dataset/          ← Module-specific data (if not in shared /datasets)
```

---

## Module Syllabus

> Modules are released progressively as they are completed. Star or watch the repo to get notified when new modules drop.

---

### 🧱 Phase 1 — Foundations (Modules 1–4)

#### Module 1 — Programming & Python Engineering
Core Python for AI/ML — the language fundamentals every practitioner needs before touching data.

`Python internals` · `OOP & design patterns` · `File I/O & APIs` · `Virtual environments` · `Git workflow`

---

#### Module 2 — Math for AI
The mathematical building blocks behind every algorithm in this series — explained visually, not as a proof dump.

`Linear algebra` · `Matrix operations` · `Calculus & gradients` · `Probability & Bayes` · `Statistics fundamentals`

---

#### Module 3 — Statistics & Probability for ML
Going deeper on the statistical thinking that separates guessing from knowing.

`Distributions` · `Hypothesis testing` · `Confidence intervals` · `Correlation vs causation` · `A/B testing basics`

---

#### Module 4 — Data Handling & Visualisation Engineering
The full data wrangling toolkit — from raw files to insight-ready DataFrames.

`NumPy` · `Pandas` · `Matplotlib & Seaborn` · `Data cleaning` · `EDA` · `Missing values` · `Outliers`

> 🛠️ **Mini Project:** Titanic Survival Analysis — cleaning, EDA, and a full preprocessing pipeline

---

### 🤖 Phase 2 — Classical ML (Modules 5–9)

#### Module 5 — ML From Scratch (Core Algorithms Implementation)
Understand algorithms by building them — not just calling `.fit()`.

`Linear regression from scratch` · `Gradient descent` · `Logistic regression` · `Decision trees` · `k-NN`

---

#### Module 6 — Supervised Learning (Regression + Classification Deep Dive)
Every major supervised algorithm, when to use each, and how to evaluate them correctly.

`Random Forest` · `XGBoost` · `SVMs` · `Naive Bayes` · `Precision / Recall / F1 / AUC` · `Cross-validation`

> 🛠️ **Mini Project:** Customer Churn Prediction — classification, evaluation metrics, sklearn Pipeline

---

#### Module 7 — Unsupervised Learning & Representation Learning
When you have data but no labels — finding hidden structure that's actually there.

`K-Means` · `DBSCAN` · `Hierarchical clustering` · `PCA` · `t-SNE` · `Autoencoders`

> 🛠️ **Mini Project:** Customer Segmentation — K-Means, PCA, RFM feature engineering

---

#### Module 8 — Model Evaluation, Tuning & ML Optimisation
Move beyond default hyperparameters and learn to systematically improve any model.

`GridSearchCV` · `RandomizedSearch` · `Optuna (Bayesian optimisation)` · `Bias-variance tradeoff` · `Calibration`

---

#### Module 9 — Feature Engineering & Real-World ML Pipelines
The step where domain knowledge becomes competitive advantage — and where most courses skip.

`Interaction features` · `Encoding strategies` · `Feature selection` · `sklearn Pipelines` · `ColumnTransformer` · `Data leakage`

---

### 🧠 Phase 3 — Deep Learning (Modules 10–16)

#### Module 10 — Neural Network Foundations
From a single perceptron to a working multi-layer network — built and understood from scratch.

`Perceptrons` · `Activation functions` · `Loss functions` · `Forward pass` · `Backpropagation` · `Gradient descent`

---

#### Module 11 — PyTorch Deep Learning
The practical toolkit for building, training, and debugging neural networks in PyTorch.

`Tensors & autograd` · `nn.Module` · `Training loops` · `DataLoader` · `GPU acceleration` · `Saving & loading models`

---

#### Module 12 — Advanced Deep Learning Optimisation
Making models train faster, more stably, and generalise better — the techniques that matter in practice.

`Dropout` · `Batch normalisation` · `LR schedulers` · `Gradient clipping` · `Mixed precision` · `Early stopping`

---

#### Module 13 — CNN & Vision Systems
Convolutional neural networks — the architecture that made computer vision work.

`Conv2D & pooling` · `Feature maps` · `CNN from scratch` · `Transfer learning (ResNet, EfficientNet)` · `Grad-CAM`

> 🛠️ **Mini Project:** Image Classifier on CIFAR-10 — CNN from scratch vs transfer learning, explainability with Grad-CAM

---

#### Module 14 — Advanced Computer Vision
Beyond classification — detection, segmentation, and modern vision architectures.

`Object detection (YOLO)` · `Semantic segmentation` · `Image augmentation` · `Vision Transformers (ViT)`

---

#### Module 15 — NLP Foundations (Classical + Embeddings)
Text as data — from bag-of-words to word vectors, with a real preprocessing pipeline.

`Tokenisation` · `TF-IDF` · `BoW` · `Word2Vec` · `GloVe` · `Text preprocessing pipelines`

---

#### Module 16 — Transformers Deep Dive
The architecture that changed everything — understood from first principles, not just called from a library.

`Attention mechanism` · `Scaled dot-product attention` · `Multi-head attention` · `Positional encoding` · `BERT vs GPT` · `HuggingFace Transformers`

> 🛠️ **Mini Project:** Sentiment Analysis on IMDb — fine-tuning DistilBERT end-to-end with HuggingFace Trainer

---

### 🚀 Phase 4 — LLMs & Generative AI (Modules 17–21)

#### Module 17 — LLM Engineering & Fine-Tuning
Working with large language models — from prompt engineering to a production-ready fine-tuned adapter.

`LLM landscape` · `Prompt engineering` · `Instruction tuning` · `LoRA & QLoRA` · `PEFT` · `SFTTrainer` · `Adapter merging`

> 🛠️ **Mini Project:** Fine-tune your own LLM with LoRA — custom instruction dataset, QLoRA, adapter export

---

#### Module 18 — RAG & AI Product Engineering
Give your LLM a knowledge base — build retrieval-augmented generation systems that actually work in production.

`Embeddings` · `Vector stores (Chroma, FAISS)` · `Chunking strategies` · `LangChain` · `LlamaIndex` · `Agentic RAG` · `RAGAS evaluation`

> 🛠️ **Mini Project:** RAG Chatbot over your own documents — Chroma, LangChain, evaluated with RAGAS

---

#### Module 19 — Generative AI Engineering
Beyond language — images, audio, and multimodal systems.

`Diffusion models` · `Stable Diffusion architecture` · `ControlNet` · `Vision-language models` · `Audio generation` · `GenAI product patterns`

---

#### Module 20 — Reinforcement Learning
Teaching agents to make decisions through reward — from grid worlds to LLM alignment techniques.

`MDPs & Bellman equations` · `Q-Learning` · `Policy gradient` · `PPO` · `RLHF` · `DPO`

---

#### Module 21 — Multimodal AI Systems
Models that see, read, and reason across modalities simultaneously.

`Vision-language models` · `CLIP` · `LLaVA` · `Multimodal RAG` · `Audio + vision fusion`

---

### ⚙️ Phase 5 — MLOps & Cloud (Modules 22–27)

#### Module 22 — Data Engineering & Big Data
Building the data infrastructure that production ML systems depend on.

`ETL pipelines` · `Apache Spark` · `Airflow` · `Data lakes` · `Feature stores` · `dbt`

---

#### Module 23 — Vector Databases & Embedding Systems
The infrastructure layer behind every modern search and RAG system.

`Qdrant` · `Weaviate` · `Pinecone` · `HNSW indexing` · `Embedding pipelines at scale`

---

#### Module 24 — MLOps Foundations
Reproducible, trackable, automated machine learning — the engineering discipline behind reliable systems.

`Experiment tracking (W&B, MLflow)` · `Model versioning` · `DVC` · `CI for ML` · `Data validation`

---

#### Module 25 — Model Deployment & Serving
From a notebook to a live endpoint that handles real traffic.

`FastAPI` · `Gradio & Streamlit` · `TorchServe` · `ONNX` · `Quantisation & pruning` · `Latency optimisation`

---

#### Module 26 — Cloud AI Engineering
Running ML workloads at scale on cloud infrastructure — the major platforms compared.

`AWS SageMaker` · `GCP Vertex AI` · `Azure ML` · `Serverless inference` · `Spot instance training`

---

#### Module 27 — Advanced MLOps & Scaling
Production-grade ML systems — monitoring, drift detection, and scaling strategies.

`Model monitoring` · `Data drift` · `A/B deployment` · `Shadow mode` · `Kubernetes for ML` · `Ray`

---

### 🎓 Phase 6 — Capstone (Modules 28–31)

#### Module 28 — Research Paper Implementation
Bridge the gap between published research and working code.

`Reading papers effectively` · `Implementing from scratch` · `Reproducing results` · `Ablation studies`

---

#### Module 29 — AI System Design & Architecture
Designing AI systems end-to-end — the skill that matters most in system design interviews.

`System design for ML` · `Scalability patterns` · `Trade-off analysis` · `Real-world case studies`

---

#### Module 30 — Enterprise AI Capstone
A complete, production-grade AI project from problem definition to deployed system.

`Problem framing` · `Architecture decisions` · `Full pipeline` · `Evaluation` · `Documentation` · `Demo`

> 🛠️ **Capstone Project:** Your choice of problem — data to deployed product, fully documented

---

#### Module 31 — AGI & Frontier Models
The current research frontier — what's happening in AI today and where it's heading.

`Scaling laws` · `Emergent capabilities` · `Constitutional AI` · `Agent frameworks` · `AI safety fundamentals`

---

## Mini Projects Summary

Eight portfolio-worthy projects, spread across the full 45-day journey:

| # | Module | Project | Dataset | Skills Demonstrated |
|---|---|---|---|---|
| 1 | Module 4 | **Titanic Survival Analysis** | Titanic | Cleaning, EDA, full preprocessing pipeline |
| 2 | Module 6 | **Customer Churn Prediction** | Telco Churn | Classification, evaluation metrics, sklearn Pipeline |
| 3 | Module 7 | **Customer Segmentation** | Online Retail | K-Means, PCA, RFM feature engineering |
| 4 | Module 13 | **Image Classifier** | CIFAR-10 | CNN from scratch vs transfer learning, Grad-CAM |
| 5 | Module 16 | **Sentiment Analysis** | IMDb Reviews | Fine-tuning DistilBERT, HuggingFace Trainer |
| 6 | Module 17 | **LLM Fine-Tuning** | Custom instruction set | LoRA, QLoRA, SFTTrainer, adapter merging |
| 7 | Module 18 | **RAG Chatbot** | Your own docs | Embeddings, Chroma, LangChain, RAGAS evaluation |
| 8 | Module 30 | **Enterprise AI Capstone** | Your choice | Full pipeline — data to deployed product |

---

## What You Will Be Able to Do

By the end of this series:

**Data & Classical ML**
- [ ] Build end-to-end ML pipelines from raw data to evaluated model
- [ ] Justify every preprocessing decision — not just copy-paste it
- [ ] Apply and compare 10+ classical ML algorithms on real datasets
- [ ] Detect and fix data leakage, class imbalance, and overfitting

**Deep Learning**
- [ ] Implement neural networks from scratch using PyTorch
- [ ] Build and fine-tune CNNs for computer vision tasks
- [ ] Understand the transformer architecture from attention mechanism to output token
- [ ] Train models that actually converge with proper regularisation

**LLMs & Modern AI**
- [ ] Fine-tune open-weight LLMs using LoRA and QLoRA on consumer hardware
- [ ] Build production RAG systems with vector search and LangChain
- [ ] Design and ship full AI-powered applications with FastAPI + Gradio
- [ ] Evaluate LLM systems using RAGAS and modern evaluation frameworks

**Engineering & Career**
- [ ] Track experiments, version models, and build reproducible pipelines
- [ ] Answer 100+ ML interview questions cold
- [ ] Maintain a GitHub portfolio of 8 working projects across all phases
- [ ] Read and implement AI research papers independently

---

## How to Follow Along

This is **self-paced**. There is no fixed schedule — go at whatever speed lets you actually understand and implement each module before moving on.

| Goal | Suggested Pace | Timeline |
|---|---|---|
| Deep understanding, job-ready portfolio | 1–2 modules per week | 4–6 months |
| Quick survey, going deeper elsewhere | 2–3 modules per week | 2–3 months |
| Full-time intensive sprint | 1 module per day | ~6 weeks |

**The only rule:** do not skip the practice tasks or mini projects. Reading notebooks without running the code will not get you anywhere. The understanding lives in the doing.

---

## Notebook Structure

Every concept notebook in this series follows this exact template:

```markdown
# [Topic Name]

## What is it?
Plain language definition. No jargon without immediate explanation.

## Why do we need it?
The problem this concept solves. What breaks if you skip it.

## Mathematical intuition
The core idea in math, explained visually where possible. No proof dumps.

## Code walkthrough
Fully annotated cells. Every line commented with *why*, not just *what*.

## Common mistakes
The top 3 errors beginners make here and how to avoid them.

## Practice task
One hands-on exercise to complete before moving to the next notebook.

## Interview questions
3–5 questions you should be able to answer after working through this notebook.
```

---

## Dependencies

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

**Phase 4–5 (LLMs & MLOps)**
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

## Resources

### Core Reading

| Resource | Type | Relevant Modules |
|---|---|---|
| [Hands-On ML with Scikit-Learn & TensorFlow](https://www.oreilly.com/library/view/hands-on-machine-learning/9781492032632/) | Book | Phases 1–3 |
| [Deep Learning with PyTorch](https://www.manning.com/books/deep-learning-with-pytorch) | Book | Phase 3 |
| [Attention Is All You Need](https://arxiv.org/abs/1706.03762) | Paper | Module 16 |
| [LoRA: Low-Rank Adaptation](https://arxiv.org/abs/2106.09685) | Paper | Module 17 |
| [QLoRA](https://arxiv.org/abs/2305.14314) | Paper | Module 17 |
| [RAGAS Evaluation Framework](https://arxiv.org/abs/2309.15217) | Paper | Module 18 |

### Free Courses

| Course | Platform | Relevant Modules |
|---|---|---|
| fast.ai Practical Deep Learning | fast.ai | Modules 10–14 |
| Andrej Karpathy's Neural Networks: Zero to Hero | YouTube | Modules 10–11 |
| HuggingFace NLP Course | huggingface.co | Modules 16–17 |
| LangChain Academy | LangChain | Module 18 |

### Tools & Platforms

| Tool | Purpose |
|---|---|
| [Weights & Biases](https://wandb.ai) | Experiment tracking |
| [HuggingFace Hub](https://huggingface.co) | Models and datasets |
| [Kaggle](https://kaggle.com) | Datasets and competitions |
| [Google Colab](https://colab.research.google.com) | Free GPU (T4) |
| [Lightning AI Studios](https://lightning.ai) | Free GPU for training |

---

## Contributing

Contributions are welcome — corrections, additional examples, better explanations, and translations.

**To contribute:**
1. Fork the repository
2. Create a branch: `git checkout -b fix/module-07-clustering-typo`
3. Make your changes
4. Open a pull request with a clear description of what you changed and why

**Please do not:**
- Add content that skips the notebook template structure
- Submit notebooks that don't run clean from top to bottom
- Add dependencies without updating `requirements.txt` and `environment.yml`

---

## Support This Series

If this series helps you:
- **⭐ Star the repo** — it helps others find it
- **Share it** with someone learning ML
- **Open an issue** if you find an error or unclear explanation

---

## License

MIT License — see [LICENSE](LICENSE) for details.  
Free to use, share, and adapt with attribution.

---

<div align="center">

**Built by [Lakshay](https://github.com/yourusername)**

*From ML to LLM — one module at a time.*

</div>
