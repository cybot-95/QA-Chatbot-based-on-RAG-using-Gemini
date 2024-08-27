## RAG-based QA Chatbot with Gemini 1.5 Flash and Pinecone DB 🚀🤖

This repository implements a Retrieval-Augmented Generation (RAG) chatbot powered by Google's Gemini 1.5 Flash large language model (LLM) and Pinecone's vector database. This chatbot leverages the strengths of both components:

* **Gemini 1.5 Flash:** Delivers powerful text generation capabilities with a long context window and multilingual support.
* **Pinecone DB:** Efficiently stores and retrieves relevant information from a provided PDF document, enabling the chatbot to access and answer questions based on its content.

**Key Feature:**

The chatbot is specifically designed to only answer questions based on the information contained within a provided PDF document. This ensures focused, accurate responses relevant to the specific knowledge source.


### Setting Up

This project requires obtaining API keys for both Gemini 1.5 Flash and Pinecone DB.  Follow the steps below for each service:

**1. Gemini 1.5 Flash API Key:**

*  **Request Access:** Visit [Google AI Platform](https://cloud.google.com/ai-platform) and request access to the Gemini 1.5 Flash API. Be sure to mention your intended use case (RAG chatbot with limited access based on a PDF document).

*  **Create API Key:** Navigate to the **IAM & Admin** section of your Google Cloud project and create an API key for the appropriate service account. 


**2. Pinecone DB API Key:**

*  **Create a Pinecone Account:** Sign up for a free account at [Pinecone](https://www.pinecone.io/). 

*  **Create an API Key:** In the Pinecone dashboard, navigate to the **Project Settings** and generate a new API key.


**Next Steps:**

1. Clone this repository.
2. Update the `.env` files with your obtained API keys for Gemini 1.5 Flash and Pinecone DB.
3. Replace `.pdf` file with your PDF document you want the chatbot to access.
4. Run the `qa_rag.ipynb` notebook line by line.

### Few Infos

LLM: Google 1.5 Flash Latest
Dimensions: 768
embeddings: models/embedding-001


### Dependencies

This project utilizes several Python libraries, make sure to install the required dependencies using `pip install -r requirements.txt` before running the script.

### Usage

Once you've completed the setup steps, replace the question with your own question or create a new invoke line!
chain.invoke({'question': "YOUR ACTUAL QUESTION HERE"})


Hope this helps !!!!
Happy Coding 😅
