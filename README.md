# DocuGraph AI — RAG Ingestion & Context Engineering Workbench

DocuGraph AI is an interactive diagnostic platform designed for AI and Search Engineers to simulate, visualize, and benchmark document chunking strategies before ingestion into vector databases.

## Problem Statement
In production Retrieval-Augmented Generation (RAG) pipelines, arbitrary text partitioning leads to boundary context loss, fragmented entity co-references, and token dilution. DocuGraph addresses this by profiling chunk coherence and generating synthetic test queries.

## Features
- **Configurable Chunking Algorithms:**
  - *Fixed-Character Window:* Sliding window with dynamic character overlap configuration.
  - *Recursive Paragraph Splitting:* Structural splitting preserving semantic section integrity.
- **Real-Time Distribution Analytics:** Computes total segments, average character volume, and overlap ratio dynamically.
- **Generative Quality Audit (Gemini 3.8 Flash):**
  - **Coherence Scoring (1–10):** Assesses semantic completeness and self-containment.
  - **Boundary Loss Detection:** Identifies cut-off assertions and broken relational statements.
  - **Synthetic Retrieval Queries:** Synthesizes realistic evaluation questions to validate dense embedding retrieval quality.
- **Benchmarking Export:** Exports chunk distributions and audit metrics to standardized JSON format.

## Tech Stack
- Vanilla JavaScript (ES6+), HTML5, CSS3 Design System
- Google Generative AI (Gemini 3.8 Flash)
- Hosted on Hugging Face Spaces

## Live Demo
[DocuGraph AI Live Space](https://huggingface.co/spaces/YOUR_USERNAME/docugraph-ai)
