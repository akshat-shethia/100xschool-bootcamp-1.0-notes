<div align="center">

# 📚 100x AI & Machine Learning
### *The Ultimate Understanding-First Collection*

[![License](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Status](https://img.shields.io/badge/Status-Active-success.svg)]()
[![AI Augmented](https://img.shields.io/badge/AI-Augmented-purple.svg)]()
[![PDF Ready](https://img.shields.io/badge/Format-PDF%20%26%20Markdown-c0392b.svg)]()

*A comprehensive, deep-dive collection of notes from the 100xDevs AI Cohort, refined for clarity, depth, and intuition.*

[**Explore the Notes**](#-modules--curriculum) · [**Download PDFs**](#-how-to-use)

---

</div>

<br>

## 🌟 About This Repository

Welcome to the definitive artifact of my journey through the **100xDevs AI & Machine Learning Cohort**. 

This repository is not just a dump of class notes. It is a **curated, "understanding-first" knowledge base**. 

I have taken the original class materials and Colab notebooks and **heavily augmented them** using advanced AI models. My goal was simple: **to bridge the gap between "knowing" and "understanding."**

### 🧠 Why This Exists (The "Ultrathink" Philosophy)

Class lectures are amazing, but sometimes complex mathematical concepts or architectural decisions need a different angle to click. 
*   **Personal Struggles:** Whenever I found a point hard to understand (like *Backpropagation calculus* or *Tokenization boundaries*), I didn't just skip it.
*   **Deep Reasoning:** I used AI to reason deeply ("ultrathink") about these topics, breaking them down into first principles.
*   **Intuition Over Rote:** These notes prioritize **mental models**, **analogies**, and **visual explanations** over dry academic text.

If you want to not just *run* code but *feel* how the data flows through a Transformer, these notes are for you.

---

## ✨ Key Features

| Feature | Description |
|:---|:---|
| **🤖 AI-Augmented Explanations** | Heavy use of AI to simplify complex topics, generate better analogies, and expand on "why" things work the way they do. |
| **📉 Visual & Intuitive** | Replaced heavy jargon with clear diagrams, tables, and step-by-step visualizations of data flow. |
| **📄 PDF Optimized** | All READMEs have been rigorously formatted to convert perfectly into **PDFs**. Download them, put them on your iPad/Kindle, and study offline. |
| **🧪 "From Scratch" Focus** | Emphasis on building things manually (like Neural Nets in NumPy) before using frameworks (PyTorch), ensuring deep foundational knowledge. |

---

## 📚 Modules & Curriculum

This repository is organized chronologically, mirroring the cohort's progression.

### 🔹 **Week 01: Foundations of Intelligence**
> *From the History of AI to the Modern LLM Boom*
- **Core Topics:** History of AI Winters, What is Intelligence?, The "Black Box" of LLMs.
- **Key Insight:** Understanding how we moved from Rule-Based Systems (Expert Systems) to Probabilistic Learning.
- **Reference:** `(Week 01) 17-01-2026`

### 🔹 **Week 02: Neural Networks from Scratch**
> *The Mathematics of Learning*
- **Core Topics:** The Perceptron, The XOR Problem, Backpropagation (Deriving the Chain Rule), Gradient Descent.
- **Key Insight:** Manually coding a Neural Network in pure NumPy to solve logic gates. Understanding *why* non-linearity (Activation Functions) is the secret sauce of Deep Learning.
- **Reference:** `(Week 02) 24-01-2026`

### 🔹 **Week 03 & 04: The Transformer Architecture**
> *How Machines "Read" and "Understand"*
- **Core Topics:** Tokenization (BPE), Word Embeddings (Word2Vec/GloVe), Semantic Vector Space, Positional Encodings.
- **Key Insight:** Tracing the journey of a sentence from raw text to numerical vectors. Why "Strawberry" has 3 Rs but models can't count them. Visualizing 768-dimensional semantic space.
- **Reference:** `(Week 03) 31-01-2026` & `(Week 04) 07-02-2026`

### 🔹 **Week 05: The Deep Learning Engine**
> *The Math & Tools: Scalars, Vectors, Matrices, Tensors & PyTorch*
- **Core Topics:** The Data Hierarchy (Scalar → Vector → Matrix → Tensor), Matrix Transformations, Matrix Multiplication (the universal engine), CPU vs. GPU parallelism, PyTorch Autograd, `nn.Module`, and the full Training Loop.
- **Key Insight:** Every operation in Deep Learning — from a single neuron to Self-Attention — is secretly just a Matrix Multiplication. Seeing how `.backward()` automates the calculus that was done by hand in Week 02.
- **Reference:** `(Week 05) 14-02-2026`

### 🔹 **Week 06: Building & Training a Modern LLM**
> *What Changed Since 2017 — and Why*
- **Core Topics:** The Classic vs. Modern Transformer stack; the four architectural upgrades: **RMSNorm (Pre-Norm)**, **SwiGLU** activation, **RoPE** positional encoding, and **Grouped Query Attention (GQA)**. KV Cache mechanics, time/space complexity of attention, and the DeepSeek MLA spotlight.
- **Key Insight:** Modern LLMs (LLaMA, Mistral, Gemma) aren't a new invention — they are the 2017 Transformer with four surgical engineering patches applied to fix training instability, memory walls, and poor generalization at scale.
- **Reference:** `(Week 06) 21-02-2026`

### 🔹 **Week 07: MiniLLM — Every Modern Component From Scratch**
> *Theory → PyTorch: Building and Training a Decoder-Only LLM*
- **Core Topics:** Full implementation of `RMSNorm`, `RoPE` (precompute + apply), `GroupedQueryAttention` (with `repeat_kv`), `SwiGLU` FFN, and the complete `TransformerBlock` / `MiniLLM` pipeline. Character-level tokenization, autoregressive training loop, gradient clipping, loss analysis, and temperature-controlled generation.
- **Key Insight:** A 2.7M-parameter character-level model (`MiniLLM`) trained on Tiny Shakespeare to a final train loss of **1.02** in ~11 min on a Tesla T4 — demonstrating that the **architecture** of a modern 70B LLaMA is identical; only the *scale* differs. Classic overfitting curve (train↓, val↑ after step 1500) was observed firsthand, making regularization intuition concrete.
- **Reference:** `(Week 07) 27-02-2026`

### 🔹 **Week 08: From API Calls to Autonomous Agents**
> *First Principles of the ReAct Pattern & Autonomous AI*
- **Core Topics:** OpenRouter API setup, temperature & the stateless memory illusion, function calling (JSON schema → `tool_calls`), the **ReAct loop** (`THOUGHT → ACTION → OBSERVATION`), building a from-scratch ReAct agent (~60 lines), the Code Agent (file I/O + Python execution), native function calling vs. string parsing, and the "Gotchas" (context window explosion, hallucination spirals, `tk/s` as the key agent metric).
- **Key Insight:** An Agent = **LLM + Tools + Loop** — and there is no magic. The same ~60-line Python pattern underlies Claude Code and Codex. The defining engineering challenge is the **Context Engineering Problem**: every ReAct iteration re-sends the *entire* conversation history, so prompt tokens compound from ~266 → 580 → 1200+ per iteration, making context compression strategies (RAG, summarization, sliding window) essential.
- **Reference:** `(Week 08) 07-03-2026`

### 🔹 **Week 09: Retrieval-Augmented Generation (RAG)**
> *Build it. Break it. Fix it. — From First Principles to Production Pipelines*
- **Core Topics:** The RAG Workflow (Retrieve-Augment-Generate), Recursive Chunking, Contextual Retrieval (Anthropic), Hybrid Search (BM25 + RRF), and the two-pass Reranking system.
- **Key Insight:** LLMs are reasoning engines, not databases. RAG is the bridge that feeds them fresh, private knowledge without the unreliability of fine-tuning. Moving from "Naive RAG" to "Production RAG" requires balancing recall (Hybrid Search) with precision (Reranking).
- **Reference:** `(Week 09) 13-03-2026`

### 🔹 **Week 10: Why RAG Breaks & What Comes Next**
> *Context Rot, Production Reality, and the Evolution of Retrieval Systems*
- **Core Topics:** Context Rot (Attention Budget), The Distractors Problem (Needle in a Haystack), Surgical Context Engineering (The ChatGPT Memory Model), and the Vectorless Frontier (PageIndex).
- **Key Insight:** Similarity $\neq$ Relevance. Large context windows introduce "Context Rot" where models lose signal in noise. The future is shifting from passive similarity search to active, reasoning-based navigation (PageIndex) and "Context Engineering" where we surgically control exactly what the model sees.
- **Reference:** `(Week 10) 23-03-2026`


---

## 🛠️ How to Use

1.  **Offline Study:** Look for the **PDF versions** in each directory. These are perfect for highlighting and annotating on tablets.

---

## ❤️ Credits & Acknowledgment

This work is heavily inspired by the teaching of **Rishabh**, **Harkirat Singh** and the **100xDevs** community. 

*   **Original Material:** 100xDevs AI Cohort
*   **Curated & Enhanced by:** [Akshat Shethia](https://www.linkedin.com/in/akshhat-shethia/)
*   **Powered by:** Human curiosity + Artificial Intelligence

---

<div align="center">

**"You don't truly understand something unless you can explain it to a simpleton."**  
*— (Often attributed to Einstein, but the spirit remains)*

🌟 **Star this repo if you found these notes helpful!** 🌟

</div>
