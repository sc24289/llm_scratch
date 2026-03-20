# Knowledge Extraction Rules — LLM Course Project

## Purpose

Define how cleaned lecture transcripts are transformed into structured knowledge representations.

This corresponds to:

> **Stage 2 — Knowledge Extraction** in the project architecture

Goal:

> Extract knowledge independent of lecture narration.

---

## Input

* Cleaned lecture file (`lectureXX.md`)
* Must already comply with `cleaning_rules.md`

---

## Output

* Knowledge file (`lectureXX_knowledge.md`)
* Structured, concept-driven representation

---

## Core Principle

This stage is **NOT summarization**.

It is:

> Transformation from narrative → structured knowledge

---

## 🔴 Concept Extraction Rule (Critical)

Extract all key concepts explicitly.

For each concept:

* Provide a clear **name**
* Provide a **definition**
* Provide an **explanation**

Do NOT:

* leave concepts implicit
* rely on lecture phrasing

---

## 🟡 De-Narration Rule

Remove lecture-style narration:

* greetings
* transitions
* storytelling structure

Convert:

> “In this lecture we will see…”

Into:

> direct knowledge statements

---

## 🔵 Structure Over Sequence Rule

Do NOT follow lecture order blindly.

Instead:

* group related ideas together
* reorganize content logically

Goal:

> maximize clarity, not fidelity to sequence

---

## 🟣 Technical Completeness Rule

ALL technical content must be preserved.

This includes:

* definitions
* examples
* distinctions
* mechanisms
* edge cases

Do NOT:

* drop details for brevity
* simplify technical explanations

---

## 🟠 Relationship Extraction Rule

Make relationships explicit.

Examples:

* Concept A → leads to Concept B
* Concept C depends on Concept D
* Process E produces Output F

This is one of the most important steps.

---

## 🧩 Process Extraction Rule

When a process is described:

* extract it as a structured sequence

Format:

* Step 1
* Step 2
* Step 3

Examples:

* training pipeline
* tokenization steps
* model workflow

---

## 🧪 Example Preservation Rule

All examples must be preserved.

Types:

* conceptual examples
* practical examples
* input/output examples

Examples should be:

* clearly separated
* easy to identify

---

## ⚖️ Distinction Rule

Explicitly capture comparisons.

Examples:

* GPT vs Transformer
* Pre-training vs Fine-tuning
* Zero-shot vs Few-shot

Format:

* side-by-side comparison when possible

---

## ⚠️ Misconception Rule

If the lecture implies or states misconceptions:

* capture them explicitly

Examples:

* common misunderstandings
* incorrect assumptions

---

## 🔗 Dependency Rule

Identify prerequisites:

* What must be understood before this concept?

Example:

* To understand embeddings → need tokens
* To understand GPT → need Transformer

---

## ⚪ Abstraction Rule

Move from:

* lecture-specific phrasing

To:

* general knowledge representation

Example:

Bad:

> “The lecturer explains that GPT is…”

Good:

> “GPT is a decoder-only Transformer model”

---

## 🧱 Output Structure Rule

Each knowledge file must include:

* Core Concepts
* Relationships
* Processes
* Examples
* Distinctions
* Dependencies
* Key Takeaways

(Exact formatting handled by `markdown_output_rules.md`)

---

## 🚫 Strict Prohibitions

* Do NOT summarize
* Do NOT omit technical content
* Do NOT keep lecture narration
* Do NOT introduce new knowledge

---

## 🎯 Quality Check

A good knowledge file should allow:

* understanding concepts without the lecture
* reconstructing the learning path
* identifying dependencies between ideas

---

## Final Principle

> If Stage 1 answers:
> “What was said?”
>
> Stage 2 answers:
> **“What must be known?”**

---

## 🧱 Required Output Structure

Each knowledge file MUST follow this structure:

# Lecture XX — Knowledge

## Core Concepts

## Definitions

## Key Mechanisms / Processes

## Relationships

## Examples

## Key Properties / Characteristics

## Comparisons

## Misconceptions

## Dependencies

---

### Definitions Format (Strict)

Each definition must follow:

Concept: <name>  
Definition: <clear, precise explanation>

---

### Relationships Format

Concept A → relation → Concept B

---

### Process Format

Step 1  
Step 2  
Step 3  

---

### Comparisons Format

Use tables whenever possible.

---
