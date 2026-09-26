# ICML Research Paper Topic Modelling

A natural language processing project that applies Latent Dirichlet Allocation (LDA) topic modelling to research papers from the International Conference on Machine Learning (ICML).

## Project Overview

This project explores the underlying thematic structure of ICML research papers using Natural Language Processing (NLP) and unsupervised topic modelling.

The analysis processes research paper titles and abstracts, applies text preprocessing, constructs a Bag-of-Words representation, trains multiple LDA models, and evaluates different topic configurations using coherence scores.

The final model is also explored using interactive topic visualisation and topic trends over time.

---

## Objectives

The project aims to:

* Clean and prepare a collection of research paper abstracts and titles.
* Apply NLP preprocessing techniques to research text.
* Convert processed documents into a Bag-of-Words representation.
* Apply Latent Dirichlet Allocation for topic discovery.
* Evaluate different numbers of topics using coherence scores.
* Identify representative terms associated with each discovered topic.
* Visualise topic distributions and topic trends across publication years.

---

## Dataset

The dataset contains ICML research papers spanning **1987–2016**.

After preprocessing and duplicate removal, the dataset contained:

```text
6,560 papers
7 columns
```

The analysis uses textual information from the papers, particularly the title and abstract fields, together with publication year information.

> **Dataset note:** The original dataset is not included in this repository unless redistribution rights permit it.

---

## NLP Pipeline

The text processing workflow includes:

```text
Research Paper Data
        │
        ▼
Data Cleaning
        │
        ├── Handle missing titles
        ├── Handle missing abstracts
        ├── Remove incomplete records
        └── Remove duplicate titles
        │
        ▼
Text Preprocessing
        │
        ├── Tokenisation
        ├── Stop-word removal
        ├── Text normalisation
        └── Lemmatization
        │
        ▼
Bag-of-Words Representation
        │
        ▼
LDA Topic Modelling
        │
        ▼
Coherence Evaluation
        │
        ▼
Final Topic Model
        │
        ├── Topic interpretation
        ├── Topic visualisation
        └── Yearly topic trends
```

---

## Topic Modelling

### Latent Dirichlet Allocation

Latent Dirichlet Allocation (LDA) was used to identify groups of words that frequently occur together across research papers.

Multiple models were trained using different numbers of topics, ranging from **2 to 10 topics**.

The models were evaluated using a coherence score to assess the semantic consistency of the discovered topics.

---

## Topic Number Evaluation

The following coherence scores were obtained:

| Number of Topics | Coherence Score |
| ---------------: | --------------: |
|                2 |          0.6069 |
|                3 |          0.6138 |
|                4 |          0.6061 |
|                5 |      **0.6314** |
|                6 |          0.6023 |
|                7 |          0.5799 |
|                8 |          0.5382 |
|                9 |          0.5837 |
|               10 |          0.5422 |

The notebook selected **5 topics** for the final LDA model based on the evaluated coherence scores.

---

## Discovered Topics

The final model identified five topic groups based on their highest-weighted terms.

### Topic 0

Representative terms included:

```text
model, learning, inference, problem,
graph, method, algorithm, set
```

### Topic 1

Representative terms included:

```text
function, learning, bound, problem,
distribution, loss, kernel, algorithm
```

### Topic 2

Representative terms included:

```text
image, network, feature, learning,
object, training, task, deep
```

### Topic 3

Representative terms included:

```text
problem, matrix, method, algorithm,
optimization, analysis, sparse, gradient
```

### Topic 4

Representative terms included:

```text
network, neural, dynamic, neuron,
system, model, process, time
```

These topic descriptions are based on the highest-weighted terms produced by the final LDA model rather than manually assigned research categories.

---

## Visualisation

The project uses `pyLDAvis` to support interactive exploration of the discovered topics.

The notebook also examines how the relative presence of the identified topics changes across publication years.

This provides an additional temporal perspective on the research themes represented in the dataset.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* NLTK
* Gensim
* pyLDAvis
* Jupyter Notebook

---

## Project Structure

```text
icml-topic-modelling/
│
├── icml_topic_modelling.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/YOUR-USERNAME/icml-topic-modelling.git
cd icml-topic-modelling
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
icml_topic_modelling.ipynb
```

---

## Reproducibility

To reproduce the analysis:

1. Obtain the ICML article dataset used in the notebook.
2. Place the dataset in the expected project location.
3. Update the dataset path if necessary.
4. Install the required dependencies.
5. Run the notebook cells sequentially.

The notebook downloads the required NLTK resources used for text preprocessing.

---

## Key Skills Demonstrated

This project demonstrates practical experience with:

* Natural Language Processing
* Text preprocessing
* Tokenisation
* Stop-word removal
* Lemmatization
* Bag-of-Words modelling
* Latent Dirichlet Allocation
* Topic coherence evaluation
* Unsupervised machine learning
* Data visualisation
* Temporal topic analysis
* Python-based data analysis

---

## Author

**Nonhle Mnqayi**

ICT Graduate | Cybersecurity Honours Student
LinkedIn: `https://www.linkedin.com/in/nonhle-okuhle-973581274/`
