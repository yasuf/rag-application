# RAG Application with Reddit Jokes

A Retrieval-Augmented Generation (RAG) application that demonstrates semantic search and contextual AI responses using a dataset of Reddit jokes. The application uses Pinecone as a vector database and Ollama for local LLM inference.

## Features

- **Vector Database Integration**: Uses Pinecone to store and search joke embeddings
- **Semantic Search**: Find relevant jokes based on natural language queries
- **Local LLM**: Powered by Ollama's Llama 3.2 model for response generation
- **Batch Processing**: Efficiently processes and indexes large datasets
- **Interactive Jupyter Notebook**: Easy-to-follow implementation in a notebook format

## Architecture

The application follows a typical RAG pattern:

1. **Data Ingestion**: Reddit jokes are loaded from a JSON file
2. **Embedding & Storage**: Text is embedded using Pinecone's embedding model and stored in a vector database
3. **Retrieval**: User queries are used to find semantically similar jokes
4. **Generation**: Retrieved context is fed to Ollama's LLM to generate responses

## Requirements

- Python 3.11
- Pipenv (for dependency management)
- Pinecone API key
- Ollama with Llama 3.2 model

## Installation

1. **Clone the repository**:

```bash
git clone https://github.com/yasuf/rag-application.git
cd rag-application
```

2. **Install dependencies**:

```bash
pipenv install
```

3. **Set up environment variables**:

Create an `.env` file in the project root:

```env
PINECONE_API_KEY=your_pinecone_api_key_here
```

4. **Install and set up Ollama**:

To install Ollama go to https://ollama.com/download/linux

## Usage

1. **Start Ollama service** (if not already running):

Start the Desktop Ollama application.

1. **Open the Jupyter notebook**:

```bash
code main.ipynb
```

2. **Run the cells sequentially** to:
   - Set up the Pinecone index
   - Process and upload joke data
   - Perform semantic search queries
   - Generate AI responses based on retrieved context

## Data

The application uses `reddit_jokes.json` containing jokes from Reddit

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

This project is open source. Please check the license file for details.

