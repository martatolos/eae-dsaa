# EAE Data Science Labs

This repository contains several labs for the Data Science Course at EAE Business School. The labs are designed to help students understand and apply various data science techniques and tools.

## How to Use

You can add each notebook in Google Colab or in your local environment.

### Run in Google Colab

Each notebook contains a link to open it in Google Colab. Click on the link to open the notebook in a new tab.

### Run in Local Environment

#### Prerequisites

The following is required to run the notebooks in your local environment:

- [Git](https://git-scm.com/downloads)
- [Python 3.10 or higher](https://www.python.org/downloads)
- [Jupyter Notebook](https://jupyter.org/install)
- [uv](https://docs.astral.sh/uv/getting-started/installation/) (Optional but recommended)

#### Clone the Repository

First clone the repository to your local machine:

```bash
git clone https://github.com/martatolos/eae-dsaa-2025.git
```

#### Install dependencies

There are 3 ways to install the dependencies:

##### Within notebook

All notebooks have a cell at the beginning that installs the dependencies. You can run this cell to install the dependencies.

##### Using pip

You can install the dependencies using pip. Run the following command in your terminal:

```bash
pip install ".[lab-n]"    # Where n is the lab number.
```

##### Using uv

You can install the dependencies using uv. Run the following command in your terminal:

```bash
uv sync --extra lab-n    # Where n is the lab number.
```

## Contents

- [Regression](./regression.ipynb)
- [Decision Trees](./decision_tree.ipynb)
- [Unsupervised Algorithms](./unsupervised.ipynb)
- [NLP: Text classification with SVMs](nlp_svm.ipynb)
- [NLP: Prompt Engineering Introduction](nlp_prompting.ipynb)
- [NLP: Tasks with GPT](./nlp_tasks_with_gpt.ipynb)
- [NLP: Retrieval Augmented Generation (RAG)](nlp_rag.ipynb)
