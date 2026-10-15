# Bonus: Good to Know

Material that didn't fit into the four course days but is worth knowing. Each module has a short
slide deck and a notebook (an `_exercises` version and a matching `_solutions` version), written
for self-study. Most modules stand on their own, so pick what you need; only 6 to 8 build on each
other.

## Getting text to analyze

| # | Module | What you'll learn | GPU? |
|---|---|---|---|
| 1 | **From PDFs (and Other Files) to Analyzable Text** | born-digital PDFs, tables, OCR for scans (English and Dutch), Word and HTML, measuring extraction quality, a batch pipeline | no |
| 2 | **Transcribing Audio and Video** | Whisper for English and Dutch, word error rate and normalization, model sizes, long recordings and video, hallucinations and how to catch them, a folder of recordings to a dataset | recommended |
| 3 | **Web Scraping and APIs** | a legal and ethical checklist, polite HTTP requests, robots.txt, scraping with BeautifulSoup, caching, the OpenAlex and Wikipedia APIs | no |

## Handling text responsibly

| # | Module | What you'll learn | GPU? |
|---|---|---|---|
| 4 | **Anonymizing Text** | direct and indirect identifiers, regular expressions and spaCy NER, measuring recall and precision in English and Dutch, redaction, pseudonyms and surrogates, a human leak check | no |
| 5 | **Annotation and Validation** | codebooks and samples, percent agreement vs. Cohen's kappa vs. Krippendorff's alpha, learning from disagreements, validating a classifier with confidence intervals, how many documents to annotate, biased proportions | no |

## Neural networks under the hood

| # | Module | What you'll learn | GPU? |
|---|---|---|---|
| 6 | **Neural Networks, the Basics** | neurons, activations and layers; how networks learn; a network written from scratch; the same classifier in scikit-learn, Keras and PyTorch; overfitting | no |
| 7 | **Convolutional Neural Networks for Text** | convolutions as learned phrase detectors; text CNNs in Keras and PyTorch; starting from GloVe; reading what each filter learned | no |
| 8 | **Recurrent Neural Networks and LSTMs** | why word order matters; the memory problem and how LSTMs solve it; bidirectional LSTMs in Keras and PyTorch; the road to attention | no |
| 9 | **Convolutional Neural Networks for Images** | images as data; CNNs in Keras and PyTorch; inside the network; pre-trained models and image embeddings; social science uses and ethics | recommended |

Modules 6 to 8 use the same bill titles, and the same train/validation/test split, as the Day 3
BERT notebook, so all scores can be compared directly with the TF-IDF baseline and fine-tuned
BERT. Keras runs on the PyTorch backend throughout, so both frameworks share one engine.

## More methods

| # | Module | What you'll learn | GPU? |
|---|---|---|---|
| 10 | **Linguistic Analysis with spaCy** | tokens, lemmas and parts of speech; named entities; dependency parsing and subject-verb-object triples; the rule-based Matcher; 60 US inaugural addresses; Dutch; processing at scale | no |
| 11 | **Topic Models with BERTopic** | embed, reduce, cluster, describe; inspecting and labeling topics; validation against known categories; how settings and random seeds change the topics; outliers; topics over time; LDA | optional |
| 12 | **Text as Data for Causal Questions** | text as outcome, treatment or confounder; differential measurement error; design-based supervised learning (DSL); why discovery and testing need separate data; adjusting for text | no |

Module 11 builds on Thursday's session on sentence transformers and document clustering, and focuses
on what that session leaves for later: validation, stability and the choices that shape a topic model.

## Doing it for real

| # | Module | What you'll learn | GPU? |
|---|---|---|---|
| 13 | **Scaling Up and Reproducibility** | pinning packages, models and data; seeds; project structure; caching; chunked and resumable jobs; from notebook to script; SLURM job arrays; git, Zenodo and a reproducibility checklist | no |

## Some routes through the material

- **Working with interviews:** 2 (transcribe) → 4 (anonymize) → 5 (code and validate)
- **Building a corpus:** 1 (files) and 3 (web) → 13 (at scale)
- **Measurement for a causal analysis:** 5 (validation) → 12 (causal inference with text)
- **Understanding what BERT replaced:** 6 → 7 → 8, then back to Day 3

## Slides

`slides/` has a PDF of each deck. 
## Notebooks

Open any notebook in Colab with the button at its top. For modules 2 and 9, enable a GPU first
(*Runtime → Change runtime type → T4 GPU*); module 11 runs fine without one.

A few modules need something extra:

- **Module 3** uses the OpenAlex API. Since February 2026 OpenAlex works with free API keys; without a key
  you get a small daily budget, enough for the notebook. The notebook explains how to add a key via
  Colab's *Secrets*.
- **Modules 2, 4, 10 and 11** download models on first use (Whisper, spaCy, a sentence transformer); that
  takes a minute.
- **Module 9** downloads pre-trained image weights; **modules 6 to 8 and 11** download two chunks of the
  bills dataset, as on Day 3.
