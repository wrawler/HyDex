# Hybrid Knowledge Retrieval Engine (Pokémon Knowledge Base)

[![Status](https://img.shields.io/badge/Status-In%20Active%20Development-blue)]()
[![Python](https://img.shields.io/badge/Python-3.11-brightgreen)]()

A hybrid Retrieval-Augmented Generation (RAG) system engineered to resolve gameplay mechanics and deterministic entity statistics with zero numeric hallucination.

---

## 🎯 Architecture & Approach

Standard semantic vector search struggles with deterministic lookups (e.g., exact base stats, damage calculations, and evolution thresholds). This engine decouples queries across two pathways:
1. **Semantic Vector Search (FAISS + Sentence-Transformers):** Resolves unstructured qualitative strategy questions from preprocessed GameFAQs guides.
2. **Structured Relational Querying (PokeAPI / REST):** Routes deterministic numeric inquiries to verified structured endpoints.

---

## 🛠️ Pipeline Design

1. **Ingestion & ETL:** Parsing and normalizing semi-structured plaintext walkthrough guides while preserving section hierarchies and metadata.
2. **Embedding & Vector Storage:** Chunking normalized text and generating dense vector embeddings stored in a local FAISS index.
3. **Retrieval & Verification:** Context routing and structured JSON-schema validation to eliminate hallucinations.

---

## 🗺️ Implementation Roadmap

- [x] Architecture design & data source identification (GameFAQs plain text, PokeAPI)
- [ ] ETL parser for semi-structured ASCII text normalization
- [ ] Embedding generation and FAISS vector indexing pipeline
- [ ] Hybrid query router & response generation
- [ ] Benchmark latency and retrieval recall

---

## 📦 Stack
* **Language:** Python 3.11
* **Vector Index:** FAISS
* **Embeddings:** Sentence-Transformers
* **Protocols:** REST APIs, JSON-Schema
