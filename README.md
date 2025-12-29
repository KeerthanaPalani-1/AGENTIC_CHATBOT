# AGENTIC_CHATBOT
A multi-agent chatbot using RAG and LLMs to answer questions from internal documents and execute tool-based queries. Features semantic document retrieval, FAISS vector store, and HuggingFace LLMs for accurate, context-aware responses.

Agentic RAG Chatbot

This project demonstrates an agent-based chatbot built with LangChain, RAG, and MCP-style service separation. It can answer questions from internal policy documents and also handle tool-based tasks like summaries or checklists.

Features

Retrieval-Augmented Generation (RAG) using FAISS and document chunking

Coordinator-based agent routing to send queries to the right agent (document or tool)

Fallback substring search when embeddings don’t return relevant results

Optimized LLM prompts to give the best possible answers from the documents

Modular MCP-style services – agents never talk directly to the vector database

CPU-only, no API tokens required

Streamlit chat UI for easy interaction

Document Content
internal company policies and procedures.

How to Run
# Create and activate virtual environment
python -m venv venv

# Windows
venv\Scripts\activate

# macOS/Linux
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Run the Streamlit chat UI
streamlit run app/chat_ui.py

Example Queries

"What is the onboarding policy?"

"How soon must incidents be reported?"

"Who approves access requests?"

"What training is required for new employees?"

"Give me a checklist for onboarding."

Notes

The chatbot answers questions based on the documents you provide; queries outside the content may return guidance tips.

Short queries are handled using embedding similarity and a fallback substring search.

LLM prompts are optimized to provide the best possible answers from documents instead of returning “Not found” unnecessarily.
