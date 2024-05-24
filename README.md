# End-to-End-RAG-Application-Using-Haystack-MistralAI-Pinecone-FastAPI
Created an end-to-end RAG application using Haystack framework, Pinecone vector store, Mistral LLM and Fastapi. 

# Project Overview

## Description
This project involves building a Retrieval-Augmented Generation (RAG) system using Haystack as the framework, Pinecone as the vector store, and FastAPI for the web framework. The data source is a single PDF file, and the Large Language Model (LLM) used is "mistralai/Mistral-7B-v0.1" from Hugging Face. The system includes an HTML interface to render responses in a JSON format.

## Components

### Data Ingestion
Ingestion.py: This file handles the ingestion of the PDF file. It extracts text from the PDF, processes it into chunks, and generates vector embeddings using Haystack's embedding model. These embeddings are then stored in a Pinecone index.
### Retrieval
Retrieval.py: This file is responsible for querying the Pinecone index. Given a user query, it retrieves the most relevant chunks of text from the Pinecone vector store based on similarity to the query.
### Generation
Generation.py: This file uses the "mistralai/Mistral-7B-v0.1" model from Hugging Face to generate responses based on the retrieved text. The generated response is then prepared to be rendered in a JSON format for the web interface.
### Utilities
Utils.py: This file contains configurations and utility functions for interacting with Pinecone. It includes setup functions for initializing the Pinecone client and managing the index.
### Web Framework
FastAPI
FastAPI Application: The FastAPI application serves as the backend for handling user queries. It processes requests, interacts with the retrieval and generation modules, and returns responses in JSON format.
HTML Page: A simple HTML page is designed to accept user queries and display responses from the LLM.


### Package Setup
Internal Package Structure
The internal package is structured to separate concerns into different modules:

ingestion.py
retrieval.py
generation.py
utils.py

- Create a conda virtual environment using in cmd using: conda create -p env-RAG python=3.9 -y
