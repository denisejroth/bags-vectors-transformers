# Bags, Vectors & Transformers

### A Methods Workshop in Computational Text Analysis

A four-day, hands-on introduction to computational text analysis in Python, for PhD
students. The course runs from classic bag-of-words methods all the way to large language
models, with a working notebook for every topic.

**Instructor:** Denise J. Roth · Strategic Communication Group · Wageningen University & Research

---

## What this course covers

The workshop follows a single arc — **from counting words, to representing meaning, to
context-aware models** — and, throughout, stresses one discipline: start with the simplest
tool that works, add complexity only when it earns its place, and validate everything.

| Day | Theme | Topics |
|-----|-------|--------|
| **1** | Bags | Text as data, preprocessing, the document-term matrix, TF-IDF, dictionaries, supervised ML, topic modeling, and the limits of bag-of-words |
| **2** | Vectors | Word embeddings: the distributional hypothesis, Word2Vec & GloVe, similarity & analogies, bias & measurement, embeddings as features |
| **3** | Transformers | Contextual embeddings, attention, BERT, fine-tuning, and using models in practice |
| **4** | LLMs | Large language models, data annotation, ethics & responsible use, open/local models, and distillation |

## How the repository is organized

Everything is grouped **by day**. Inside each day, `slides/` holds the lecture decks (PDF to
view, `.tex` source to edit) and `notebooks/` holds the hands-on material — each topic has an
`_exercises` notebook (for participants) and a matching `_solutions` notebook.

```
day1/
  slides/       lecture decks (.pdf + .tex source)
  notebooks/    *_exercises.ipynb  and  *_solutions.ipynb
day2/  ...
day3/  ...
day4/  ...
```

Each day also has its own `README.md` with a short guide to that day's materials.

## Running the notebooks

The notebooks are written for **Google Colab** — no local installation needed. Open a
notebook, and at the top of each you'll find setup cells that install what's required.

- **Days 1–2** run on a normal (CPU) Colab runtime.
- **Days 3–4** use transformer models and LLMs: switch on a GPU via
  *Runtime → Change runtime type → T4 GPU* before running them.

To run locally instead, see `requirements.txt`. Python 3.10+ is recommended.

## A note on the data

The notebooks use small, openly available datasets so they run anywhere with no special
access:

- Toy corpora (hardcoded example sentences) for the earliest, illustrative notebooks
- The **NLTK inaugural address** corpus (US presidential inaugurals, 1789–present)
- **TweetEval** sentiment (an academic tweet benchmark)
- **`dreamproit/bill_labels_us`** — US Congressional bills labeled by policy area (public domain)
- Pre-trained **GloVe** vectors and small open models from the **Hugging Face Hub**

## Setup for instructors

Each notebook has an **"Open in Colab"** badge at the top. These point at a placeholder path
(`YOUR-USERNAME/bags-vectors-transformers`). After you create the GitHub repository, do a
find-and-replace across the notebooks to swap in your actual `username/repo` (and branch, if
not `main`) so the badges open the right files.

## Prerequisites

Basic Python, roughly at the level of an introductory DataCamp course (variables, lists,
loops, functions). No prior experience with text analysis is assumed — the course starts
from the beginning.

## License

Course materials are shared for teaching and research use. See `LICENSE` for details.
