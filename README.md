Transformer-based Encoder–Decoder from Scratch (PyTorch)

sidenote:I Guess this readme is not neccessary because i've explained everything in notebook, but following the tradition of adding read-me file,
i will explain the "Why" of this project here, if you are intrested to knw the "HOW" and "WHAT" then spend some time on the notebooks i've uploaded.
No need to bang your head here and there, buying expensive courses to understand Transformers, this repo is enough, after spending good amount of time on this 
repo i gurentee that you will understand Transformer in depth from begginer to advance. In your journey if you would come up with a doubt feel free to contact 
me on LinkedIn: https://www.linkedin.com/in/abraar-ahmad-820163359?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=ios_app
now let's begin


This repository is a from scratch implementation of the Transformer encoder–decoder architecture described in the paper “Attention Is All You Need”.
The goal of this project is not to use high-level abstractions, but to understand and implement every core component of the Transformer manually, using beginner-friendly and readable PyTorch code.

The repository walks through the complete pipeline:

tokenization

dataset preparation

attention mechanisms

encoder and decoder stacks

training loop

checkpointing and inference

If you have basic knowledge of neural networks, this repository is designed to take you from beginner to advanced understanding of Transformers, step by step.

Motivation

Most Transformer implementations rely heavily on libraries that hide the internal mechanics.
This project was built with the opposite philosophy:

Understand the Transformer by building it yourself.

Every major idea introduced in the original paper—self-attention, multi-head attention, positional encoding, masking, and encoder–decoder interaction—is explicitly implemented and commented in code.

Dataset Experiments & Practical Constraints

During development, multiple datasets and training environments were explored:

Initially, the OPUS Books English–Italian dataset (~33k sentence pairs) was used.

Training was attempted across multiple Google Colab sessions, but GPU usage limits were repeatedly reached.
<img width="931" height="585" alt="image" src="https://github.com/user-attachments/assets/117246b8-f74f-42d1-ab61-c292593cd067" />


Due to these limitations, the final experiments were conducted using the LingoIITGN/PHINC Hinglish–English dataset (~13k sentence pairs).

Because the Hinglish–English dataset is relatively small, the final translation quality is not state-of-the-art.
However, this is a data and hardware limitation, not a model limitation.

The same architecture, when trained on larger datasets with stronger GPUs, is capable of producing significantly better results.

The focus of this repository is architectural correctness and conceptual clarity, not leaderboard performance.

Educational Focus

This repository is intentionally written with clear, beginner-friendly code, even where more compact or optimized solutions exist.

Key design choices:

Explicit tensor operations instead of hidden abstractions

Manual construction of attention masks

Clear separation of encoder inputs, decoder inputs, and labels

Tokenization and vocabulary building shown explicitly

Training and validation logic written step-by-step

In addition to the main Transformer implementation, three additional files/notebooks are included purely for educational purposes, to help readers understand individual components in isolation.

What You Will Learn from This Repo

How raw text is converted into token indices

How self-attention works internally

Why multi-head attention is needed

How positional encoding injects order information

How encoder and decoder interact during training and inference

How masking prevents information leakage

How a full Transformer training loop is built from scratch

This repository is especially useful if:

You want to truly understand Transformers, not just use them

You are preparing for research, interviews, or advanced ML work

You want a reference implementation that mirrors the original paper closely

Final Note

This project prioritizes understanding over optimization and clarity over brevity.

If you are willing to read, run, and experiment with the code, this repository can serve as a complete learning resource for Transformers, starting from first principles and progressing to a full encoder–decoder model.
