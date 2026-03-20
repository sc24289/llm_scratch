# Cleaning Rules — LLM Course Project

## Purpose

Define how raw transcripts are transformed into clean, structured Markdown while **preserving all content**.

This stage corresponds to **Stage 1 — Source Processing** in the project architecture.

---

## TASK

You are cleaning a raw YouTube transcript and converting it into structured Markdown.

---

## GOAL

Preserve all meaningful content while improving:

* readability
* structure
* correctness

Cleaning must be **lossless**.

---

## INPUT

* Raw transcript (`.txt`)

---

## OUTPUT

* Clean, structured Markdown (`.md`)
* Content must remain faithful to the original lecture

---

## Core Instructions

### 1. Clean Formatting

* Remove timestamps
* Remove filler words (um, uh, you know, etc.)
* Fix punctuation and sentence boundaries
* Merge broken lines into proper paragraphs

---

### 2. Preserve Meaning (Critical)

* Do NOT summarize
* Do NOT omit technical content
* Do NOT simplify explanations unless strictly redundant
* Keep:

  * all concepts
  * all examples
  * all reasoning

---

### 3. Improve Clarity

* Fix transcription errors (e.g., wrong technical terms)
* Normalize terminology:

  * LLM
  * Transformer
  * Tokenization

---

### 4. Add Structure

* Add a top-level title
* Organize content into sections (`##`, `###`)
* Group related ideas into paragraphs

---

### 5. Optional Enhancements

ONLY if clearly implied:

* Bullet points for lists
* Code blocks (if code is explicitly discussed)
* Short clarifications (minimal, non-intrusive)

---

### 6. Strict Prohibitions

* Do NOT add new knowledge
* Do NOT change the intent of the speaker
* Do NOT convert into a summary or tutorial
* Do NOT remove content because it seems redundant

---

# 🔴 Technical Completeness Rule (CRITICAL)

ALL technical content must be preserved.

This includes:

* Code explanations (even if incomplete)
* Specific tokens, parameters, functions
* Edge cases and alternative scenarios
* Comparisons (e.g., GPT vs NLP models)
* Implementation notes

Do NOT remove content that appears:

* repetitive
* secondary
* loosely structured

👉 If it contributes to understanding, it must remain.

---

# 🟡 Repetition Handling Rule

Repetition must NOT be blindly removed.

Allowed:

* Consolidate repeated explanations into a structured block

Not allowed:

* Removing repeated explanations that add:

  * nuance
  * examples
  * clarification

---

# 🔵 Code Fidelity Rule

When code is discussed:

* Preserve ALL explanations
* Preserve:

  * variable names
  * token names
  * function names
  * workflow

Do NOT:

* reconstruct missing code
* simplify code logic
* remove partial code descriptions

---

# 🟣 Special Tokens Preservation Rule

When tokens are mentioned, they MUST be explicitly preserved.

Examples:

* `<|endoftext|>`
* `<|unk|>`
* `[BOS]`, `[EOS]`, `[PAD]`

Do NOT:

* generalize them
* omit specific names

---

# 🟠 Technical Detail Preservation

Do NOT collapse or simplify technical sections.

Always preserve explicitly:

* tokens
* parameters
* lists of concepts

Example:

Correct:

* `<|endoftext|>, <|unk|>, [BOS], [EOS], [PAD]`

Incorrect:

* “special tokens”

---

# 🧩 Code Placeholder Rule

When code is referenced but not fully present:

* Insert a placeholder
* Preserve surrounding explanation
* Do NOT reconstruct or invent code

The placeholder must follow the formatting defined in:

👉 `markdown_output_rules.md`

---

# ⚪ Lossless Cleaning Principle

Stage 1 cleaning must be **lossless**.

Goal:

> The cleaned document should allow reconstruction of the original lecture.

This means:

* No technical information is removed
* No conceptual explanation is lost

Cleaning =
✔ formatting
✔ structuring

NOT =
❌ summarization
❌ compression

---

# ✅ Final Checklist

Before finalizing output:

* [ ] No content loss
* [ ] All technical details preserved
* [ ] Special tokens explicitly listed
* [ ] Code explanations preserved
* [ ] Placeholder inserted where needed
* [ ] Structure improved but meaning unchanged

---
