# Bags, Vectors & Transformers

### A Methods Workshop in Computational Text Analysis

A four-day, hands-on introduction to computational text analysis in Python. The course starts
with counting words and ends with large language models, and every topic comes with a notebook
you can run in your browser.

The course was first taught as a WASS PhD course at Wageningen University & Research on
October 12–16, 2026. The materials are written so you can also work through them on your own.

**Instructor:** Denise J. Roth, Strategic Communication Group, Wageningen University & Research<br>
**Sentence transformers session (Day 4):** Art Dewulf, Public Administration and Policy Group,
Wageningen University & Research

---

## What the course covers

The course follows one arc: from counting words, to representing meaning, to models that read
each word in its context. Along the way it keeps returning to the same advice: start with the
simplest method that works, add complexity only when it pays off, and validate everything.

| Day | Theme | Topics |
|-----|-------|--------|
| **1** | Bags | Text as data, preprocessing, the document-term matrix, TF-IDF, dictionaries, supervised machine learning, topic modeling, and the limits of bag-of-words |
| **2** | Vectors | Word embeddings: the distributional hypothesis, Word2Vec and GloVe, similarity and analogies, bias and measurement, embeddings as features |
| **3** | Transformers | Contextual embeddings, attention, BERT, zero-shot classification and fine-tuning, the Hugging Face Hub, and a group exercise on new data |
| **4** | Sentence transformers and LLMs | Sentence embeddings, clustering and topic modeling; how LLMs work, three ways to reach one, data annotation and validation, ethics, open and local models, and distillation |

Beyond the four days, the `bonus/` folder has 19 self-study modules (see below).

## Prerequisites

Basic Python, roughly at the level of an introductory course such as DataCamp's *Introduction to
Python* (variables, lists, loops, functions). No experience with text analysis is needed. If you
are new to coding, you can still follow the ideas, but plan some extra time for the notebooks.

## How the repository is organized

```
day1/                     Bags: bag-of-words methods
day2/                     Vectors: word embeddings
day3/                     Transformers: BERT and the Hugging Face Hub
day4/                     LLMs
  SentenceTransformers/   slides and notebooks for the sentence transformers session
bonus/                    19 self-study modules and an extra notebook
playground/               an embedding playground that runs in your browser
requirements.txt
LICENSE
```

Each day has a `slides/` folder with PDFs of the lecture decks and a `notebooks/` folder with
the hands-on material. Most notebooks come in pairs: an `_exercises` version to work through and
a `_solutions` version to check your answers against. Each day also has its own `README.md` with
a short guide to that day's materials.

## Running the notebooks

The notebooks are written for Google Colab, so you don't need to install anything. Open a
notebook here on GitHub and click the **Open in Colab** button at the top. The first cells
install whatever that notebook needs.

- Days 1 and 2 run on a normal (CPU) runtime.
- Days 3 and 4 use transformer models and LLMs, so switch on a GPU before you start:
  *Runtime → Change runtime type → T4 GPU*.
- For the bonus modules, `bonus/README.md` says which ones need a GPU.

No accounts or API keys are needed, except for the optional OpenRouter section of the Day 4
notebook on reaching an LLM; without a key, those cells skip themselves.

To run the notebooks on your own computer instead, use Python 3.10 or newer and install the
packages in `requirements.txt`. That file covers the core packages; the sentence transformers
notebooks and most bonus modules install a few more in their first cells.

## Bonus material

The `bonus/` folder collects material that didn't fit into four days. Each module has a short
slide deck and a notebook, and most stand on their own:

- **Getting text to analyze:** PDFs and OCR, audio and video, web scraping and APIs (1 to 3)
- **Handling text responsibly:** anonymizing text, annotation and validation (4 and 5)
- **Neural networks under the hood:** the basics, CNNs and RNNs for text, CNNs for images (6 to 9)
- **More methods:** spaCy, topic models with BERTopic, text as data for causal questions (10 to 12)
- **Doing it for real:** scaling up and reproducibility (13)
- **Beyond classification with LLMs:** scaling with pairwise comparisons, information extraction,
  themes and span coding, fine-tuning an LLM, synthetic data and augmentation (14 to 16, 18, 19)
- **Beyond English:** working with other languages (17)

[`bonus/README.md`](bonus/README.md) describes every module and suggests a few routes through
the material. The folder also has an extra notebook by Art Dewulf on zero-shot classification
with a local LLM through `llama-cpp-python` (needs a GPU).

## Embedding playground

`playground/index.html` lets you explore the same 50-dimensional GloVe vectors as the Day 2
notebook: find a word's nearest neighbors, compare two words, solve analogies, place words
between two poles, and find the odd one out. Download the file and open it in any browser. The
vectors are built into the file, so it works offline too.

## Data and models

The notebooks use small, openly available datasets and models, so they run without special
access:

- Short example texts written into the first notebooks
- US presidential inaugural addresses (NLTK's `inaugural` corpus) and the Brown corpus
- TweetEval sentiment (`cardiffnlp/tweet_eval`)
- US Congressional bill titles labeled by policy area (`dreamproit/bill_labels_us`, public domain)
- For the Day 3 group exercise: ClimateBERT's environmental claims and climate sentiment
  datasets, and PUBHEALTH health claims
- Pre-trained GloVe vectors, BERT-style models and sentence transformers, and Qwen2.5 1.5B
  Instruct as the open LLM on Day 4

The bonus modules use a few other datasets, and each module explains its own.

## Acknowledgments

Thanks to Art Dewulf for developing and teaching the sentence transformers session, to Summer
Skillen for her help as teaching assistant, and to the Wageningen School of Social Sciences
(WASS) for making the course possible.

## License and citation

The course materials are licensed under CC BY 4.0: you can share and adapt them for any
purpose, as long as you give credit. Datasets and pre-trained models keep their own licenses.
See `LICENSE` for details.

To credit the materials:

> Roth, D. J. (2026). *Bags, Vectors & Transformers: A methods workshop in computational text
> analysis* [Course materials]. Wageningen University & Research.
> https://github.com/denisejroth/bags-vectors-transformers
