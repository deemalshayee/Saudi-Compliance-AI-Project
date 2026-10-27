# Saudi Compliance AI 🇸🇦

An Arabic Retrieval-Augmented Generation (RAG) system designed to answer questions about Saudi labor regulations using relevant legal documents and source-based citations.

## Overview

Saudi Compliance AI helps users find relevant information in Saudi labor regulations by retrieving relevant legal articles and using a locally hosted language model to generate grounded Arabic answers.

The system uses a hybrid retrieval approach that combines semantic similarity with keyword matching to identify relevant legal provisions.

## Key Features

- **Arabic Legal Document Processing:** Structures legal articles while preserving article numbers, source types, page references, and related provisions.
- **Hybrid Retrieval:** Combines semantic search and keyword matching to retrieve relevant legal content.
- **Semantic Search:** Uses multilingual sentence embeddings and FAISS for efficient similarity search.
- **Local LLM Integration:** Uses Gemma 3 12B to generate answers based on retrieved legal context.
- **Source-Aware Citations:** Identifies the relevant regulation and article in generated answers.
- **Confidence-Based Rejection:** Rejects questions when the retrieved context is insufficient to provide a reliable answer.
- **Evaluation:** Tests the system on questions about maternity leave, probation, overtime, breastfeeding breaks, disability, and other labor-related topics.

## Legal Sources

The system processes three categories of Saudi labor regulations:

1. Saudi Labor Law
2. Executive Regulations of the Labor Law
3. Unified Model of Workplace Regulations

## Technology Stack

- Python
- Jupyter Notebook
- Sentence-Transformers
- Multilingual sentence embeddings
- FAISS
- Gemma 3 12B (GGUF)
- Retrieval-Augmented Generation (RAG)
- Natural Language Processing (NLP)

## How It Works

1. **Document Processing:** Extracts and structures legal articles from regulatory documents.
2. **Chunking:** Organizes legal content into retrievable text chunks while preserving source metadata.
3. **Embedding Generation:** Converts text chunks into multilingual vector embeddings.
4. **Hybrid Retrieval:** Combines semantic similarity and keyword matching to find relevant provisions.
5. **Answer Generation:** Supplies retrieved context to Gemma 3 12B to generate an Arabic response.
6. **Source Attribution:** Includes the relevant legal source and article in the answer.
7. **Evaluation:** Tests retrieval and answer generation using representative questions.

## Project Structure

```text
Saudi-Compliance-AI/
├── data/
│   └── processed/
├── notebooks/
│   ├── rag_development.ipynb
│   └── rag_development_clean.ipynb
├── src/
├── tests/
└── .gitignore
```

## Running the Project

The
