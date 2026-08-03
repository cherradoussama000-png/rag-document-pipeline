
RAG Document Pipeline
Production-grade Retrieval-Augmented Generation (RAG) system designed to ground LLMs in private business data. The system strictly constrains the model to retrieved context, effectively eliminating hallucinations.

Architecture
The pipeline is split into two decoupled workflows:

Ingestion: Pulls files on a schedule, chunks them, embeds them using NVIDIA NeMo, and upserts the vectors into Pinecone.
Chat: Accepts a user query, retrieves the nearest matching vectors from Pinecone, and passes them as strict context to the LLM.
Tech Stack
Orchestration: n8n
LLM: OpenAI
Vector Database: Pinecone
Embeddings: NVIDIA NeMo
Text Splitter: Recursive Character
Live Demo & Architecture Diagram


<a href="https://www.loom.com/share/058e0ba56d0c4d878b956a206798a665" target="_blank">
  <img src="https://img.shields.io/badge/Demo-Click_to_Watch-CCFF00?style=for-the-badge" alt="Watch Demo" />
</a>
