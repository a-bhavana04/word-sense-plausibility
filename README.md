# Word Sense Plausibility

Final Project for COMPSCI 685 – Advanced Natural Language Processing

This project studies how encoder-based Transformer models score the plausibility (1–5) of different senses of an ambiguous word when placed inside a narrative context. Instead of predicting a single “correct” sense, the task models graded plausibility, reflecting how humans reason about meaning under uncertainty.


<img width="1280" height="733" alt="image" src="https://github.com/user-attachments/assets/3f98cf58-429d-4bce-820c-9fd355fd1770" />

## Repository Map

* **`encoder-based regression/`** – Baselines that fine-tune ALBERT, BERT, DeBERTa, and RoBERTa exclusively on curated human annotations. Each notebook corresponds to a single model.
* **`synthetic-encoder-based regression/`** – Mirrors of the baseline notebooks that incorporate synthetic examples alongside gold-labeled data; these represent the main experiments.
* **`synthetic-data-gen/`** – Utilities for prompting LLMs, rendering prompts, and evaluating generated examples (`gpt_generation.ipynb`, `llm_annotator.ipynb`, `evaluate.py`).
* **`synthetic-data-outputs/`** – Stores raw JSON outputs from GPT, Mistral, or Qwen runs, along with adjudicated gold references.
* **`SFT+regression/`** – Notebook for instruction tuning (SFT) prior to regression training.
* **`IAA-analysis/`** – Notebooks for calculating inter-annotator agreement (IAA) metrics like Fleiss’ κ.
* **`EDA/`** – Notebook for performing exploratory data analysis on gold as well as synthetic datasets.
