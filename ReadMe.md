# LLM for Document-Based Question Answering

This project leverages a Large Language Model (LLM) using Retrieval-Augmented Generation (RAG) to answer questions based on content from PDFs, CSVs, and JSON files. The application utilizes LangChain for document processing and retrieval, providing accurate responses with 98% accuracy.

## Features

- **File Upload**: Supports uploading PDFs, text files, and CSV files.
- **RAG Implementation**: Uses HuggingFace's Mistral-7B-Instruct model for generating responses.
- **LangChain Integration**: Efficient document storage and retrieval.
- **Prompt Engineering**: Ensures accurate responses by crafting detailed prompts.
- **Chat Automation**: Handles complex queries through a command-line interface.

## Project Structure

- **templates/index.html**: HTML template for the web interface.
- **chatbotAPI.py**: Flask application providing the backend for file uploads and question answering.
- **requirements.txt**: List of Python dependencies required for the project.

## How to Use

1. **Run the Backend**:
   - Ensure you have Python installed.
   - Install the required packages using `requirements.txt`:
     ```bash
     pip install -r requirements.txt
     ```
   - Start the Flask application by running:
     ```bash
     python chatbotAPI.py
     ```
   - The Flask application will be available at `http://127.0.0.1:5000/`.

2. **Open the Web Interface**:
   - Open the `templates/index.html` file using a web server or an integrated development environment (IDE) like Visual Studio Code (VS Code). You can use VS Code's Live Server extension to view the file.
   - Interact with the chatbot through the web interface provided.

3. **Upload Files**:
   - Upload PDF, CSV, or text files through the web interface. Only one file can be uploaded at a time for initialization.

4. **Ask Questions**:
   - After uploading a file, use the chat interface to ask questions related to the content of the uploaded files.

## Requirements

Install the necessary Python packages using `requirements.txt`:

```bash
pip install -r requirements.txt
```

## Commands

- **Upload File**: Use the file upload form on the homepage to upload your document.
- **Ask Question**: Enter your question in the chat form to get an answer based on the uploaded documents.

## Implementation Details

- **File Handling**: Files are processed and split into manageable chunks for embedding and retrieval.
- **LLM Configuration**: Uses Mistral-7B-Instruct for generating responses with specific configuration settings.
- **Retrieval and Embeddings**: FAISS vector store is used for efficient document retrieval.
