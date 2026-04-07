# AI Ethics RAG System

This repository implements a **Retrieval-Augmented Generation (RAG) pipeline** to explore and answer questions on **Artificial Intelligence Ethics**. It integrates document retrieval, embeddings, and conversational reasoning to provide context-aware responses grounded in academic literature.

---

## 📑 Project Overview

- **Goal:** Build a modular RAG system that queries and explains ethical principles of AI using scholarly sources.  
- **Core Document:** *Artificial Intelligence (AI) Ethics: Ethics of AI and Ethical AI* (Siau & Wang, 2020).  
- **Workflow Tool:** [Flowise](https://flowiseai.com/) for pipeline design.  
- **Embedding Model:** Google Gemini (`gemini-embedding-001`).  
- **LLM:** Mistral (`mistral-tiny`).  
- **Vector Store:** In-memory retriever with top-k similarity search.  

---

## ⚙️ Architecture

1. **File Loader** → loads *AI Ethics.pdf*  
2. **Text Splitter** → chunks text (size = 1000, overlap = 200)  
3. **Gemini Embedding** → generates embeddings  
4. **Vector Store** → stores embeddings, retrieves top-k matches  
5. **Buffer Memory** → maintains conversation context  
6. **MistralAI** → generates responses (temperature = 0.9)  
7. **Conversational Retrieval QA Chain** → combines retriever + memory + chat model  

---




---

## 🖼️ System Screenshot

![System Screenshot](AI%20ETHICS%20RAG%20SYSTEM.png)

---

## 🧠 Example Interaction

**User:**  
`Why should we build ethical AI?`

**System Response:**  
AI should be built ethically to:  
1. Prevent harm to humans (privacy, discrimination, safety).  
2. Address moral challenges (bias, fairness, accountability).  
3. Protect human rights (freedom of speech, right to work, dignity).  
4. Mitigate misuse risks (deepfakes, fraud, surveillance).  

*(Source: Siau & Wang, 2020)*

---

## 🚀 Usage Instructions

1. Clone this repository:
   ```bash
   git clone https://github.com/Isha09-prompt
