# Lecture 04 — Knowledge

## Core Concepts

- Transformer Architecture  
- Encoder  
- Decoder  
- Tokenization  
- Token IDs  
- Vector Embeddings  
- Autoregressive Generation  
- Self-Attention Mechanism  
- Long-Range Dependencies  
- Attention Scores  
- BERT  
- GPT  
- Transformer vs LLM  

---

## Definitions

Concept: Transformer  
Definition: A deep neural network architecture introduced in 2017 that processes sequences using attention mechanisms instead of recurrence or convolution.

Concept: Encoder  
Definition: A component of the Transformer that converts input tokens into vector embeddings while capturing semantic relationships.

Concept: Decoder  
Definition: A component of the Transformer that generates output tokens using embeddings and previously generated tokens.

Concept: Tokenization  
Definition: The process of breaking text into smaller units (tokens) and assigning each a unique identifier.

Concept: Vector Embedding  
Definition: A numerical vector representation of tokens that captures semantic relationships between words.

Concept: Autoregressive Generation  
Definition: A process where a model generates output sequentially, using previously generated tokens as input for predicting the next token.

Concept: Self-Attention  
Definition: A mechanism that allows a model to assign importance weights to different tokens in a sequence when computing representations.

Concept: Long-Range Dependency  
Definition: The ability of a model to capture relationships between tokens regardless of their distance in a sequence.

Concept: BERT  
Definition: A Transformer-based model that uses only the encoder and predicts masked words using bidirectional context.

Concept: GPT  
Definition: A Transformer-based model that uses only the decoder and generates text by predicting the next word sequentially.

---

## Key Mechanisms / Processes

### Transformer Workflow

Step 1: Input text is provided  
Step 2: Text is tokenized into tokens  
Step 3: Tokens are converted into token IDs  
Step 4: Encoder converts token IDs into embeddings  
Step 5: Embeddings are passed to the decoder  
Step 6: Decoder receives embeddings + partial output  
Step 7: Decoder predicts the next word  
Step 8: Process repeats until full output is generated  

---

### Autoregressive Generation

Step 1: Model receives initial input  
Step 2: Predicts next token  
Step 3: Appends predicted token to input  
Step 4: Uses updated sequence to predict next token  
Step 5: Repeat until sequence completion  

---

### Tokenization → Embedding Pipeline

Step 1: Sentence → tokens  
Step 2: Tokens → token IDs  
Step 3: Token IDs → vector embeddings  
Step 4: Embeddings → model input  

---

## Relationships

Transformer → consists of → Encoder + Decoder  

Encoder → produces → Vector Embeddings  

Decoder → uses → Embeddings + Partial Output  

Tokenization → produces → Token IDs  

Token IDs → transformed into → Vector Embeddings  

Self-Attention → enables → Long-Range Dependency modeling  

Autoregressive Generation → depends on → Previous Outputs  

GPT → derived from → Transformer  

BERT → derived from → Transformer  

---

## Examples

### Tokenization Example

Input:  
“Fine tuning is fun for all”

Tokens:  
- Fine  
- tuning  
- is  
- fun  
- for  
- all  

---

### Embedding Example

- dog and puppy → vectors close together  
- apple and banana → vectors close together  
- football and tennis → vectors close together  

---

### Translation Example (Transformer)

Input: English sentence  

Process:
- Tokenization  
- Embedding  
- Encoder processing  
- Decoder prediction  

Output: German translation (generated one word at a time)

---

### Autoregressive Example

Partial output:  
“Das ist ein”

Next prediction:  
“Beispiel”

---

## Key Properties / Characteristics

- Transformers are deep neural networks  
- Operate on sequences using attention  
- Capture semantic meaning via embeddings  
- Use parallel processing (unlike RNNs)  
- Generate output sequentially (decoder side)  
- GPT models are decoder-only  
- BERT models are encoder-only  
- Output generation is iterative and autoregressive  

---

## Comparisons

### Transformer vs GPT

| Feature | Transformer | GPT |
|--------|------------|-----|
| Architecture | Encoder + Decoder | Decoder only |
| Use case | General sequence modeling | Text generation |
| Input processing | Full sequence | Left-to-right |

---

### BERT vs GPT

| Feature | BERT | GPT |
|--------|------|-----|
| Architecture | Encoder only | Decoder only |
| Direction | Bidirectional | Left-to-right |
| Task | Masked word prediction | Next word prediction |
| Strength | Understanding | Generation |

---

### Transformer vs LLM

| Statement | Truth |
|----------|------|
| All Transformers are LLMs | ❌ False |
| All LLMs are Transformers | ❌ False |

---

## Misconceptions

- Transformers and LLMs are not the same  
- Not all Transformers are used for language tasks  
- Not all LLMs are based on Transformers  
- GPT is not the full Transformer (only decoder)  
- Transformer was not originally designed for text generation  

---

## Dependencies

To understand Transformers, the following concepts are required:

- Neural Networks  
- Tokens and Tokenization  
- Vector Representations  
- Sequence Modeling  

To understand GPT:

- Transformer architecture  
- Decoder mechanism  
- Autoregressive generation  

To understand Self-Attention:

- Tokens  
- Context in sequences  
- Importance weighting  

---

## Key Takeaways

- Transformers are the foundation of modern LLMs  
- They use encoder-decoder architecture  
- Self-attention enables context-aware processing  
- Output is generated one token at a time  
- GPT and BERT are specialized Transformer variants  
- Transformer ≠ LLM (not interchangeable concepts)  
