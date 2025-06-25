# Automated Annotation of Semantic Relationships for Lost Terms in MT

This module automates the classification of **semantic relationships** between *lost rare lemmas* and their counterparts in machine translation (MT) output. It supports the study presented at IWCS 2025 on lexical simplification and rare term loss in domain-sensitive translation settings.

## Objective

The aim is to replace or reduce manual annotation efforts by identifying how lost rare terms in the reference translation relate to their counterparts in the machine-translated sentence. This process improves MT quality analysis in low-resource and domain-specific contexts.

## Target Task

Given a sentence pair (reference vs. MT), the system identifies rare terms missing in the MT and automatically classifies the **type of relationship** between the missing term and the translated content.

### Output: One of the following classes
1. **Spelling or Version Variant**
2. **Abbreviation or Acronym Relation**
3. **Character Set Issue**
4. **Semantic Equivalence**

## Method

We train a classifier based on **ConfliBERT**, a domain-aware language model fine-tuned for political conflict data, using a lightweight classification head.

- The model is trained on manually annotated examples.
- Additional synthetic examples are created for underrepresented classes using:
  - Rule-based acronym expansions and contractions.
  - Back-translation for semantic and spelling variation.
- Four relation classes are used in this implementation (most frequent and automatable).

## Performance

| Class                     | F1 (Validation) | F1 (Test) |
|--------------------------|----------------|-----------|
| Character Set Issue      | 0.75           | 0.67      |
| Spelling / Variant       | 0.67           | 0.64      |
| Semantic Equivalence     | 0.56           | 0.62      |
| Acronym / Abbreviation   | 0.56           | 0.61      |
| **Macro Average**        | **0.64**       | **0.63**  |

## Folder Structure

Automated Annotations/

├── data/ # Training_data_v4.csv

├── models/ # Fine-tuned ConfliBERT model and weights (download and pretrain ConfliBERT)

├── pred/ # mapped_prediction_data.csv

├── scripts/ # Automated_annotation_classifier.ipynb

└── README.md # This file
