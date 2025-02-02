CHAT_WITH_DOC

Overview

CHAT_WITH_DOC is a Streamlit-based web application that enables users to upload PDF documents, index their contents using Pinecone, and interact with them by asking questions. The application integrates LangChain for embedding generation, Google Generative AI (Gemini) for answering queries, and Pinecone for efficient vector storage and retrieval.

Features

📂 Upload PDF Documents: Users can upload PDF files to the application.

📤 Document Indexing: Extracts text from the uploaded PDFs and indexes it into Pinecone.

💬 Ask Questions: Users can ask questions related to the document’s content and receive AI-generated answers.

📝 Query History: Maintains a record of user queries and responses.

📜 Document Preview: Displays the first 500 characters of the uploaded document as a preview.

🔒 Session Management: Caches uploaded documents and indexed data for better performance.

Technologies Used

Python: Core programming language.

Streamlit: Web framework for interactive UI.

Pinecone: Vector database for document indexing and retrieval.

LangChain: Framework for embedding generation and chunking.

PyPDF2: Library for extracting text from PDFs.

Google Generative AI (Gemini): Used to generate AI-based answers.

dotenv: Manages environment variables securely.

Installation

Clone the repository:

git clone https://github.com/yourusername/your-repo-name.git
cd your-repo-name

Create and activate a virtual environment (optional):

python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate

Install the required dependencies:

pip install -r requirements.txt

Set up environment variables:

Create a .env file in the project root and add the following keys:

PINECONE_API_KEY=<your_pinecone_api_key>
GOOGLE_API_KEY=<your_google_api_key>
INDEX_NAME=<your_pinecone_index_name>

Run the Streamlit application:

streamlit run app.py

Usage

Upload Document:

Navigate to the sidebar and upload a PDF file.

The document will be processed and indexed into Pinecone.

Ask Questions:

Enter a query in the text input field under the "Chat" tab and click "Submit".

The application retrieves relevant document chunks and generates an answer.

View Document Details:

Switch to the "Document Details" tab to view metadata about the uploaded document.

Review Query History:

Switch to the "Query History" tab to see past queries and responses.

File Structure

├── app.py                # Main application code
├── requirements.txt      # Python dependencies
├── .env                  # Environment variables (ignored in Git)
├── README.md             # Project documentation
└── ...                   # Other files

Dependencies

Python >= 3.7

Streamlit

PyPDF2

Pinecone

LangChain

Google Generative AI SDK

dotenv

Known Issues

File Size Limit: Ensure uploaded PDFs are within the allowed size for efficient processing.

API Limits: Query responses are subject to Pinecone and Google Generative AI API limits.

Future Enhancements

Support for additional file formats (e.g., DOCX, TXT).

Improved error handling and logging.

Integration with other LLMs and embedding models.

Enhanced UI with better document navigation and search options.
