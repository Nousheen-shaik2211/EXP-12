# EXP-12
# RAG Data Indexing and FAISS Retrieval

## Aim
To build a basic data indexing pipeline for Retrieval-Augmented Generation (RAG) by splitting a text document into chunks, generating embeddings, storing them in a FAISS vector store, and retrieving relevant chunks using similarity search.

## Technologies Used
- Python
- LangChain
- OpenAI Embeddings
- FAISS
- RecursiveCharacterTextSplitter

## Algorithm
1. Install the required Python packages.
2. Configure the OpenAI API key.
3. Define a sample text about climate change.
4. Split the text using `RecursiveCharacterTextSplitter` with a chunk size of 300 and overlap of 30.
5. Convert the text chunks into Document objects.
6. Generate embeddings using `OpenAIEmbeddings`.
7. Store the embedded documents in FAISS using `FAISS.from_documents()`.
8. Search for the query "What are the effects of climate change?"
9. Retrieve the top two relevant chunks with relevance scores.
10. Print the number of chunks and retrieval results.

## Project Structure
```text
RAG_FAISS_Data_Indexing/
├── main.py
├── README.md
├── requirements.txt
└── .gitignore
```

## Installation

```bash
pip install -r requirements.txt
```

## Configure API Key

**Windows PowerShell:**
```powershell
$env:OPENAI_API_KEY="your_api_key_here"
```

**Linux/macOS:**
```bash
export OPENAI_API_KEY="your_api_key_here"
```

Replace the placeholder with your valid OpenAI API key. Do not commit the key to GitHub.

## Run the Experiment

```bash
python main.py
```

## Expected Output
The program displays:
- Number of chunks created
- Search query
- Two retrieved text chunks
- Relevance score for each retrieved chunk

The exact number of chunks, retrieved text, and scores depend on the text and embedding model.

## Conclusion
This experiment demonstrates the indexing and retrieval stages of a basic RAG pipeline using text chunking, vector embeddings, FAISS, and similarity search.
