Medical Chatbot 

An AI-powered medical chatbot built with Python, LangChain, Ollama, Hugging Face Embeddings, and Pinecone. This project uses a Retrieval-Augmented Generation (RAG) system to retrieve relevant information from medical PDF documents and generate context-aware answers to user questions.

 Technologies Used
Python 3.10 – Core programming language
LangChain – LLM orchestration and RAG pipeline
Ollama (Llama 3.2) – Local large language model
Hugging Face Embeddings – Text embedding generation
Pinecone – Vector database for storing and retrieving document embeddings
AWS – Cloud infrastructure for the vector database
 Features
Medical question answering based on document retrieval
PDF document processing and text extraction
Semantic search using vector embeddings
Context-aware responses using Retrieval-Augmented Generation (RAG)
Integration with a locally running Llama model through Ollama
Vector storage and retrieval using Pinecone
 Prerequisites

Before getting started, make sure you have installed:

Python 3.10
Git
Ollama
A Pinecone account and API key
Access to the required Hugging Face embedding model
 
 Installation and Setup
Step 1: Clone the Repository
git clone https://github.com/MELKEMIABDOU/Medical-ChatBot.git
Step 2: Navigate to the Project Directory
cd Medical-ChatBot
Step 3: Create a Python Virtual Environment
Create a virtual environment using Python's built-in venv module:

python -m venv venv
Activate the virtual environment according to your operating system.

Windows (Command Prompt):

venv\Scripts\activate
Windows (PowerShell):

.\venv\Scripts\Activate.ps1
macOS / Linux:

source venv/bin/activate
Step 4: Install Dependencies
Make sure your virtual environment is activated, then install the required Python packages:

python -m pip install --upgrade pip
pip install -r requirements.txt
Step 5: Configure Environment Variables
Configure the API keys and settings required by the application, including your Pinecone API key.

If your project uses a .env file, create it in the project root and add the variables expected by your code.

Important: Never upload API keys or other sensitive credentials to GitHub.

Step 6: Set Up Ollama
Install Ollama from the official website:

https://ollama.com/

Download the Llama 3.2 model:

ollama pull llama3.2
Verify that the model is installed:

ollama list
Step 7: Run the Application
Run the application using the entry-point file in your repository. For example, if the main file is app.py:

python app.py
Replace app.py with the correct filename if your project uses a different entry point.

 Configuration

Configure the API credentials and model settings required by the application.

Create a .env file in the project root directory if the application supports environment variables.
Add your Pinecone API key and any other required configuration values.
Configure the Hugging Face embedding model and Ollama model according to the project code.

Example .env configuration:

PINECONE_API_KEY=your_pinecone_api_key


Important: Never commit API keys, passwords, or other secrets to GitHub. Add .env to your .gitignore file.

 Set Up Ollama

Install Ollama from the official website:

https://ollama.com/

After installing Ollama, download the Llama 3.2 model:

ollama pull llama3.2


Verify that the model is available:

ollama list


Make sure the model name matches the one configured in your application.

 Medical PDF Documents

The chatbot uses medical PDF documents as its knowledge source.

The typical RAG workflow is:

Load medical PDF files.
Extract and split the document text into manageable chunks.
Generate embeddings using a Hugging Face embedding model.
Store the embeddings in Pinecone.
Retrieve relevant document chunks when a user asks a question.
Pass the retrieved context to the language model to generate an answer.

Follow the repository's implementation to determine where to place PDF files and how to run the document ingestion process.

 Run the Application

Once the dependencies, environment variables, Ollama model, and Pinecone configuration are ready, run the application using the entry point defined in the repository.

For example, if the project uses app.py:

python app.py


If it uses a different entry point, replace app.py with the appropriate filename. Check the project files for the correct command.

 Project Architecture
Medical PDFs 
     -->     
Document Loading and Text Splitting
     -->
Hugging Face Embeddings
     -->
Pinecone Vector Database
     -->
User Question
     -->
Semantic Retrieval
     -->
Relevant Document Context
     -->
Ollama (Llama 3.2) + LangChain
     -->
Generated Answer

 Disclaimer

This project is intended for educational and research purposes only. It is not a substitute for professional medical advice, diagnosis, or treatment. Always consult a qualified healthcare professional for medical concerns.

 Contributing

Contributions, suggestions, and improvements are welcome.

Fork the repository.
Create a feature branch.
Commit your changes.
Open a pull request.

 

Built with Python, LangChain, Ollama, Hugging Face, and Pinecone.
