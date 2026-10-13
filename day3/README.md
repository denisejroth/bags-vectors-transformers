# Day 3 — Transformers

Contextual embeddings: how models finally learn that a word's meaning depends on its
sentence. Attention, BERT, and how to use transformers in practice.

## Slides
1. **Contextual Embeddings**: the "bank" problem, attention, BERT, masked language modeling,
   what BERT was trained on and what that costs, word pieces, and what comes out of the model
2. **Transformers in Practice**: pre-train/fine-tune, three ways to use a model, how zero-shot
   classification and fine-tuning work, choosing an approach, measuring success
3. **The Hugging Face Hub**: loading models and datasets, reading a model card, choosing a model,
   where your data goes, and a Hub scavenger hunt
4. **Your Turn: BERT on New Data**: the group exercise, reporting back, how classification errors
   carry into your analysis, and what to report in a paper

## Notebooks
1. **BERT**: Part A opens the model up (tokenization, hidden states, the "bank" test, attention);
   Part B classifies policy texts with a TF-IDF baseline, zero-shot classification, frozen
   features and fine-tuning
2. **Your Turn: BERT on New Data** (group exercise): each table takes one of three datasets from
   the Hugging Face Hub (environmental claims, climate sentiment, or PUBHEALTH health claims),
   compares a TF-IDF baseline, zero-shot classification and fine-tuning, and reports back to the room

Each comes with an `_exercises` version and a matching `_solutions` version.

⚠️ **Enable a GPU** in Colab (*Runtime → Change runtime type → T4 GPU*) before running.
