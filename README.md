📚 Scholar Chat Bot with PDFs 📚

Overview

Scholar Chat Bot is an AI-powered application that allows users to interact with academic and research PDFs using natural language queries. By leveraging Google Gemini AI, FAISS for vector storage, and Streamlit for the user interface, this tool helps users extract key insights from scientific documents efficiently.

Features\
✅ Upload multiple PDF documents (up to 200MB per file)\
✅ Extract and process text from PDFs using PyPDF2\
✅ Split text into manageable chunks for efficient processing\
✅ Store and retrieve embeddings using FAISS\
✅ Perform intelligent Q&A using Google Gemini AI\
✅ Interactive web-based chat interface using Streamlit\

Tech Stack\
•	Programming Language: Python=3.10 \
•	Framework: Streamlit\
•	AI Model: Google Gemini AI (via langchain_google_genai)\
•	Vector Storage: FAISS\
•	Text Processing: PyPDF2, RecursiveCharacterTextSplitter\
•	Environment Management: dotenv\


Installation
1.	Clone the repository\
bash\

git clone https://github.com/your-repo/scholar-chat-bot.git\
cd scholar-chat-bot\
3.	Create a virtual environment (optional but recommended)\

bash\

python -m venv venv\
source venv/bin/activate   # On macOS/Linux\
venv\Scripts\activate      # On Windows\

4.	Install dependencies\
bash\

pip install -r requirements.txt\
5.	Set up API key for Google AI\
o	Create a .env file in the project root\
o	Add your Google API Key:\

GOOGLE_API_KEY=your_api_key_here

Usage
1.	Run the Streamlit app\
bash\

streamlit run app.py

2.	Upload your PDF files
3.	Enter a research-related query
4.	Receive detailed responses based on the document content\
   
** How It Works
1.	PDF Upload: Users upload PDFs via the Streamlit UI.
2.	Text Extraction: PyPDF2 extracts text from all pages.
3.	Text Chunking: RecursiveCharacterTextSplitter divides content into smaller chunks.
4.	Embedding Generation: Google Gemini AI converts text into embeddings.
5.	Vector Storage: FAISS stores embeddings for efficient retrieval.
6.	Question Answering: User queries are matched with relevant text chunks, and Google Gemini AI generates responses. 
   
Example Query \
User Input:

What are the key takeaways from the Clinical Knowledge Embeddings research?


Bot Response:
•	Clinical knowledge embeddings provide a unified representation of clinical knowledge by integrating seven medical vocabularies.
•	These embeddings were validated through a phenotype risk score analysis involving 4.57 million patients from Clalit Healthcare Services.
•	Inter-institutional clinician panels confirmed the alignment of embeddings across 90 diseases and 3,000 clinical codes.
•	The model improves AI-based clinical vocabulary integration for patient-level models.

Future Enhancements
•	Support for more document formats (e.g., Word, Excel)
•	Multi-document summarization
•	Integration with citation/reference management tools
License
This project is open-source and available under the MIT License.

