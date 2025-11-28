# Phase 02 – Data Pipeline & Exploratory Data Analysis (EDA)

**Course:** ITAI 2277 – Artificial Intel Resource  
**Project:** AI Course Copilot – RAG-Powered Study & Project Assistant  
**Team Members:** Oscar Cortez, Judith Barrios, Ruben Valenzuela Alvarado, Darnell Newman  

---

## 📘 Overview
This phase focused on building the complete **data pipeline** for the RAG-based AI Course Copilot.  
The work includes data collection, preprocessing, chunking, embedding generation, dataset organization, and exploratory data analysis.

The goal was to create a clean, well-structured dataset suitable for semantic retrieval and later integration in Phase 03 (Working AI Model).

---

## 🗂️ Phase Deliverables
### ✔ 1. Data Report (Uploaded as DOCX)
A detailed written report describing:

- Data sources  
- Collection strategy  
- Cleaning and preprocessing steps  
- Feature engineering  
- Chunking and embedding pipeline  
- Exploratory visualizations  
- Insights and observations  

👉 **File:** `Phase02_Data_Pipeline_and_EDA.docx`

---

## 🔍 Week 4 – Data Collection & Organization

### **Data Sources**
We collected only instructor-approved and publicly available materials:
- Course syllabi  
- Assignment instructions  
- Rubrics  
- Project guidelines  
- Public AI/ML references  

### **Collection Methods**
- Manual review of course files  
- Automated extraction using:
  - **PyPDF2** (PDF parsing)
  - **BeautifulSoup / Requests** (web scraping)
- Metadata assigned to each file (course, week, topic)

### **Dataset Structure**   
data/
├── raw/ # Original documents
├── processed/ # Clean & normalized text
├── embeddings/ # Vector embeddings
└── metadata.json # Metadata for indexing

We follow strict ethical guidelines:
- No personal student data  
- No copyrighted material  
- Only allow-listed files  

---

## 🔧 Week 5 – Preprocessing & Feature Engineering

### **Preprocessing Steps**
- Remove headers, footers, noise  
- Normalize whitespace  
- Fix encoding  
- Convert text to UTF-8  
- Remove duplicates  

### **Chunking Strategy**
- 300–500 token segments  
- Each chunk receives metadata:
  - Course name  
  - Topic  
  - Document type  
  - Week number  

### **Embedding Generation**
Models used:
- **SentenceTransformers**  
- **OpenAI text-embedding models**  

Pipeline:
clean_text → chunk → embed → store_in_vectorDB

### **Dataset Split**
Created:
- Training set  
- Validation set  
- Test set  

To benchmark retrieval performance before Phase 03.

---

## 📊 Week 6 – Exploratory Data Analysis (EDA)

### **Statistical Findings**
- Average document size  
- Distribution of chunk lengths  
- Keyword frequency (`AI`, `ethics`, `retrieval`, etc.)  

### **Visualizations**
Generated using Matplotlib:
- Histogram of document tokens  
- Word cloud  
- Bar chart of document counts per week  

### **Insights**
- Some rubric and instruction files contain overlapping text → cleaned via semantic deduplication  
- Ethics/policy documents are high-value data for accurate retrieval  
- Balanced indexing improves RAG answer quality  

---

## 🧩 Phase Insights
- Clean, consistent text drastically improves embedding quality  
- Organized metadata structure ensures reliable vector search  
- EDA revealed imbalances across course weeks → corrected in indexing  
- Prepared all assets for Phase 03 model training and validation  

---

## 📦 Included in This Folder
- **Phase02_Report.docx**  
- `README.md` (this file)

---

## 🔗 Next Steps
Phase 03 will incorporate:
- Chunked & embedded dataset  
- Retrieval benchmarking (BM25 vs RAG)  
- Full working model for the AI Course Copilot  

---
