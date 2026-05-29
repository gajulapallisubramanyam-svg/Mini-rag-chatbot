# Mini RAG Chatbot

## Overview

This project implements a simple Retrieval-Augmented Generation (RAG) chatbot using Python, LangChain, FAISS, Hugging Face Embeddings, and Transformers. The chatbot can answer user questions based on the content of a PDF document by retrieving relevant information and generating context-aware responses.

## Objective

The objective of this project is to build a complete RAG pipeline that:

* Reads a PDF document
* Extracts text from the PDF
* Splits the text into chunks
* Generates vector embeddings
* Stores embeddings in a FAISS vector database
* Performs semantic search
* Retrieves relevant context
* Uses an LLM to generate answers

## Technologies Used

* Python
* Jupyter Notebook
* LangChain
* FAISS
* Hugging Face Embeddings
* Sentence Transformers
* Transformers
* PyPDFLoader

## Project Structure

```text
mini-rag-chatbot/
│
├── Mini_RAG_Chatbot.ipynb
├── README.md
├── requirements.txt
│
├── sample_data/
│   └── MachineLearningTomMitchell.pdf
│
└── screenshots/
```

## RAG Pipeline

### 1. Document Loading

The PDF document is loaded using PyPDFLoader.

### 2. Text Extraction

Text is extracted from all pages of the PDF.

### 3. Text Chunking

The extracted text is split into smaller chunks using RecursiveCharacterTextSplitter.

### 4. Embedding Generation

Embeddings are generated using the Sentence Transformer model:

```python
sentence-transformers/all-MiniLM-L6-v2
```

### 5. Vector Database Creation

Embeddings are stored in a FAISS vector database for efficient similarity search.

### 6. Semantic Search

When a user asks a question, the vector database retrieves the most relevant chunks based on semantic similarity.

### 7. Context Retrieval

The retrieved chunks are combined to form the context.

### 8. Prompt Engineering

The retrieved context and user query are combined into a prompt.

### 9. Answer Generation

The prompt is passed to the FLAN-T5 language model to generate the final answer.

## Sample Questions

* What is machine learning?
* What is a well-posed learning problem?
* Explain the LMS algorithm.
* What are the applications of machine learning?
* What are the components of a learning system?

## Workflow

```text
PDF
 ↓
Text Extraction
 ↓
Chunking
 ↓
Embeddings
 ↓
FAISS Vector Store
 ↓
Semantic Search
 ↓
Context Retrieval
 ↓
Prompt Engineering
 ↓
LLM Response
```

## Results

The chatbot successfully retrieves relevant information from the PDF document and generates context-aware answers using Retrieval-Augmented Generation (RAG).

## Conclusion

This project demonstrates the complete implementation of a RAG pipeline using modern NLP tools and vector databases. The system improves answer quality by retrieving relevant information from external documents before generating responses.
