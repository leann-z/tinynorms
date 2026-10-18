# TinyNorms

Curriculum order and the geometry of alignment in tiny language models.

> Work in progress. The training and analysis scaffolding is built. Experiments haven't been run yet.

Tiny models are small enough to train from scratch many times, which makes it possible to control exactly when a model learns a behavioural norm and then compare the resulting weights directly. This project uses that to ask two questions:

- **Does curriculum order matter?** Are norms introduced early in training harder to fine-tune away than norms introduced late?
- **Where does a norm live?** Treating a learned norm as a task vector, is it localised to certain layers, low-rank, or roughly linear (addable, composable, negatable)?

## Setup

- Small nanoGPT-style models
- A simple base corpus mixed with synthetic, LLM-generated norm data
- A curriculum mixer that schedules norm data early, late, or interleaved
- Evals for norm adherence, robustness to adversarial fine-tuning, and general LM quality
- Weight-space analysis: per-layer task-vector magnitude, cosine similarity, effective rank, interpolation

## Progress

- [x] Scaffold: curriculum mixer, training loop, evals, weight-space library, CPU smoke test
- [ ] Generate norm dataset
- [ ] Curriculum sweeps
- [ ] Robustness and weight-space analysis
