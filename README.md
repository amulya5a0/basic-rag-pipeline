# RAG Hands-on Practice

## Overview

This repository contains hands-on tutorials exploring Retrieval-Augmented Generation (RAG) using Python, LangChain, LLM APIs, embeddings, and vector databases.

The tutorials cover the core stages of a RAG pipeline, from loading content and preparing documents to generating embeddings, storing vectors, retrieving relevant information, and using the retrieved context to generate responses with a Large Language Model (LLM).

The practice examples cover custom text, PDF files, additional documents, local vector-store persistence, and online content where supported by the corresponding notebook.

## Technologies Used

- **Python** — Core programming language
- **LangChain** — Document processing and RAG pipeline components
- **LLM APIs** — Language model responses
- **OpenAI Embeddings** — Text-to-vector conversion
- **ChromaDB** — Vector storage and similarity search
- **Jupyter Notebook** — Step-by-step experimentation
- **Python dotenv** — Environment variable management

## RAG Implementation: Step by Step

### Step 1: Configure the Environment

Set up the Python environment, install the required dependencies, and configure API credentials using environment variables.

Initialize the language model through LangChain to generate responses to prompts.

### Step 2: Load the Source Content

Explore how content can be prepared from different sources:

- **Custom text:** Work with text written or supplied directly by the user.
- **PDF files:** Extract text from PDF documents using a document loader.
- **Additional documents:** Load and incorporate documents into the retrieval workflow.
- **Online content:** Prepare content from supported online sources when the relevant notebook includes a web or URL loader.

The objective is to make information from different sources available for retrieval.

### Step 3: Add Document Metadata

Associate documents or chunks with metadata, such as source names and other relevant identifiers.

Metadata helps identify where retrieved information originated and supports source tracking.

### Step 4: Split Documents into Chunks

Divide long documents into smaller, manageable text chunks using a text splitter such as `RecursiveCharacterTextSplitter`.

Configure chunk size and overlap to preserve useful context across chunk boundaries and prepare content for embedding.

### Step 5: Generate Text Embeddings

Convert text chunks into numerical vector representations using an embedding model.

These embeddings represent semantic information and allow the system to search for content related to a user's query.

### Step 6: Store Embeddings in a Vector Database

Store the document chunks and their embeddings in a vector store such as ChromaDB.

Organize the content so that relevant chunks can be retrieved efficiently when a query is submitted.

### Step 7: Perform Semantic Search

Convert a user's query into a representation suitable for retrieval and search the vector store for semantically relevant chunks.

Retrieve the most relevant results instead of relying only on exact keyword matches.

### Step 8: Provide Retrieved Context to the LLM

Pass the user's question and the retrieved source content to the language model.

Use the retrieved context to generate an answer relevant to the supplied documents or other indexed content.

### Step 9: Explore Local Vector-Store Persistence

Practise saving and reusing a vector store locally, where implemented, so previously indexed content can be accessed again without rebuilding the entire index every time.

### Step 10: Add New Documents

Explore extending an existing retrieval collection with additional documents, making their content available to subsequent semantic searches and LLM responses.

## Tutorial Notebooks

The repository is organized into progressive hands-on exercises:

1. **`1.0_Rag_with_own_text.ipynb`** — Introduction to RAG using custom text.
2. **`2.0_RAG_PDF.ipynb`** — Loading PDF documents, adding metadata, splitting text, creating embeddings, storing vectors, and performing semantic search.
3. **`3.0_RAG_local_persistance.ipynb`** — Exploring local vector-store persistence.
4. **`4.0_RAG_Add_Docs.ipynb`** — Practising the addition of documents to the retrieval workflow.

Additional source files and folders support the tutorial exercises. Refer to each notebook for its specific implementation.

## Getting Started

### Prerequisites

- Python
- Jupyter Notebook
- Required Python packages
- An API key for the LLM and embedding provider used in the notebook

### Installation

1. Clone this repository.
2. Create and activate a Python virtual environment.
3. Install the dependencies listed in `requirements.txt`.
4. Create a local `.env` file based on `.env.example`.
5. Add the required API key to your local environment configuration.
6. Open the relevant notebook in Jupyter Notebook.
7. Follow the notebook cells in order, providing the required text, documents, PDFs, or supported online source.


## Learning Outcomes

Through these exercises, the repository explores:

- The fundamental concepts of Retrieval-Augmented Generation.
- Ingesting and preparing text from different sources.
- Document chunking and metadata management.
- Generating and storing text embeddings.
- Vector similarity search and context retrieval.
- Connecting retrieved information to LLM-generated responses.
- Local vector-store persistence and adding documents to a retrieval collection.
