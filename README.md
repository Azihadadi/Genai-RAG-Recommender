# GenAI-RAG-Recommender

**An Enhanced Retrieval-Augmented Generation (RAG) System for Food Recommendations**  
*Powered by IBM watsonx.ai Granite LLM + ChromaDB + Sentence Transformers*

---

## Overview
This repository demonstrates an **end-to-end GenAI-powered recommendation system** that integrates **vector similarity search** with **large language model reasoning** to provide **contextual**, **personalized food recommendations**.

The system combines:

- **Vector databases (ChromaDB)** for similarity search and metadata filtering

- **Sentence Transformers** for semantic embeddings

- **IBM watsonx.ai Granite LLM** for natural language understanding and conversational responses

- **RAG pipeline** that grounds LLM outputs with structured food data

While the application domain here is food & nutrition, the architecture is **domain-agnostic** and can be directly adapted to other verticals such as **healthcare**, **e-commerce**, or **knowledge management**

---
## Features
- Vector similarity search over structured JSON data (ingredients, calories, taste profiles)  
- Retrieval-Augmented Generation (LLM responses grounded in retrieved context)  
- Conversational chatbot (CLI interface with smart comparison mode)  
- Explainability: shows similarity scores and metadata alongside recommendations  

---

## Structure
```
genai-rag-recommender/
│
├── data/ 
│ ├──FoodDataSet.json # Sample dataset for demo
├── enhanced_rag_chatbot.py # Main chatbot (IBM Granite + RAG)
├── shared_functions.py # Utility functions (ChromaDB, embeddings, search)│ 
├── requirements.txt # Python dependencies
└── README.md # Project overview and documentation
```

---

## Quickstart

### 1. Clone & Install
```bash
git clone https://github.com/Azihadadi/genai-rag-recommender.git
cd genai-rag-recommender
pip install -r requirements.txt
```


### 2. Configure IBM watsonx.ai credentials
Update the following section in enhanced_rag_chatbot.py with your credentials:
```bash
my_credentials = {
    "url": "https://us-south.ml.cloud.ibm.com"
}
project_id = "skills-network"
```
### 3. Run chatbot
```bash
python enhanced_rag_chatbot.py
```

## Tech Stack

- `Python 3.10+`
- IBM watsonx.ai Granite Instruct Models
- ChromaDB (cosine similarity, HNSW)
- Sentence Transformers (all-MiniLM-L6-v2)
- Numpy/ Scipy
---
