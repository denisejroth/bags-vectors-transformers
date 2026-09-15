# Day 4 — Large Language Models

What LLMs are, how to use them for research (especially data annotation), the ethical and
practical questions they raise, and how to get the best of both worlds through distillation.

## Slides
1. **LLMs & Annotation** — what LLMs are, what they do, prompting, and data annotation
2. **Ethics, Open Models & Distillation** — responsible use, the case for open/local models,
   and distilling an LLM into a fast BERT classifier

## Notebooks
1. **LLM Annotation** — run a small open LLM locally, annotate policy text, validate against
   a gold standard, distill into a BERT classifier, and see how you'd do it with Ollama

Comes with an `_exercises` version and a matching `_solutions` version.

⚠️ **Enable a GPU** in Colab (*Runtime → Change runtime type → T4 GPU*) before running.
Uses an open, ungated model (Qwen2.5-1.5B) — no account or API key required.
