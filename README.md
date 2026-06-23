<div align="center">

<img src="https://img.shields.io/badge/Duration-45%20Days-blueviolet?style=for-the-badge" />
<img src="https://img.shields.io/badge/Level-Beginner%20to%20Advanced-orange?style=for-the-badge" />
<img src="https://img.shields.io/badge/Language-Python%203.10%2B-blue?style=for-the-badge&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/Framework-PyTorch%20%7C%20HuggingFace-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" />
<img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" />

# ML to LLM — 45-Day AI/ML Series

**A structured, beginner-to-advanced journey through Machine Learning, Deep Learning, LLMs, and Generative AI.**  
Every concept explained. Every function justified. Every module ends with a real project.

[Getting Started](#getting-started) · [Roadmap](#series-roadmap) · [Projects](#mini-projects-summary) · [Resources](#resources) · [Contributing](#contributing)

</div>

---

## About This Series

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

## Repository Structure

```
ml-to-llm-45days/
│
├── README.md                            ← You are here
├── requirements.txt                     ← All dependencies
├── environment.yml                      ← Conda environment
│
├── module-01-python-engineering/
│   ├── README.md                        ← Module overview & syllabus
│   ├── 01-python-internals.ipynb
│   ├── 02-oop-and-design-patterns.ipynb
│   ├── 03-file-io-and-apis.ipynb
│   └── mini-project/
│       ├── README.md
│       └── notebook.ipynb
│
├── module-02-math-for-ai/
├── module-03-statistics-probability/
├── module-04-data-handling-visualisation/
├── module-05-ml-from-scratch/
│   ...
├── module-17-llm-engineering-finetuning/
├── module-18-rag-ai-product-engineering/
│   ...
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

Each module follows this consistent internal structure:

```
module-XX-topic-name/
├── README.md           ← Syllabus, concepts covered, interview questions
├── 01-concept-a.ipynb  ← One notebook per major concept
├── 02-concept-b.ipynb
├── 03-concept-c.ipynb
└── mini-project/
    ├── README.md        ← Problem statement, deliverables
    ├── notebook.ipynb   ← Fully worked solution
    └── dataset/         ← Data if not in shared /datasets
```

---

## Getting Started

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

## Series Roadmap

```
MODULE 1–4               MODULE 5–9               MODULE 10–16
──────────────────       ──────────────────       ──────────────────
Programming &        →   Core ML              →   Deep Learning,
Math Foundations         Algorithms               CNNs & NLP
                                                        │
                                                        ▼
MODULE 28–31             MODULE 22–27             MODULE 17–21
──────────────────       ──────────────────       ──────────────────
Research &           ←   MLOps, Cloud         ←   LLMs, RAG &
Capstone                 & Deployment             Generative AI
```

Content is uploaded module by module as it is completed. Each module folder appears in this repo as it goes live — star or watch the repo to get notified.

---

## Module Syllabus

> Each module is a self-contained unit with notebooks, concept notes, and a mini project. Modules are released progressively — check back regularly or watch the repo.

---

### Foundation Modules

#### Module 1 — Programming & Python Engineering
Core Python for AI/ML — the language fundamentals every practitioner needs before touching data.

`Python internals` · `OOP & design patterns` · `File I/O & APIs` · `Virtual environments` · `Git workflow`

---

#### Module 2 — Math for AI
The mathematical building blocks behind every algorithm in this series.

`Linear algebra` · `Matrix operations` · `Calculus & gradients` · `Probability & Bayes` · `Statistics fundamentals`

---

#### Module 3 — Statistics & Probability for ML
Going deeper on the statistical thinking that separates guessing from knowing.

`Distributions` · `Hypothesis testing` · `Confidence intervals` · `Correlation vs causation` · `A/B testing basics`

---

#### Module 4 — Data Handling & Visualisation Engineering
The full data wrangling toolkit — from raw files to insight-ready DataFrames.

`NumPy` · `Pandas` · `Matplotlib & Seaborn` · `Data cleaning` · `EDA` · `Missing values` · `Outliers`

---

### Classical ML Modules

#### Module 5 — ML From Scratch (Core Algorithms Implementation)
Understand algorithms by building them — not just calling `.fit()`.

`Linear regression from scratch` · `Gradient descent` · `Logistic regression` · `Decision trees` · `k-NN`

---

#### Module 6 — Supervised Learning (Regression + Classification Deep)
Every major supervised algorithm, when to use each, and how to evaluate them correctly.

`Random Forest` · `XGBoost` · `SVMs` · `Naive Bayes` · `Precision / Recall / F1 / AUC` · `Cross-validation`

---

#### Module 7 — Unsupervised Learning & Representation Learning
When you have data but no labels — finding hidden structure.

`K-Means` · `DBSCAN` · `Hierarchical clustering` · `PCA` · `t-SNE` · `Autoencoders`

---

#### Module 8 — Model Evaluation, Tuning & ML Optimisation
Move beyond default hyperparameters and learn to systematically improve any model.

`GridSearchCV` · `RandomizedSearch` · `Optuna (Bayesian)` · `Bias-variance tradeoff` · `Calibration`

---

#### Module 9 — Feature Engineering & Real-World ML Pipelines
The step where domain knowledge becomes competitive advantage — and where most courses skip.

`Interaction features` · `Encoding strategies` · `Feature selection` · `sklearn Pipelines` · `ColumnTransformer` · `Data leakage`

---

### Deep Learning Modules

#### Module 10 — Neural Network Foundations
From a single perceptron to a working multi-layer network — built and understood from scratch.

`Perceptrons` · `Activation functions` · `Loss functions` · `Forward pass` · `Backpropagation` · `Gradient descent`

---

#### Module 11 — PyTorch Deep Learning
The practical toolkit for building, training, and debugging neural networks.

`Tensors & autograd` · `nn.Module` · `Training loops` · `DataLoader` · `GPU acceleration` · `Saving & loading models`

---

#### Module 12 — Advanced Deep Learning Optimisation
Making models train faster, more stably, and generalise better.

`Dropout` · `Batch normalisation` · `LR schedulers` · `Gradient clipping` · `Mixed precision` · `Early stopping`

---

#### Module 13 — CNN & Vision Systems
Convolutional neural networks — the architecture that made computer vision work.

`Conv2D & pooling` · `Feature maps` · `CNN from scratch` · `Transfer learning (ResNet, EfficientNet)` · `Grad-CAM`

---

#### Module 14 — Advanced Computer Vision
Beyond classification — detection, segmentation, and modern vision architectures.

`Object detection (YOLO)` · `Semantic segmentation` · `Image augmentation` · `Vision Transformers (ViT)`

---

### NLP & Transformers Modules

#### Module 15 — NLP Foundations (Classical + Embeddings)
Text as data — from bag-of-words to word vectors.

`Tokenisation` · `TF-IDF` · `BoW` · `Word2Vec` · `GloVe` · `Text preprocessing pipelines`

---

#### Module 16 — Transformers Deep Dive
The architecture that changed everything — understood from first principles.

`Attention mechanism` · `Scaled dot-product attention` · `Multi-head attention` · `Positional encoding` · `BERT vs GPT` · `HuggingFace Transformers`

---

### LLM & Generative AI Modules

#### Module 17 — LLM Engineering & Fine-Tuning
Working with large language models — from prompt to production fine-tuned adapter.

`LLM landscape` · `Prompt engineering` · `Instruction tuning` · `LoRA & QLoRA` · `PEFT` · `SFTTrainer` · `Adapter merging`

---

#### Module 18 — RAG & AI Product Engineering
Give your LLM a knowledge base — build retrieval-augmented generation systems that actually work.

`Embeddings` · `Vector stores (Chroma, FAISS)` · `Chunking strategies` · `LangChain` · `LlamaIndex` · `Agentic RAG` · `RAGAS evaluation`

---

#### Module 19 — Generative AI Engineering
Beyond language — images, audio, and multimodal systems.

`Diffusion models` · `Stable Diffusion architecture` · `ControlNet` · `Vision-language models` · `Audio generation` · `GenAI product patterns`

---

#### Module 20 — Reinforcement Learning
Teaching agents to make decisions through reward — from grid worlds to LLM alignment.

`MDPs & Bellman equations` · `Q-Learning` · `Policy gradient` · `PPO` · `RLHF` · `DPO`

---

#### Module 21 — Multimodal AI Systems
Models that see, read, and reason across modalities simultaneously.

`Vision-language models` · `CLIP` · `LLaVA` · `Multimodal RAG` · `Audio + vision fusion`

---

### Engineering & MLOps Modules

#### Module 22 — Data Engineering & Big Data
Building the data infrastructure that production ML systems depend on.

`ETL pipelines` · `Apache Spark` · `Airflow` · `Data lakes` · `Feature stores` · `dbt`

---

#### Module 23 — Vector Databases & Embedding Systems
The infrastructure layer behind every modern search and RAG system.

`Qdrant` · `Weaviate` · `Pinecone` · `HNSW indexing` · `Embedding pipelines at scale`

---

#### Module 24 — MLOps Foundations
Reproducible, trackable, automated machine learning — the engineering discipline.

`Experiment tracking (W&B, MLflow)` · `Model versioning` · `DVC` · `CI for ML` · `Data validation`

---

#### Module 25 — Model Deployment & Serving
From a notebook to a live endpoint that handles real traffic.

`FastAPI` · `Gradio & Streamlit` · `TorchServe` · `ONNX` · `Quantisation & pruning` · `Latency optimisation`

---

#### Module 26 — Cloud AI Engineering
Running ML workloads at scale on cloud infrastructure.

`AWS SageMaker` · `GCP Vertex AI` · `Azure ML` · `Serverless inference` · `Spot instance training`

---

#### Module 27 — Advanced MLOps & Scaling
Production-grade ML systems — monitoring, drift detection, and scaling.

`Model monitoring` · `Data drift` · `A/B deployment` · `Shadow mode` · `Kubernetes for ML` · `Ray`

---

### Capstone Modules

#### Module 28 — Research Paper Implementation
Bridge the gap between published research and working code.

`Reading papers effectively` · `Implementing from scratch` · `Reproducing results` · `Ablation studies`

---

#### Module 29 — AI System Design & Architecture
Designing AI systems end-to-end — the skill that matters in system design interviews.

`System design for ML` · `Scalability patterns` · `Trade-off analysis` · `Real-world case studies`

---

#### Module 30 — Enterprise AI Capstone
A complete, production-grade AI project from problem definition to deployed system.

`Problem framing` · `Architecture decisions` · `Full pipeline` · `Evaluation` · `Documentation` · `Demo`

---

#### Module 31 — AGI & Frontier Models Understanding
The current frontier — what's happening in AI research and where it's heading.

`Scaling laws` · `Emergent capabilities` · `Constitutional AI` · `Agent frameworks` · `AI safety fundamentals`

---

## What You Will Learn

By the end of this series, you will be able to:

**Data & Classical ML**
- [ ] Build end-to-end ML pipelines from raw data to evaluated model
- [ ] Justify every preprocessing decision — not just copy-paste it
- [ ] Apply and compare 10+ classical ML algorithms on real datasets
- [ ] Detect and fix data leakage, class imbalance, and overfitting

**Deep Learning**
- [ ] Implement neural networks from scratch using PyTorch
- [ ] Build and fine-tune CNNs for computer vision tasks
- [ ] Understand the transformer architecture from attention to output
- [ ] Train models that actually converge with proper regularisation

**LLMs & Modern AI**
- [ ] Fine-tune open-weight LLMs using LoRA and QLoRA on consumer hardware
- [ ] Build production RAG systems with vector search and LangChain
- [ ] Design and ship full AI-powered applications with FastAPI + Gradio
- [ ] Evaluate LLM systems with RAGAS and other modern frameworks

**Engineering & Career**
- [ ] Track experiments, version models, and build reproducible pipelines
- [ ] Answer 100+ ML interview questions that come up in technical rounds
- [ ] Maintain a GitHub portfolio of 7 working projects across all phases
- [ ] Read and implement AI research papers independently

---

## Who Should Follow This Series?

This series is designed to work across different starting points. Find yourself below:

**Perfect fit:**

| Profile | Why this works for you |
|---|---|
| **CS / engineering student** wanting to enter AI/ML | Structured depth that goes beyond what courses cover, with interview prep built in |
| **Self-taught developer** with Python experience | Closes the gap between knowing syntax and knowing *how ML systems actually work* |
| **Complete beginner** to both Python and ML | Everything is explained from scratch — no assumed knowledge, ever |
| **Developer pivoting to AI** from another stack | Practical, engineering-first approach — you'll build things, not just read theory |
| **Someone who took a course but feels lost in practice** | Bridges the gap between tutorials and the "glue code" that real projects need |

**You may need to supplement if:**
- You are already working as an ML engineer and want cutting-edge research depth — pair this with papers and arXiv
- You want a university-level mathematical treatment — pair with a linear algebra or probability textbook
- You need certification — this repo does not issue certificates, but the portfolio you build is more valuable

**Not designed for:**
- People who want to use AI tools (ChatGPT, Midjourney) without understanding what's under the hood
- People looking for a passive learning experience — every module has code to write and questions to answer

---

## How to Follow Along

This is a **self-paced** series. There is no fixed schedule — go at whatever speed lets you actually understand and implement each module before moving on.

**Suggested pace for different goals:**

| Goal | Suggested pace | Timeline |
|---|---|---|
| Deep understanding, job-ready portfolio | 1–2 modules per week | 4–6 months |
| Quick survey before going deeper elsewhere | 2–3 modules per week | 2–3 months |
| Intensive sprint (full-time study) | 1 module per day | ~6 weeks |

**The only rule:** do not skip the practice tasks or mini projects. Reading the notebooks without running the code will not get you anywhere. The understanding lives in the doing.

---

## Mini Projects Summary

Every module ends with a mini project. These are the highlights — the ones that produce something portfolio-worthy.

| # | Module | Project | Dataset | Skills demonstrated |
|---|---|---|---|---|
| 1 | Module 4 | Titanic Survival Analysis | Titanic | Cleaning, EDA, full preprocessing pipeline |
| 2 | Module 6 | Customer Churn Prediction | Telco Churn | Classification, evaluation metrics, sklearn Pipeline |
| 3 | Module 7 | Customer Segmentation | Online Retail | K-Means, PCA, RFM feature engineering |
| 4 | Module 13 | Image Classifier | CIFAR-10 | CNN from scratch vs transfer learning, Grad-CAM |
| 5 | Module 16 | Sentiment Analysis | IMDb Reviews | Fine-tuning DistilBERT, HuggingFace Trainer |
| 6 | Module 17 | LLM Fine-Tuning | Custom instruction set | LoRA, QLoRA, SFTTrainer, adapter merging |
| 7 | Module 18 | RAG Chatbot | Your own docs | Embeddings, Chroma, LangChain, RAGAS evaluation |
| 8 | Module 30 | Enterprise AI Capstone | Your choice | Full pipeline — data to deployed product |

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

## Resources

### Core Reading

| Resource | Type | Covers |
|---|---|---|
| [Hands-On ML with Scikit-Learn & TensorFlow](https://www.oreilly.com/library/view/hands-on-machine-learning/9781492032632/) | Book | Phase 1–3 |
| [Deep Learning with PyTorch](https://www.manning.com/books/deep-learning-with-pytorch) | Book | Phase 3 |
| [Attention Is All You Need](https://arxiv.org/abs/1706.03762) | Paper | Module 16 |
| [LoRA: Low-Rank Adaptation](https://arxiv.org/abs/2106.09685) | Paper | Module 17 |
| [QLoRA paper](https://arxiv.org/abs/2305.14314) | Paper | Module 17 |
| [RAGAS evaluation framework](https://arxiv.org/abs/2309.15217) | Paper | Module 18 |

### Free Courses

| Course | Platform | Covers |
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

## Notebook Template

Every concept notebook in this series follows this exact structure:

```markdown
# [Topic Name]

## What is it?
Plain language definition. No jargon without immediate explanation.

## Why do we need it?
The problem this concept solves. What breaks if you skip it.

## Mathematical intuition
The core idea in math, explained visually where possible. No proof dumps.

## Code walkthrough
Fully annotated cells. Every line has a comment explaining *why*, not just *what*.

## Common mistakes
The top 3 errors beginners make here and how to avoid them.

## Practice task
One hands-on exercise to complete before moving to the next notebook.

## Interview questions
3–5 questions you should be able to answer after working through this notebook.
```

---

## Contributing

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

## Support This Series

If this series helps you, consider:
- Starring the repo (it helps others find it)
- Sharing it with someone learning ML
- Opening an issue if you find an error or unclear explanation

---

## License

This project is licensed under the **MIT License** — see [LICENSE](LICENSE) for details.  
You are free to use, share, and adapt this material with attribution.

---

<div align="center">

**Built by [Lakshay](https://github.com/yourusername)**  
*From ML to LLM — one day at a time.*

</div>
