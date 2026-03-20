---
title: Introduction to Large Language Models
source: lecture02.txt
cleaned_on: 2026-03-19
---

# Introduction

Hello everyone, welcome to the second lecture in the **“Building Large Language Models from Scratch”** series.

In the previous lecture, we introduced the overall goals of this series. Our objective is not just to explore applications, but to understand how large language models (LLMs) work from a fundamental level.

---

## Lecture Overview

In this lecture, we will cover:

1. What is a large language model (LLM)?
2. Why are they called “large”?
3. Differences between modern LLMs and earlier NLP models
4. The “secret sauce” behind LLMs
5. Key terminology: AI, ML, Deep Learning, Generative AI, LLMs
6. Applications of LLMs

---

## What is a Large Language Model?

At its simplest:

> A large language model is a neural network designed to understand, generate, and respond to human-like text.

### Key Components

- **Neural Network**
  - Consists of layers of interconnected neurons
  - Learns patterns from data

- **Language Capability**
  - Understands input text
  - Generates meaningful responses
  - Mimics human-like interaction

### Example

Using a system like ChatGPT:
- You provide input (e.g., “Plan a relaxing day”)
- The model responds with structured, context-aware suggestions

This demonstrates:
- Understanding
- Generation
- Contextual reasoning

---

## Why “Large” Language Models?

The term “large” refers to the **number of parameters** in the model.

### Example: GPT Models

- GPT-3 Small: 125 million parameters
- GPT-3 Medium: 350 million
- GPT-3 Large: 760 million
- GPT-3: 175 billion parameters

Modern models can even reach **trillions of parameters**.

### Key Insight

- More parameters → higher capacity to learn patterns  
- Larger models → better performance on complex tasks  

---

## LLMs vs Earlier NLP Models

### Earlier NLP Models

- Designed for **specific tasks**
  - Translation
  - Sentiment analysis
  - Classification
- Required separate models for each task

### LLMs

- **General-purpose**
- One model can perform:
  - Translation
  - Question answering
  - Text generation
  - Summarization

### Example

Earlier:
- One model → translation  
- Another → sentiment analysis  

Now:
- One LLM → all tasks  

---

## The Secret Behind LLMs

The key innovation is the **Transformer architecture**.

### Key Points

- Introduced in the 2017 paper:
  **“Attention Is All You Need”**
- Enables:
  - Context understanding
  - Long-range dependencies
  - Efficient training

### Important Note

The Transformer architecture is the foundation of modern LLMs.

---

## Key Terminology

### Concept Hierarchy

```mermaid
graph TD
    AI[Artificial Intelligence]
    ML[Machine Learning]
    DL[Deep Learning]
    LLM[Large Language Models]

    AI --> ML
    ML --> DL
    DL --> LLM