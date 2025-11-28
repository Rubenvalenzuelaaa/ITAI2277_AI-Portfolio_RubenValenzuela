Phase 01 – Project Proposal

AI Course Copilot – RAG-Powered Study & Project Assistant
Course: ITAI 2277 – Artificial Intel Resource
Students: Oscar Cortez, Judith Barrios, Ruben Valenzuela Alvarado, Darnell Newman
Date: September 8, 2025

📌 Overview

This phase presents the proposal for our capstone project:
AI Course Copilot – a RAG-powered assistant designed to help students study, complete assignments, and retrieve course-aligned information with accurate citations.

The goal is to reduce confusion, improve transparency, and provide instructors with verifiable AI-generated outputs.

🧠 Problem Statement

Students often waste time searching across scattered resources, inconsistent notes, and low-quality online explanations.
This leads to:

Learning inefficiencies

Inconsistent assignment quality

Risk of plagiarism or hallucinated answers

Lack of transparency for instructors

Solution: A just-in-time AI assistant that retrieves from an approved corpus and produces source-grounded, citation-required answers.

👥 Users & Stakeholders
Primary Users

ITAI students completing labs, proposals, assignments.

Secondary Users

Instructors and TAs who need transparency and citation-based AI outputs.

Stakeholders

Department faculty

Accessibility services

Academic integrity board

📂 Data & Tools

Corpus of course docs (syllabi, rubrics, assignments, notes)

Python, Jupyter, FAISS/Chroma

Embedding models

LLM API or local model fallback

Lightweight UI (Flask/FastAPI + minimal frontend)

Governance includes allow-listed sources, version tagging, and citation rules.

🛠 Technical Approach
1. Data Ingestion & Chunking

PDF/HTML/Markdown → cleaned text → semantic chunks.

2. Indexing

FAISS/Chroma vector DB + metadata filtering.

3. Retrieval

Hybrid BM25 + dense embeddings + reranker.

4. Generation

Prompt templates enforce:

No hallucinations

Required citations

Concise structured responses

5. Evaluation

Query set testing

Precision@k

A/B prompt testing

🏗 System Architecture

Client UI → API → Retrieval (BM25 + dense) → Reranker → LLM → Answer + Citations

Includes logs, observability, and dataset version control.

⚠️ Risks & Mitigations
Risk	Mitigation
Noisy or inconsistent PDFs	Preprocessing + spot checks
API limits	Local fallback model + caching
Project scope	Weekly syncs + strict scope boundaries
Hallucinations	Force citations + reject out-of-corpus queries
🌱 Ethical Considerations

Academic integrity: enforce citations

Fairness: diverse sources, documented limitations

Privacy: no personal data ingestion

Transparency: exposed source list + reproducible queries

👥 Team Roles

Oscar Cortez: PM & Evaluation Lead

Judith Barrios: Retrieval/Indexing

Ruben Valenzuela: Data Curation & QA

Darnell Newman: Frontend & UX

📦 Deliverables

One-page project proposal

Minimal RAG demo

Integrated prototype

Final system + documentation + video demo
