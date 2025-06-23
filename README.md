# Chat with PDF

This project provides interactive Streamlit web applications that allow users to upload PDF files and chat with their contents using advanced Large Language Models (LLMs). The apps leverage [embedchain](https://github.com/embedchain/embedchain) for knowledge base management and support both OpenAI and locally running Ollama Llama models.

## Features

- **Upload and Chat with PDFs:** Upload a PDF and ask questions about its content.
- **Multiple LLM Backends:** 
  - Use OpenAI API (in [`chat_pdf.py`](chat_pdf.py))
  - Use local Ollama Llama3 ([`chat_pdf_llama3.py`](chat_pdf_llama3.py)) or Llama3.2 ([`chat_pdf_llama3.2.py`](chat_pdf_llama3.2.py))
- **Persistent Knowledge Base:** Each session uses a temporary vector database for document embeddings.
- **Chat History:** (In Llama3.2 app) Maintains chat history and allows clearing it.
- **PDF Preview:** (In Llama3.2 app) Preview uploaded PDFs in the sidebar.

## Requirements

See [requirements.txt](requirements.txt):

- streamlit
- embedchain
- streamlit-chat

## Usage

### 1. Install dependencies

```sh
pip install -r requirements.txt
```

### 2. Run an app

Choose one of the following scripts:

#### a. OpenAI (requires OpenAI API key)

```sh
streamlit run chat_pdf.py
```

#### b. Llama3 with Ollama (requires Ollama running locally)

```sh
streamlit run chat_pdf_llama3.py
```

#### c. Llama3.2 with Ollama (with chat history and PDF preview)

```sh
streamlit run chat_pdf_llama3.2.py
```

### 3. Interact

- Upload a PDF file.
- Ask questions about its content in the chat interface.

## Notes

- For Llama3/Llama3.2 apps, ensure [Ollama](https://ollama.com/) is running locally and the required models are available.
- The OpenAI app requires a valid OpenAI API key.

## File Overview

- `chat_pdf.py`: Chat with PDF using OpenAI API.
- `chat_pdf_llama3.py`: Chat with PDF using Llama3 via Ollama.
- `chat_pdf_llama3.2.py`: Enhanced chat with PDF using Llama3.2 via Ollama, with chat history and PDF preview.
- `requirements.txt`: Python dependencies.

## License
MIT License.
