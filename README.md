# langchain-rag-pipeline
# LangChain RAG Document Question Answering

A Retrieval-Augmented Generation (RAG) system built with Python and LangChain that answers questions using information retrieved from a research document.

## Project Overview

This project demonstrates a complete RAG pipeline using a research paper as the knowledge source.

The system:

1. Loads a PDF document
2. Splits the document into smaller chunks
3. Converts chunks into numerical embeddings
4. Stores embeddings in a FAISS vector database
5. Retrieves relevant chunks based on a user's question
6. Passes the retrieved context to Google Gemini
7. Generates an answer based on the retrieved document content

## RAG Pipeline

```text
PDF Document
     ↓
PyMuPDFLoader
     ↓
Document Chunking
     ↓
Hugging Face Embeddings
     ↓
FAISS Vector Database
     ↓
Similarity Search / Retriever
     ↓
Relevant Context
     ↓
Google Gemini
     ↓
Final Answer