📚 RAG Knowledge Assistant

An intelligent Retrieval-Augmented Generation (RAG) based AI assistant that answers user queries using document context instead of relying only on pre-trained knowledge.

This system retrieves relevant document chunks using embeddings and a vector database, then generates accurate answers using an LLM.

🚀 Project Overview

Traditional LLMs sometimes hallucinate or give generic answers.
This project solves that problem by:

Converting documents into embeddings

Storing them in a vector database

Retrieving relevant chunks based on user query

Passing retrieved context to the LLM

Generating grounded, context-aware responses

🧠 Architecture

User Question
↓
Embedding Generation
↓
Vector Database Search (FAISS)
↓
Top Relevant Chunks Retrieved
↓
LLM (with context)
↓
Final Answer

🛠 Tech Stack

Python

OpenAI / Groq LLM

Sentence Transformers (Embeddings)

FAISS (Vector Database)

LangChain (optional)

Jupyter Notebook

📂 Project Structure
rag-knowledge-assistant/
│
├── RAG_App.ipynb
├── data/
│   └── sample_document.txt
├── requirements.txt
└── README.md

⚙️ Installation

Clone the repository:

git clone https://github.com/yourusername/rag-knowledge-assistant.git
cd rag-knowledge-assistant


Install dependencies:

pip install -r requirements.txt

🔑 API Setup

If using OpenAI:

import os
os.environ["OPENAI_API_KEY"] = "your_api_key_here"


If using Groq:

os.environ["GROQ_API_KEY"] = "your_groq_api_key"

▶️ How It Works (Step-by-Step)

Load document

Split into chunks

Convert chunks into embeddings

Store embeddings in FAISS

Take user question

Convert question to embedding

Retrieve top-k relevant chunks

Send chunks + question to LLM

Generate final response

📊 Example Output

User Question:

Why is brightness important in HCI?

Retrieved Chunks:

Importance of brightness in HCI

Adjustable brightness example

Dark mode explanation

Final Answer:
Brightness is important in HCI because it improves readability, reduces eye strain, and ensures usability in different lighting conditions.
