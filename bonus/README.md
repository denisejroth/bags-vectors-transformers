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

## Beyond classification with LLMs

| # | Module | What you'll learn | GPU? |
|---|---|---|---|
| 14 | **Scaling Texts with Pairwise Comparisons** | degrees instead of categories; direct ratings from the model's probabilities; pairwise comparisons in both orders and position bias; Bradley–Terry scaling; validation against crowd toxicity scores; how many comparisons; anchoring new texts | yes |
| 15 | **Information Extraction with an LLM** | records instead of labels; a schema as codebook; free-form JSON versus structured outputs in Ollama; grounding checks for every quote; recall and hand checks; who gets quoted in BBC political news | yes |
| 16 | **Themes and Span Coding** | BERTopic to discover themes, an LLM to name them, a codebook you control; span coding of exact passages; highlighting; word-level agreement and prompt sensitivity; themes across 60 inaugural addresses | yes |
| 18 | **Fine-Tuning an LLM** | when fine-tuning an LLM is worth it; LoRA and QLoRA; training conversations with the prompt masked out; fine-tuning Qwen2.5 0.5B on the bill titles; prompted vs. few-shot vs. fine-tuned; how much data you need; side effects; saving and sharing adapters | yes |
| 19 | **Synthetic Data and Augmentation with LLMs** | what synthetic data is (and isn't) for; augmenting 40 coded titles with LLM paraphrases; synthetic titles from definitions and with real examples; comparing classifiers on the same real test set; checks for diversity, realism, label quality and leakage; temperature, rare categories and memorized titles; risks and reporting | yes |

These modules build on Day 4 (prompting, label scoring, validation) and use small open models that run
on Colab's free GPU: Qwen2.5 1.5B through Hugging Face in modules 14 and 19, Qwen2.5 7B through Ollama
in modules 15 and 16, and Qwen2.5 0.5B with LoRA in module 18. Module 16 starts from the BERTopic workflow
of module 11 and reuses the structured outputs of module 15, but works on its own. Modules 18 and 19 use
the same bill titles and test set as Day 4, so their results compare directly with the prompting
strategies there and with fine-tuned BERT on Day 3. Module 19 turns the question around: instead of
using an LLM to code texts, it uses one to write extra training texts, and asks when that helps.

## Beyond English

| # | Module | What you'll learn | GPU? |
|---|---|---|---|
| 17 | **Working with Other Languages** | three routes (a model for your language, a multilingual model, translation first); tokenizer costs across nine parallel languages; RobBERT vs. XLM-R for Dutch; cross-lingual transfer; translate-test and translate-train with NLLB-200; low-resource languages; language identification in mixed corpora; comparability across languages; multilingual embeddings | yes |

Module 17 uses SIB-200: the same sentences in more than 200 languages, so every comparison between
languages is fair. It runs nine of them, from English and Dutch to Limburgish, Yoruba and Quechua.

## Some routes through the material

- **Working with interviews:** 2 (transcribe) → 4 (anonymize) → 5 (code and validate)
- **Building a corpus:** 1 (files) and 3 (web) → 13 (at scale)
- **Measurement for a causal analysis:** 5 (validation) → 12 (causal inference with text)
- **Understanding what BERT replaced:** 6 → 7 → 8, then back to Day 3
- **LLMs for measurement:** Day 4 → 14 (scales) → 15 (records) → 16 (themes and spans), with 5 for validation
- **Prompting, distilling or fine-tuning:** Day 3 (BERT) → Day 4 (prompting, distillation) → 18 (fine-tuning an LLM)
- **From exploring to measuring:** 11 (topics) → 16 (from topics to a codebook and spans)
- **Comparative and multilingual research:** 1 or 3 (collect) → 17 (languages) → 5 (validate in every language)
- **When coded data is scarce:** 5 (how many to annotate) → Day 4 (distillation) → 19 (synthetic training data) → 18 (fine-tuning)

## Slides

`slides/` has a PDF of each deck.

## Notebooks

Open any notebook in Colab with the button at its top. For modules 2, 9 and 14 to 19, enable a GPU first
(*Runtime → Change runtime type → T4 GPU*); module 11 runs fine without one.

A few modules need something extra:

- **Module 3** uses the OpenAlex API. Since February 2026 OpenAlex works with free API keys; without a key
  you get a small daily budget, enough for the notebook. The notebook explains how to add a key via
  Colab's *Secrets*.
- **Modules 2, 4, 10 and 11** download models on first use (Whisper, spaCy, a sentence transformer); that
  takes a minute.
- **Module 9** downloads pre-trained image weights; **modules 6 to 8 and 11** download two chunks of the
  bills dataset, as on Day 3.
- **Module 14** downloads Qwen2.5 1.5B and the Civil Comments validation split. ⚠️ The comments are real
  and include insults and profanity; the notebook leaves out identity attacks, threats and sexual content.
- **Modules 15 and 16** install Ollama in Colab and download Qwen2.5 7B (4.7 GB); together that takes a few
  minutes. Module 16 also downloads a sentence transformer and NLTK's inaugural addresses. No accounts or
  API keys are needed for any of the three.
- **Module 17** downloads several models (RobBERT, XLM-RoBERTa, NLLB-200, two sentence transformers and
  GlotLID, about 5 GB in total) and nine languages of SIB-200. NLLB-200's license allows research use
  only.
- **Module 18** downloads Qwen2.5 0.5B and two chunks of the bills dataset; fine-tuning takes a few
  minutes on a T4.
- **Module 19** downloads Qwen2.5 1.5B and two chunks of the bills dataset; generating the paraphrases
  and synthetic titles takes about ten minutes on a T4.
