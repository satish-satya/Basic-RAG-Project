
🤖 Basic RAG Chatbot using OpenAI + FAISS
Retrieval-Augmented Generation (RAG) Application
Ask questions from your own PDF, DOCX, and TXT files using OpenAI and FAISS.

🚀 Overview
This project is a simple yet powerful RAG (Retrieval-Augmented Generation) chatbot built with:

🔥 OpenAI GPT Models
🧠 OpenAI Embeddings
⚡ FAISS Vector Database
📄 PDF Support
📝 DOCX Support
📚 TXT Support
The chatbot reads documents, converts them into embeddings, stores them in a FAISS vector database, retrieves relevant information, and generates accurate answers using OpenAI.

✨ Features
✅ Multiple document support

✅ OpenAI Embeddings

✅ GPT-Powered Answers

✅ Semantic Search

✅ FAISS Vector Database

✅ Source Citations

✅ Persistent Storage

✅ Command-Line Interface

✅ Easy to Understand Code

📂 Project Structure
BASIC-RAG-PROJECT/
│
├── .env
├── rag.py
│
├── data/
│   ├── sample.txt
│   ├── sample.pdf
│   └── sample.docx
│
└── vector_store/
    ├── faiss.index
    └── chunks.json
🛠️ Installation
1️⃣ Clone Repository
git clone https://github.com/your-username/basic-rag-project.git

cd basic-rag-project
2️⃣ Create Virtual Environment
py -m venv myenv
Activate:

myenv\Scripts\activate
3️⃣ Install Dependencies
pip install openai python-dotenv numpy faiss-cpu pypdf python-docx
🔑 OpenAI API Setup
Create a .env file:

OPENAI_API_KEY=your_openai_api_key_here
Example:

OPENAI_API_KEY=sk-proj-xxxxxxxxxxxxxxxxxxxxxxxx
📚 Add Documents
Put your files inside the data directory.

data/
├── company_policy.pdf
├── notes.txt
└── employee_handbook.docx
Supported Formats:

File Type	Supported
TXT	✅
PDF	✅
DOCX	✅
XLSX	❌
Images	❌
🧠 Models Used
Embedding Model
text-embedding-3-small
Used to convert document chunks into vectors.

Chat Model
gpt-4.1-mini
Used to generate final answers.

⚙️ How It Works
Documents
    │
    ▼
Document Loading
    │
    ▼
Chunking
    │
    ▼
OpenAI Embeddings
    │
    ▼
FAISS Index
    │
    ▼
User Question
    │
    ▼
Similarity Search
    │
    ▼
Relevant Chunks
    │
    ▼
GPT Response
    │
    ▼
Final Answer
▶️ Run the Application
py rag.py
or

python rag.py
💬 Example
User Question
What is the leave policy?
Assistant Response
Employees are entitled to 20 annual leave days.

Sources: employee_handbook.docx
💾 Saved Vector Store
After the first run:

vector_store/
├── faiss.index
└── chunks.json
These files are reused automatically.

This makes future startup much faster ⚡

🔄 Rebuild Vector Store
Delete:

vector_store/
Then run:

py rag.py
The application will recreate:

✅ Embeddings

✅ FAISS Index

✅ Chunk Metadata

❗ Common Errors
🔴 Authentication Error (401)
Incorrect API key provided
Possible Causes
Invalid API Key
Deleted API Key
Expired API Key
Billing Not Enabled
Solution
✅ Check API key

✅ Update .env

✅ Verify OpenAI billing settings

🔴 No Documents Found
No readable text found in the data folder
Solution
Add:

.txt
.pdf
.docx
files inside the data folder.

📦 Tech Stack
Technology	Usage
Python	Backend
OpenAI	Embeddings + LLM
FAISS	Vector Search
NumPy	Vector Operations
PyPDF	PDF Reading
python-docx	DOCX Reading
dotenv	Environment Variables
🎯 Future Improvements
🌐 Streamlit Web Interface
💬 Chat History
🧠 Conversation Memory
📄 Multiple Knowledge Bases
🐳 Docker Support
🔍 Hybrid Search
📈 Analytics Dashboard
👨‍💻 Author
Satish Kumar
Learning:

Python
OpenAI APIs
FAISS
RAG Systems
Generative AI
AI Application Development
⭐ If you found this project useful, consider giving it a star!
