# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Educational Jupyter notebook repository for the Data Science & Advanced Analytics course at EAE Business School (2025 edition). All content lives in top-level `.ipynb` files — there is no application code, no build step, no CI pipeline.

## Dependencies

Managed via `uv` with per-lab optional dependency groups in `pyproject.toml`:

```bash
uv sync --extra lab-1   # regression, decision trees (numpy, pandas, sklearn, seaborn)
uv sync --extra lab-2   # decision trees + visualization (dtreeviz, plotly, pydotplus)
uv sync --extra lab-3   # unsupervised (plotly, sklearn)
uv sync --extra lab-4   # prompt engineering (openai, python-dotenv)
uv sync --extra lab-5   # NLP tasks with GPT (openai, spacy)
uv sync --extra lab-6   # RAG (langchain, chromadb, openai, tiktoken, pypdf)
```

Python version: `>=3.10, <3.13` (ruff targets 3.12).

## Notebook-to-Lab Mapping

| Lab | Notebook(s) | Topic |
|-----|------------|-------|
| 1 | `regression.ipynb` | Linear & logistic regression (sklearn) |
| 2 | `decision_tree.ipynb` | Decision tree classification & visualization |
| 3 | `unsupervised.ipynb` | Clustering & dimensionality reduction |
| 4 | `nlp_prompting.ipynb`, `open_ai_test.ipynb` | Prompt engineering with OpenAI |
| 5 | `nlp_tasks_with_gpt.ipynb`, `nlp_svm.ipynb` | NLP tasks, text classification with SVMs |
| 6 | `nlp_rag.ipynb` | Retrieval-Augmented Generation (LangChain + ChromaDB) |

## Linting

```bash
uv run ruff check .
uv run ruff format --check .
```

Ruff config is in `ruff.toml` (line length 120, extensive lint rule set, target py312).

## Key Conventions

- Each notebook starts with a Colab badge linking to `martatolos/eae-dsaa-2025` on the `main` branch. When renaming or adding notebooks, update the Colab link accordingly.
- Each notebook includes an inline `%pip install` cell so students can run in Colab without local setup. Keep these in sync with `pyproject.toml` optional-dependencies.
- Labs 4-6 require an OpenAI API key via `.env` file or inline variable. `.env` is gitignored.
- `reviews.tsv` is a dataset used by the NLP notebooks.
- PDFs and pickle files are gitignored (used transiently by the RAG lab).
