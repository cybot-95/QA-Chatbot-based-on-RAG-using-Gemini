## RAG-based QA Chatbot with Gemini 1.5 Flash and Pinecone DB

This repository implements a Retrieval-Augmented Generation (RAG) chatbot powered by Google's Gemini 1.5 Flash large language model (LLM) and Pinecone's vector database. This chatbot leverages the strengths of both components:

* **Gemini 1.5 Flash:** Delivers powerful text generation capabilities with a long context window and multilingual support.
* **Pinecone DB:** Efficiently stores and retrieves relevant information from a provided PDF document, enabling the chatbot to access and answer questions based on its content.

**Key Feature:**

The chatbot is specifically designed to only answer questions based on the information contained within a provided PDF document. This ensures focused, accurate responses relevant to the specific knowledge source.


### Setting Up

This project requires obtaining API keys for both Gemini 1.5 Flash and Pinecone DB.  Follow the steps below for each service:

**1. Gemini 1.5 Flash API Key:**

*  **Request Access:** Visit [Google AI Platform](https://cloud.google.com/ai-platform) and request access to the Gemini 1.5 Flash API. Be sure to mention your intended use case (RAG chatbot with limited access based on a PDF document).

*  **Enable Billing:** Once approved, enable billing for your Google Cloud project. 

*  **Create API Key:** Navigate to the **IAM & Admin** section of your Google Cloud project and create an API key for the appropriate service account. 


**2. Pinecone DB API Key:**

*  **Create a Pinecone Account:** Sign up for a free account at [Pinecone](https://www.pinecone.io/). 

*  **Create an API Key:** In the Pinecone dashboard, navigate to the **Project Settings** and generate a new API key.


**Next Steps:**

1. Clone this repository.
2. Update the `config.py` file with your obtained API keys for Gemini 1.5 Flash and Pinecone DB.
3. Replace `path/to/your/document.pdf` with the actual path to the PDF document you want the chatbot to access.
4. Run the `run_chatbot.py` script to start the chatbot.


### Dependencies

This project utilizes several Python libraries:

* `transformers`
* `pinecone`
* [Library for PDF processing (Choose one based on your preference)]
    * `PyMuPDF`
    * `pdfminer.six`

Make sure to install the required dependencies using `pip install -r requirements.txt` before running the script.

### Usage

Once you've completed the setup steps, run the following command to start the chatbot:

```bash
python run_chatbot.py
```

This will launch the chatbot interface where you can ask questions about the provided PDF document. Remember, the chatbot will only answer questions based on the information contained within that document.

**Example Usage:**

* User: What are the key features of the product mentioned in the document?
* Chatbot: (Provides a response summarizing the product features based on the PDF)

### Additional Notes

* This code provides a basic example of a RAG chatbot. You can extend it further by adding functionalities like handling different question formats or implementing a conversation history.
* Consider exploring advanced techniques for text processing and information retrieval to improve the accuracy and efficiency of the chatbot.


We hope this repository helps you build a powerful RAG chatbot tailored to answer questions from a specific document!
