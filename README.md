---
title: DocuGraph AI
emoji: 📄
colorFrom: gray
colorTo: blue
sdk: static
pinned: false
---

# DocuGraph AI — RAG Context & Chunking Diagnostics Workbench

An interactive diagnostics workbench designed for AI engineers to simulate, evaluate, and optimize document partitioning strategies for Retrieval-Augmented Generation (RAG) pipelines.

---

## Overview

In production RAG workflows, chunk boundary selection directly impacts dense retrieval accuracy. Suboptimal chunking causes context fragmentation, lost entity co-references, and token dilution. 

**DocuGraph AI** runs client-side partitioning algorithms coupled with generative validation via the Gemini API to assess semantic integrity before documents reach vector databases.

---

## Key Features

- **Configurable Partition Strategies:**
  - *Fixed Character Chunking* with customizable sliding window overlap.
  - *Recursive Paragraph Splitting* aligned to document structural boundaries.
- **Real-Time Distribution Metrics:**
  - Immediate computation of total segment count, average chunk length, and window overlap ratio.
- **Generative Context Auditing (Gemini API):**
  - **Coherence Scoring (1–10):** Evaluates semantic completeness and self-containment.
  - **Boundary Loss Detection:** Flags truncated facts, missing antecedents, or fragmented statements.
  - **Synthetic Retrieval Queries:** Synthesizes realistic evaluation questions per chunk to test embedding retrieval accuracy.
- **Zero-Backend Architecture:** Executes entirely in the browser using static Web APIs; API credentials remain stored locally in `localStorage`.
- **Structured Audit Export:** Generates standardized JSON reports for integration with offline benchmarking workflows.

---

## Technical Stack

- **Frontend Engine:** HTML5, Modern CSS (Design System / Dark Theme), Vanilla JavaScript (ES6+)
- **LLM Integration:** Google Generative AI (Gemini 2.5 Flash via REST API)
- **Deployment Target:** Hugging Face Spaces (Static SDK) / GitHub Pages / Vercel

---

## Quickstart

1. Clone or open the repository.
2. Launch `index.html` in any modern web browser or visit the hosted Hugging Face Space.
3. (Optional) Provide your Gemini API key in the configuration bar to enable generative semantic auditing.
4. Paste reference documentation or click **Load Benchmark Text**.
5. Select a partitioning strategy and click **Generate Chunks**.
6. Click **Run Semantic Quality Audit**