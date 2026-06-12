# Makemore — Study Walkthrough

Personal study of Andrej Karpathy's [makemore](https://github.com/karpathy/makemore) — a character-level language model built from scratch.

## What is Makemore?

Makemore takes a list of words and generates more words that look like them. It's a character-level language model — predicts the next character given previous characters. Starting from a simple bigram model and progressively building up to a full Transformer.

## What I Studied (Part 1 — Bigram Model)

- **Bigram model** — counting character pairs, building probability table
- **Sampling** — how to generate new names from learned probabilities
- **Loss function** — negative log likelihood, why it measures model quality
- **Neural network formulation** — same bigram model rewritten as a single linear layer
- **PyTorch basics** — tensors, one-hot encoding, softmax, gradient descent
- **Training loop** — forward pass, loss, backward, weight update

## Key Insight

A bigram model is just a lookup table — "given character A, what's the probability of character B next?" The neural network version does the exact same thing but learns it through gradient descent instead of counting. Both give the same answer — but the neural net version scales to more complex models.

## Notebook

The main notebook (`makemore_part1_bigram.ipynb`) contains:
- Full bigram implementation (counting + neural net version)
- Inline personal notes and understanding at each step
- Loss tracking and sampling examples

## Stack

- Python
- PyTorch
- Jupyter Notebook
- Following: [Karpathy's Zero to Hero — Lecture 2](https://www.youtube.com/watch?v=PaCmpygFfXo)

## Part of

This repo is part of my study series following Andrej Karpathy's [Neural Networks: Zero to Hero](https://github.com/karpathy/nn-zero-to-hero) course.

| Repo | Topic | Status |
|------|-------|--------|
| micrograd-study | Autograd engine, backprop | ✅ Done |
| makemore-study | Character-level LM series | 🔄 In progress |

### Makemore Series Progress

| Part | Topic | Status |
|------|-------|--------|
| Part 1 | Bigram model (counting + neural net) | ✅ Done |
| Part 2 | MLP — Bengio et al. 2003 | 🔄 In progress |
| Part 3 | Activations, gradients, BatchNorm | ⏳ Upcoming |
| Part 4 | Becoming a Backprop Ninja | ⏳ Upcoming |
| Part 5 | WaveNet — deeper architecture | ⏳ Upcoming |
| Part 6 | Building GPT from scratch | ⏳ Upcoming |
