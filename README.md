# RAG Chat System

A Retrieval Augmented Generation (RAG) chat system with a web interface that enables intelligent conversations with your documents. The system combines the power of large language models with local document knowledge to provide accurate, context-aware responses.

![RAG Chat System](https://github.com/Absorber97/RAG-Chat-System/blob/main/assets/CleanShot%202024-11-05%20at%2020.12.48%402x.png)

- Step 1: https://github.com/Absorber97/RAG-Document-Loader
- Step 2: https://github.com/Absorber97/Vectorstores-Embedding
- Step 3 (This Project): https://github.com/Absorber97/RAG-Chat-System

- Google Slides: https://docs.google.com/presentation/d/1M6phftXYIXe3JoNBUYQaHX8w-ksWT1gSVVD-0rbM45k/edit?usp=sharing
- Google Slides (PDF): https://drive.google.com/file/d/1jDRWnCCFaf5n-EntWYbexF-5OuvhchNj/view?usp=sharing

## Features

### Document Processing
- **Multiple Format Support**:
  - PDF Documents: Academic papers, reports, books
  - YouTube Videos: Automatic transcription and processing
  - Web Pages: Direct URL content extraction
  - Extensible architecture for new formats

### Intelligent Search
- Vector-based semantic search using OpenAI embeddings
- Source attribution for transparency
- Context-aware responses
- Conversational memory for follow-up questions

### User Interface
- Clean, intuitive web interface
- Real-time document processing feedback
- Chat history management
- Source document management
- Progress indicators for long operations

## Installation

1. **Create Virtual Environment**:
   ```bash
   python -m venv venv
   ```

   - On Windows:
     ```bash
     venv\Scripts\activate
     ```
   - On macOS/Linux:
     ```bash
     source venv/bin/activate
     ```

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Configure OpenAI API**:
   - Create a `.env` file:
     ```env
     OPENAI_API_KEY=your_api_key_here
     ```

4. **Install System Dependencies**:
   - **ffmpeg** (for YouTube processing):
     - On macOS:
       ```bash
       brew install ffmpeg
       ```
     - On Ubuntu/Debian:
       ```bash
       sudo apt-get install ffmpeg
       ```
     - On Windows:
       ```bash
       choco install ffmpeg
       ```

## Project Structure

```
Step 3/
├── data/
│ ├── chroma/ # Vector database
│ ├── sources/ # Source documents
│ └── temp/ # Temporary files
├── rag/ # Core RAG implementation
│ ├── init.py
│ ├── rag_chain.py
│ ├── rag_loader.py
│ ├── rag_service.py
│ └── rag_vectorstore.py
├── utils/
│ └── env_manager.py
├── .env # Environment variables
├── .gitignore
├── panel_app.py # Web interface
├── requirements.txt
└── start.py # Application entry point
```


## Usage

1. Start the application:

bash
python start.py


2. Access the web interface at the provided URL (typically http://localhost:XXXX)

3. Use the interface:
   - **Chat Tab**: Ask questions about your documents
   - **Add Sources Tab**: Upload new documents
     - Upload PDF files
     - Add YouTube URLs
     - Add webpage URLs

4. Features:
   - Ask questions about document content
   - Follow-up questions supported
   - See source attributions
   - Clear chat history
   - Add new documents dynamically

## Development

- Python 3.9+
- Uses Panel for web interface
- LangChain for RAG implementation
- ChromaDB for vector storage
- OpenAI for embeddings and chat

## License

MIT License
