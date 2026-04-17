+++
title = "B.Tech Major Project: Legal Judgment Summarization using Transformer Models"
slug = "btech-major-project-nit-hamirpur"
date = 2026-04-16T00:00:00+05:30
draft = false
+++

## Overview

Designed and implemented an end-to-end NLP system to automatically summarize long-form Indian court judgments using transformer-based architectures.

This project focuses on handling **long-context documents**, **domain-specific language**, and **evaluation of abstractive summarization models**.

---

## Problem Statement

Legal judgments are often lengthy and complex, making them difficult to quickly interpret.  
The goal was to generate concise, meaningful summaries while preserving legal semantics.

---

## Tech Stack

Python, HuggingFace Transformers, PyTorch, NLP

---

## System Design

- **Data Preprocessing**
  - Cleaned and structured raw legal documents  
  - Converted Data into JSON files to properly map them to there respective Judgement and it's summary as reading and writing such long files was very resource coming on the large scale.


- **Chunk-based Summarization**
  - Split long judgments into smaller chunks due to transformer token limits  
  - Generated partial summaries and merged them  

- **Model Training**
  - Fine-tuned multiple transformer models  
  - Experimented with different architectures and hyperparameters  

- **Evaluation**
  - Used **ROUGE, BLEU, and BERTScore**  
  - Performed comparative analysis across models  

---

## Key Results

- Processed **4,378 Indian court judgments**
- Achieved **+9.2% improvement in ROUGE score**
- Built a scalable pipeline for long-document summarization

---

## Challenges

- Handling **very long input sequences**
- Maintaining **semantic consistency across chunks**
- Evaluating summaries beyond surface-level metrics

---

## Key Learnings

- Deep understanding of **transformer limitations and optimization**
- Model evaluation and selection in research settings

---

## Future Work

- Improve coherence using hierarchical summarization  