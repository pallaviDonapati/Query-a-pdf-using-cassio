# Query-a-pdf

Overview

This project enables querying PDF documents stored in Astra DB by extracting content, embedding it using OpenAI embeddings, and storing the embeddings in a Cassandra vector store. Users can query the system with natural language questions, and the project retrieves relevant document content based on vector similarity, generating answers with the OpenAI language model.

Project Overview

This repository demonstrates how to use Astra DB (Cassandra) and OpenAI to create a question-answering system. The pipeline extracts text from a PDF, splits it into chunks, embeds those chunks, and stores the embeddings in Astra DB. When users submit queries, the system retrieves the most relevant document chunks from Astra DB using vector similarity, and OpenAI generates answers based on those chunks.

Repository Contents

app.py: Main code for extracting text from PDFs, embedding with OpenAI, storing in Astra DB, and querying with natural language.

requirements.txt: Lists all necessary dependencies to run the project.

Key Features

PDF Extraction: Extract text from PDFs using PyPDF2.
Text Chunking: Split the document into smaller chunks using CharacterTextSplitter.
Embedding: Use OpenAI embeddings to generate vector representations of the document chunks.
Cassandra Vector Store: Store and retrieve the embeddings in Astra DB, using Cassandra for vector search.
Query Answering: Retrieve relevant chunks from Astra DB using vector similarity and generate answers with OpenAI.

Model Interaction
PDF Extraction: Text is extracted from the PDF using PyPDF2.
Text Chunking: The extracted text is divided into smaller chunks using the CharacterTextSplitter.
Embedding: OpenAI embeddings are used to transform the text into vector representations.
Vector Store: The embeddings are stored in Cassandra, enabling fast and efficient vector search.
Query Answering: When the user submits a query, the system retrieves relevant document chunks from Cassandra and generates an answer using OpenAI's language model.
