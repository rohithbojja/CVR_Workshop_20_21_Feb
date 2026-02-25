# LLMs From Scratch for Teens (Complete PPT Deck Content)

This file is a complete **ready-to-paste** deck outline for PowerPoint/Google Slides.

## Slide 1 — Title
**Build a Large Language Model (LLM) From Scratch**  
A beginner workshop for ages 15+

---

## Slide 2 — Today’s Mission
- Understand how LLMs work internally
- Build each key part in simple steps
- Train a tiny GPT-style model
- Generate text from your own model

---

## Slide 3 — What is an LLM?
- A model that predicts the next token
- Learns patterns from huge text datasets
- Can answer questions, summarize, and write text

---

## Slide 4 — Text becomes numbers
Pipeline:
1. Raw text
2. Tokenization
3. Token IDs
4. Embedding vectors

Example: "I love AI" -> ["I", "love", "AI"] -> [12, 47, 6]

---

## Slide 5 — Math you need (only 4 ideas)
- Vector
- Matrix
- Dot product
- Softmax

These are the core operations behind attention.

---

## Slide 6 — Embeddings
- Embedding = learned vector for each token
- Similar words end up with similar vectors
- Converts symbolic text into continuous math space

---

## Slide 7 — Why position matters
- Attention alone does not know token order
- Add positional embeddings to encode location
- "dog bites man" != "man bites dog"

---

## Slide 8 — Attention intuition
Each token asks:
- What am I looking for? (**Query**)
- What does every other token offer? (**Key**)
- What info should I take from them? (**Value**)

---

## Slide 9 — Attention formula
`Attention(Q, K, V) = softmax(QK^T / sqrt(d_k))V`

- `QK^T` = similarity scores
- `softmax` = convert to probabilities
- weighted sum of `V` = context-aware output

---

## Slide 10 — Multi-head attention
- Run attention multiple times in parallel
- Each head learns a different relationship
- Concatenate and project outputs

---

## Slide 11 — Transformer block
A block contains:
1. Multi-head attention
2. Residual + LayerNorm
3. Feed-forward network (MLP)
4. Residual + LayerNorm

---

## Slide 12 — GPT architecture
- Token + positional embeddings
- Stack of transformer blocks
- Final linear layer to vocab logits
- Softmax gives next-token probabilities

---

## Slide 13 — Causal mask
- GPT should not look at future tokens while training
- Causal mask hides right-side tokens
- Prevents cheating

---

## Slide 14 — Training objective
- Task: next-token prediction
- Loss: cross-entropy
- Optimizer: AdamW
- Iterate for many batches/epochs

---

## Slide 15 — Generation loop
1. Start with prompt tokens
2. Predict next token
3. Append token
4. Repeat

Optional controls: temperature, top-k, top-p

---

## Slide 16 — Evaluation basics
- Training loss
- Validation loss
- Perplexity
- Manual quality checks

---

## Slide 17 — Common failure modes
- Hallucinations (confident wrong outputs)
- Bias from data
- Toxic or unsafe generations

---

## Slide 18 — Responsible AI checklist
- Curate data carefully
- Add filters and safety checks
- Human review for sensitive use cases
- Monitor model behavior continuously

---

## Slide 19 — Hands-on project ideas
- Tiny story generator
- Subject-specific Q&A bot
- Song lyric style model

---

## Slide 20 — Build roadmap (after class)
1. Improve tokenizer (BPE)
2. Add train/validation split
3. Track metrics in plots
4. Increase model size slowly
5. Experiment with real datasets

---

## Slide 21 — Recap
- You now understand LLM internals
- You built a mini GPT pipeline
- You can continue toward stronger models

---

## Slide 22 — Live Visualization Demo Plan
- Demo 1: Softmax temperature bars
- Demo 2: Attention heatmap with token labels
- Demo 3: Causal mask matrix
- Demo 4: Training loss curve

---

## Slide 23 — Interactive Knobs Students Can Control
- Temperature (creativity)
- Top-k (vocabulary filtering)
- Training steps (loss trend)
- Sequence length (context size)

---

## Slide 24 — Step-by-Step Lab Flow
1. Predict outcome
2. Run cell
3. Change one variable
4. Re-run and compare
5. Explain result in one sentence

---

## Slide 25 — Final Build Challenge
- Customize one visualization
- Improve one model component
- Present before/after result
- Explain what changed and why

