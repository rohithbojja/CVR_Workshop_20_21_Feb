# Speaker Notes — LLM From Scratch (Teen-Friendly)

Use this with `LLM_From_Scratch_Teen_Friendly_PPT_Content.md` to teach confidently.

## Teaching style
- Keep explanations short and visual.
- Ask one question every 2–3 slides.
- Alternate theory and demo frequently.

## Time plan (90–120 min)
- Slides 1–6: 25 min (foundations)
- Slides 7–13: 35 min (attention + transformer)
- Slides 14–16: 20 min (training + evaluation)
- Slides 17–21: 15 min (safety + roadmap + recap)

## Suggested prompts
- "If text is words, why turn it into numbers?"
- "What does attention really measure?"
- "Why must GPT hide future tokens?"

## Interactive checkpoints
- After slide 5: quick dot-product mini quiz
- After slide 9: students explain Q/K/V in their own words
- After slide 14: identify input/target pairs for next-token prediction

## Demo moments
1. Tokenization demo from notebook
2. Attention weight matrix shape demo
3. Tiny training loop loss decreasing
4. Generation demo with random prompt

## Common confusion and fixes
- **Confusion**: "Embeddings are just lookup tables?"
  - **Fix**: Yes, but learned during training, so meaning emerges.
- **Confusion**: "Why divide by sqrt(d_k)?"
  - **Fix**: Keeps scores stable as vector size grows.
- **Confusion**: "Does model understand like humans?"
  - **Fix**: It learns statistical patterns, not human consciousness.

## Exit ticket (5 min)
Ask each student to answer:
1. What is one role of attention?
2. What does cross-entropy do in training?
3. Name one AI safety risk.


## Visualization-first teaching sequence
- Start each concept with a plot/heatmap before formula details.
- Ask students to predict the plot shape before running cells.
- Keep one “control variable” at a time to avoid confusion.

## Interactive lab protocol (repeatable)
1. Baseline run (default values)
2. Modify exactly one variable
3. Re-run and observe differences
4. Write a one-line explanation

## Recommended variable changes
- Softmax temperature: 2.0 -> 1.0 -> 0.5 -> 0.2
- Top-k: None -> 50 -> 20 -> 5
- Training steps: 20 -> 50 -> 100
- Sequence length: 8 -> 16 -> 32


## Running the HTML visual lab
- Open `LLM_From_Scratch_Deep_Interactive_Visualizer.html` directly in the browser.
- Use tab order: Math -> Tokenization -> Embeddings -> Attention -> Causal Mask -> Sampling.
- For each tab, ask students to change one control and explain what changed.

