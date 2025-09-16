# RAG Project (Retrieval-Augmented Generation)

This project demonstrates a Retrieval-Augmented Generation (RAG) pipeline implemented in Google Colab using LangChain and Google Generative AI embeddings.
It retrieves relevant context from external sources and augments user queries before passing them to a Large Language Model (LLM) for more accurate answers.


# Features

Built and tested in Google Colab (no local setup required)
Load documents from the web using LangChain WebBaseLoader
Split text into chunks with RecursiveCharacterTextSplitter
Store and query embeddings using Chroma Vector Database
Use Google Generative AI embeddings for semantic search
End-to-end RAG workflow in a Jupyter Notebook

# Files

RAG_PROJECT.ipynb → The main Colab notebook with the full pipeline
README.md → Project documentation

# How to Run (Google Colab)

Open the notebook in Google Colab:
Click here: Open in Colab
Upload the RAG_project.ipynb file
Install required dependencies inside Colab:
 
  !pip install langchain langchain_chroma langchain_community langchain_core langchain_google_genai langchain_text_splitters bs4


Add your Google Generative AI API Key in Colab:

import os

os.environ["GOOGLE_API_KEY"] = "your_api_key_here"


Run the notebook cells step by step:

  Load data (web/documents)
  
  Chunk text and create embeddings
  
  Store in Chroma vector database
  
  Query and generate answers with RAG

# Example Workflow

Input query: "Explain LangChain RAG in simple terms"
Retriever fetches context from documents.
LLM generates an enriched answer using both the query and context.

# Future Improvements

Add more document loaders (PDF, CSV, etc.)
Try other vector databases (Pinecone, Weaviate, FAISS)
Deploy as a Streamlit or Gradio app for interaction
