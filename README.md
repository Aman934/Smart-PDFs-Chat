# Chat with PDFs

This project enables users to upload PDF documents, process them, and interact with the content through a conversational AI interface. The application uses `Streamlit` for the web interface, `PyPDF2` for PDF parsing, and integrates `Langchain` with the `Groq` model for conversational AI powered by embeddings and vector search.

## Requirements

Before running the project, ensure you have the following dependencies installed:

- Python 3.x
- `streamlit` for the web interface
- `dotenv` for environment variable management
- `PyPDF2` for reading PDFs
- `langchain` and `langchain_community` for language model integration
- `faiss` for vector search

Install the dependencies by running the following:

```bash
pip install -r requirements.txt
