#RAG Model Integration with Langflow and Ollama
Overview
This project demonstrates the creation of a Retrieval-Augmented Generation (RAG) model using Langflow and Ollama. The workflow involves processing a PDF document, splitting the text into chunks, and embedding these chunks using Ollama’s embedding model. The embedded text is stored in an Astra database for efficient retrieval. User queries are processed through the system, leveraging chat memory to generate context-aware responses from a Local Language Model (LLM).

Features
PDF Processing: Extracts and splits text from PDFs.
Embedding Generation: Uses Ollama for creating embeddings of text chunks.
Astra DB Integration: Stores embeddings in a scalable database for efficient retrieval.
RAG Workflow: Combines retrieval with LLM to generate informed responses.
Chat Memory: Maintains conversation context for more coherent interactions.
Architecture
1. Data Ingestion and Embedding
The initial part of the workflow involves ingesting a PDF file, splitting its content into smaller chunks, and generating embeddings using Ollama. The embeddings are stored in an Astra database.


2. Query Processing and Response Generation
User queries are embedded and matched against the stored data in Astra DB. Relevant information is retrieved and combined with chat memory before being sent to the LLM for generating a response.


Usage
Running the Workflow
Load the PDF: Upload your PDF file using the file loader component.
Embedding and Storage: The text is split into chunks, embedded using Ollama, and stored in Astra DB.
Query and Generate: Input your query through the chat interface. The system retrieves relevant chunks, incorporates chat memory, and generates a response using the LLM.
Example Input and Output
Input: "Can you summarize the main points from the PDF?"
Output: The LLM generates a summary based on the most relevant chunks retrieved from Astra DB, considering the context from previous interactions.
Screenshots
Data Ingestion and Embedding

Query Processing and Response Generation

Contributing
Contributions are welcome! Please open an issue or submit a pull request for any improvements or suggestions.

JSON File:
You can download and import the given json file to your langflow account and use the RAG.
