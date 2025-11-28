# Phase 03 – Working AI Model

This phase documents the development, evaluation, and optimization of the retrieval-augmented AI model  
used for the **AI Course Copilot – RAG-Powered Study & Project Assistant**.

## 📌 Objectives
- Build and test the RAG (Retrieval-Augmented Generation) pipeline.
- Compare BM25, dense embeddings, and hybrid retrieval methods.
- Improve chunking, preprocessing, and semantic indexing.
- Evaluate accuracy, relevance, and citation reliability.
- Run experiments and refine model performance.

## 📁 Contents
- **Phase 03.docx** – Full technical report for the model development phase.
- Embedding scripts (SentenceTransformers)
- Chunking & cleaning utilities
- FAISS or ChromaDB index files
- Evaluation notebooks
- Error analysis logs and experiment results

## 🧠 Key Work Completed
- Constructed a hybrid retrieval pipeline using BM25 + dense vectors.
- Designed a reranking layer using cross-encoder scoring.
- Tuned chunk sizes, overlap, and embedding strategies.
- Performed evaluation using **Precision@5, Recall@10, MRR, ROUGE-L, BERTScore**, etc.
- Reduced hallucination using improved instructions + grounding techniques.
- Achieved significantly better results than baseline retrieval.

## ✅ Outcome
A reliable, optimized, and high-accuracy RAG model  
that forms the core intelligence of the **AI Course Copilot** system.
