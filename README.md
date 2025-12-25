# Semantic Representation of Idioms

This project investigates how multilingual sentence embeddings represent idiomatic expressions, with a focus on the distinction between literal and figurative meaning and on cross-lingual semantic alignment.

The experiments are based on the **LaBSE** multilingual sentence embedding model and evaluate its behavior on idiomatic data in English and Russian.

---

## Research Questions

1. **Monolingual:**  
   Does LaBSE distinguish between literal and figurative uses of idioms within a single language?

2. **Cross-lingual:**  
   Are idiomatic meanings preserved across languages in the embedding space?

3. **Semantic vs. Lexical Preference:**  
   Does the model prefer literal translations over **definitions** of idioms?

---

## Experiments

### Experiment 1: Monolingual Idiom Distinction (MAGPIE)
- Dataset: MAGPIE
- Task: Compare similarities between
  - figurative–figurative
  - literal–literal
  - figurative–literal pairs
- Metrics:
  - Cosine similarity distributions
  - Mann–Whitney U tests
  - Cohen’s *d*
  - Precision@k (global and by usage)
  - PCA + silhouette score

---

### Experiment 2: Cross-lingual Alignment (RU–EN)
- Dataset: Idioms in Context (RU–EN)
- Task:
  - Compare aligned vs. random RU–EN sentence pairs
- Metrics:
  - Mean cosine similarity
  - Retrieval accuracy (Precision@1/5/10)
  - Cohen’s *d*
- Baseline:
  - TF-IDF cosine similarity

---

### Experiment 3: Literal vs. Definition Preference (LIdioms)
- Dataset: LIdioms
- Task:
  - Compare the similarity of Russian idioms to
    - **literal translations**
    - **definitions (paraphrases of meaning)**
- Metrics:
  - Mean similarity difference
  - Proportion of cases preferring literal vs. definition
  - Mann–Whitney U test
  - Cohen’s *d*

---

## How to Run

The experiments are implemented in a single Jupyter notebook.

### Google Colab (recommended)
1. Upload the entire repository **including all folders** (`data/`, `data_utils/`, `model/`, `experimentation/`).
2. Open `main.ipynb` in Google Colab.
3. Install dependencies if prompted:
   ```python
   !pip install sentence-transformers scikit-learn numpy pandas scipy 
4. Run all cells (Runtime → Run all).

### Local
1. Clone the repository (all folders are required).
2. Install dependencies:
!pip install sentence-transformers scikit-learn numpy pandas scipy jupyter
3. Open and run main.ipynb.
All datasets required to reproduce the results are included in the repository.


