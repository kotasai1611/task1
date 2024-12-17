# Chat with Multiple PDFs

A Streamlit application that enables interactive conversations with multiple PDF documents. Using state-of-the-art machine learning models, this app leverages natural language processing (NLP) to parse, embed, and retrieve information from PDFs.

## Features

- **PDF Text Extraction**: Efficiently extracts text from uploaded PDF documents using `PyPDF2`.
- **Text Chunking**: Splits long text into manageable chunks for embedding and retrieval.
- **Vector Store Creation**: Uses `HuggingFaceInstructEmbeddings` and `FAISS` to generate and store vector embeddings.
- **Conversational AI**: Supports multi-turn conversations with a `ConversationalRetrievalChain` backed by `HuggingFaceHub`.
- **Streamlit Integration**: Provides a user-friendly web interface for uploading PDFs, processing, and querying.

## Requirements

- Python 3.8+
- Packages:
  - `streamlit`
  - `dotenv`
  - `PyPDF2`
  - `langchain`
  - `FAISS`
  - `huggingface_hub`

Install dependencies using:

```bash
pip install -r requirements.txt
```

## How to Use

1. Open the application in your browser after starting it locally.
2. Upload one or more PDF files via the sidebar.
3. Click "Process" to analyze the documents.
4. Enter your questions in the input box, and the app will respond based on the uploaded content.

## Application Structure

- **`app.py`**: Main script that defines the application logic and user interface.
- **`htmlTemplates.py`**: Contains CSS and HTML templates for customizing the UI.
- **Functions**:
  - `get_pdf_text`: Extracts text from uploaded PDFs.
  - `get_text_chunks`: Splits text into smaller chunks.
  - `get_vectorstore`: Creates a vector store from text chunks using FAISS.
  - `get_conversation_chain`: Builds a conversational chain for querying the vector store.
  - `handle_userinput`: Manages user interaction and displays responses.

## Future Enhancements

- Support for additional file types (e.g., Word documents, Excel sheets).
- Enhanced UI with document previews and analysis insights.
- Deployment to cloud platforms like AWS, GCP, or Azure.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your changes.
