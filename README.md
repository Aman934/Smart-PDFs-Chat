# Chat with PDFs

This is a Streamlit application that allows users to interact with PDF documents using conversational AI. The app processes PDFs, extracts text, and enables users to ask questions about the content of these documents. 

## Features
- Upload multiple PDFs and extract text from them
- Split text into manageable chunks for processing
- Convert text into embeddings using HuggingFace's `sentence-transformers`
- Store embeddings in FAISS for efficient retrieval
- Use GROQ model for conversational AI
- Maintain conversation history

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/chat-with-pdfs.git
    cd chat-with-pdfs
    ```

2. Create and activate a virtual environment (optional but recommended):

    ```bash
    python -m venv env
    source env/bin/activate  # On Windows, use `env\Scripts\activate`
    ```

3. Install the required packages:

    ```bash
    pip install -r requirements.txt
    ```

4. Set up your environment variables by creating a `.env` file and adding your GROQ API key:

    ```env
    GROQ_API_KEY=your_groq_api_key_here
    ```

## Usage

1. Run the Streamlit application:

    ```bash
    streamlit run app.py
    ```

2. In the sidebar, upload your PDF documents and click on "Process".

3. Ask questions about the content of the uploaded documents in the text input field.

## Code Overview

### Main Application

The main application is contained in `app.py` and includes:

- `init_groq_model`: Initializes the GROQ model for conversational AI.
- `get_pdf_text`: Extracts text from the uploaded PDF documents.
- `get_text_chunks`: Splits the extracted text into manageable chunks.
- `get_vectorstore`: Converts text chunks into embeddings and stores them in FAISS.
- `get_conversation_chain`: Creates a conversational AI chain using the GROQ model and the vectorstore.
- `handle_userinput`: Handles user input and manages the conversation history.
- `main`: Sets up the Streamlit interface and handles file uploads and processing.

### Additional Files

- `requirements.txt`: Lists all the dependencies needed for the project.
- `.env`: Contains the environment variables, specifically the GROQ API key.

## Acknowledgements

- [Streamlit](https://streamlit.io/)
- [HuggingFace](https://huggingface.co/)
- [FAISS](https://github.com/facebookresearch/faiss)
- [GROQ](https://groq.com/)

Feel free to fork this repository and customize it to suit your needs. Contributions are welcome!
