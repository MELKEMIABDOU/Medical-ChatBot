Medical Chatbot 🩺

An AI-powered medical chatbot built with Python, LangChain, Ollama, Hugging Face Embeddings, and Pinecone. This project uses a Retrieval-Augmented Generation (RAG) system to retrieve relevant information from medical PDF documents and generate context-aware answers to user questions.

🚀 Technologies Used
Python 3.10 – Core programming language
LangChain – LLM orchestration and RAG pipeline
Ollama (Llama 3.2) – Local large language model
Hugging Face Embeddings – Text embedding generation
Pinecone – Vector database for storing and retrieving document embeddings
AWS – Cloud infrastructure for the vector database
✨ Features
Medical question answering based on document retrieval
PDF document processing and text extraction
Semantic search using vector embeddings
Context-aware responses using Retrieval-Augmented Generation (RAG)
Integration with a locally running Llama model through Ollama
Vector storage and retrieval using Pinecone
📋 Prerequisites

Before getting started, make sure you have installed:

Python 3.10
Git
Conda (Anaconda or Miniconda)
Ollama
A Pinecone account and API key
A Hugging Face account or access to the required embedding model, if applicable
🛠️ Installation and Setup
Step 1: Clone the Repository
git clone https://github.com/entbappy/End-to-End-Medical-Chatbot.git

Step 2: Navigate to the Project Directory
cd End-to-End-Medical-Chatbot

Step 3: Create and Activate a Conda Environment
conda create -n medibot python=3.10 -y
conda activate medibot

Step 4: Install Dependencies
pip install -r requirements.txt

⚙️ Configuration

Configure the API credentials and model settings required by the application.

Create a .env file in the project root directory if the application supports environment variables.
Add your Pinecone API key and any other required configuration values.
Configure the Hugging Face embedding model and Ollama model according to the project code.

Example .env configuration:

PINECONE_API_KEY=your_pinecone_api_key


Important: Never commit API keys, passwords, or other secrets to GitHub. Add .env to your .gitignore file.

🤖 Set Up Ollama

Install Ollama from the official website:

https://ollama.com/

After installing Ollama, download the Llama 3.2 model:

ollama pull llama3.2


Verify that the model is available:

ollama list


Make sure the model name matches the one configured in your application.

📚 Medical PDF Documents

The chatbot uses medical PDF documents as its knowledge source.

The typical RAG workflow is:

Load medical PDF files.
Extract and split the document text into manageable chunks.
Generate embeddings using a Hugging Face embedding model.
Store the embeddings in Pinecone.
Retrieve relevant document chunks when a user asks a question.
Pass the retrieved context to the language model to generate an answer.

Follow the repository's implementation to determine where to place PDF files and how to run the document ingestion process.

▶️ Run the Application

Once the dependencies, environment variables, Ollama model, and Pinecone configuration are ready, run the application using the entry point defined in the repository.

For example, if the project uses app.py:

python app.py


If it uses a different entry point, replace app.py with the appropriate filename. Check the project files for the correct command.

🏗️ Project Architecture
Medical PDFs
     |
     v
Document Loading and Text Splitting
     |
     v
Hugging Face Embeddings
     |
     v
Pinecone Vector Database
     |
     v
User Question
     |
     v
Semantic Retrieval
     |
     v
Relevant Document Context
     |
     v
Ollama (Llama 3.2) + LangChain
     |
     v
Generated Answer

🔒 Disclaimer

This project is intended for educational and research purposes only. It is not a substitute for professional medical advice, diagnosis, or treatment. Always consult a qualified healthcare professional for medical concerns.

👨‍💻 Contributing

Contributions, suggestions, and improvements are welcome.

Fork the repository.
Create a feature branch.
Commit your changes.
Open a pull request.
📄 License

Add the appropriate license to this repository if you intend to distribute or reuse the project.

Built with Python, LangChain, Ollama, Hugging Face, and Pinecone.
