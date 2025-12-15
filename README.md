# ChatGPT vs. the Duplex

This repository contains data, code, and documentation for **ChatGPT vs. the Duplex**, This project examines how different generative AI models attempt to write duplex poems, a form created by Jericho Brown that depends on repetition, variation, and emotional compression. Our study, undertaken as a class, combines computational approaches with close reading. We generate duplexes using several state-of-the-art models, measure phrase repetition and similarity, evaluate meter and rhyme, and compare AI-written poems to Brown’s examples. By analyzing both the form and the language of these poems, the study shows to what degree AI captures the meaning and significance of the duplex as well as what its limits reveal about creativity and the difficulty of capturing a poet’s voice

## Project Overview

This project examines whether contemporary generative AI models can:
1. Identify the poetic form known as the **duplex**
2. Generate poems that meaningfully adhere to the duplex’s formal constraints



## Related Work

Our methodology builds on two foundational studies by Walsh et al.:

- *Sonnet or Not, Bot? Poetry Evaluation for Large Models and Datasets* (EMNLP 2024)
- *Does ChatGPT Have a Poetic Style?* (CHR 2024)
- *Fightin' Words: Lexical Feature Selection and Evaluation for Identifying the Content of Political Conflict* (Cambridge University Press, 2017)


## Data

### Human-Authored Poetry
- Public-domain poems from Walsh et al.’s released dataset
- Additional ghazals and blues poems collected from Poetry Foundation and Poets.org
- Jericho Brown’s five duplex poems (used for analysis, not prompting)

### AI-Generated Poetry
- Models: GPT-4 (258) , GPT-4o Mini (258) , Claude Sonnet 4.5 (258) , OLMo 3-7B-Instruct (254)
- Prompt types: general, figurative, specific
- Total poems generated: 1,019

All data were cleaned to remove titles, prefatory text, encoding artifacts, and model commentary.

## Experiments

We conduct three categories of experiments:

1. **Memorization tests**
2. **Poetic form classification**
3. **Formal and stylistic analysis of generated duplexes**, including:
   - Repetition adherence
   - Syllable counts
   - Cosine similarity to Brown’s duplexes
   - Pronoun usage
   - Significant word analysis (Monroe et Al's “fighting words”)

## Repository Structure

```text
duplex-project/
│
├── DH_2026_abstract.pdf
│
├── data/
│   ├── ai_generated_poetry/
│   │   ├── clean/
│   │   └── raw/
│   │
│   ├── original_human-authored_poetry/
│   │
│   ├── poems_and_tags/
│   │
│   ├── repeating_phrases/
│   │
│   ├── similarity_scores/
│   │
│   └── duplex_themes.xlsx
│
├── notebooks/
│   ├── syllable_meter_rhyme_analysis.ipynb
│   ├── Repeating_Phrases.ipynb
│   ├── Poem_Similarity v2.ipynb
│   └── duplex-or-not-public.ipynb
│
└── README.md
```
