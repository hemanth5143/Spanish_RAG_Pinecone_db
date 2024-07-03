###Spanish RAG System with Pinecone and Mistral-7B

This project implements a Retrieval-Augmented Generation (RAG) system in Spanish using Pinecone as a vector database and the Mistral-7B language model. The system is designed to answer questions about the Bible based on the Reina Valera Spanish translation.

## Key Features

- Uses Pinecone for efficient vector storage and retrieval
- Leverages the Mistral-7B-Instruct-v0.1 model for natural language understanding and generation
- Employs the jina-embeddings-v2-base-es model for creating Spanish-optimized embeddings
- Implements 8-bit quantization for reduced memory usage
- Utilizes LlamaIndex for document indexing and query processing

## System Components

1. **Document Loading**: Reads Bible text from a local directory
2. **Embedding Generation**: Creates vector embeddings of the text using jina-embeddings-v2-base-es
3. **Vector Storage**: Stores embeddings in a Pinecone serverless index
4. **Language Model**: Uses Mistral-7B-Instruct-v0.1 for question answering
5. **Query Engine**: Processes user queries and retrieves relevant information

## Usage

The system can answer questions about the Bible in Spanish. For example:

```python
response = query_engine.query("¿Cuáles son los puntos clave de la Biblia? - Traducción Reina Valera al Español")
print(response)
```

## Setup

The project requires several Python libraries and API keys for Hugging Face and Pinecone. Detailed setup instructions are provided in the notebook.

## Note

This project is designed to run in a Google Colab environment with GPU acceleration. Adjustments may be needed for local execution or different hardware config
