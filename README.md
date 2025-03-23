# Document Management and RAG-based Q&A Application 🚀
**Overview**
This repository contains a scalable backend system for Document Management and Retrieval-Augmented Generation (RAG) Q&A, built using Python, PostgreSQL, and RabbitMQ.

The system allows users to:
✅ Ingest documents and generate embeddings using an LLM-based model.
✅ Retrieve relevant documents for Q&A using TF-IDF, BM25, or vector search.
✅ Generate answers using RAG (Retrieval-Augmented Generation).
✅ Queue tasks asynchronously using RabbitMQ for efficient processing.
🎯 Features
✅ API Endpoints

POST /documents – Upload document data, generate embeddings, and store them in PostgreSQL.

POST /ask – Accepts a question, retrieves relevant documents, and generates an answer using RAG.

GET /documents – Lists all uploaded documents.

POST /select-documents – Allows users to specify documents for RAG-based Q&A.

✅ Data Storage
PostgreSQL is used to store document metadata, embeddings, and processed text.

pgvector is used for efficient vector similarity search in PostgreSQL.

✅ Embedding & Retrieval Mechanisms
Uses LLM-based embeddings (Ollama Llama, OpenAI, or Hugging Face models).

Supports TF-IDF, BM25, and vector similarity retrieval.

✅ Asynchronous Processing with RabbitMQ
Document ingestion and embedding generation are processed asynchronously.

RabbitMQ queues document ingestion tasks to optimize performance.

✅ Enhanced Logging & Error Handling
Structured Logging for tracking API requests & background tasks.

Retries & Dead-letter Queues (DLQ) for handling failures in document processing.

**🛠 Tech Stack**
Component	Technology Used
Backend	Python (FastAPI / Flask)
Database	PostgreSQL (with pgvector)
Message Queue	RabbitMQ
Embedding Models	OpenAI API, Hugging Face Transformers, LangChain
Retrieval Algorithms	TF-IDF, BM25, Vector Similarity Search
Logging	Python Logging Module
Testing	Pytest
Containerization	Docker
Version Control	Git


**📐 System Architecture**
✅ Modular Design – Separate services for APIs, tasks, caching, and logging.
✅ Scalability – Supports large-scale document processing and retrieval.
✅ Transactional Consistency – Ensures synchronization across DB, cache, and message queue.


**📌 Future Enhancements**
Integrate FAISS for optimized vector search.

Deploy on AWS/GCP with managed PostgreSQL & RabbitMQ.

Implement a front-end UI for interactive document management and Q&A.
💡 Contributions are welcome! Feel free to fork, improve, and submit PRs. 🚀


## 🖼 Sample Images
![image](https://github.com/user-attachments/assets/d11d071b-b373-462f-8ab6-55cd4da58bec)
![image](https://github.com/user-attachments/assets/7f9324ed-7c96-4a37-a484-87c00273ca43)
![image](https://github.com/user-attachments/assets/ee387730-8788-4ee7-ac4c-7829f3de6e64)






