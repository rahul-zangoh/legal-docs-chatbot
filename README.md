## Feature Branch Changes
- Added chatbot testing notes
- Updated project description

## Testing Git Workflow
This section is updated from main branch by another developer.


# ⚖️ Law Assistant AI – RAG-based Legal Document Chatbot

A **Generative AI web app** powered by **FastAPI** + **LLM (Hugging Face)** that allows users to **upload legal documents** (PDF/TXT), ask natural language questions, and get **context-aware, intelligent answers** using a **Retrieval-Augmented Generation (RAG)** pipeline.

---


## 🎥 Demo Video

[![Watch the demo](https://via.placeholder.com/800x450.png?text=▶️+Watch+Demo+Video)](https://drive.google.com/file/d/1UqxArDxRQ9FHO_uG9jWRKETBywb_zEDg/view?usp=sharing)


  

*👉 Upload a document, ask a question, and get legal context-based answers within seconds.*

---
## 📸 Screenshots

### 📝 Input Screen
Upload your `.pdf` or `.txt` legal document and ask your question.

![Input Screenshot](assets/Screenshot%20%2857%29.png "Input UI")



---

### 📤 Output Screen
Get AI-generated context-aware answers based on your document.
![Input Screenshot](assets/Screenshot%20%2858%29.png "Output UI")


## ✨ Features

✅ Upload legal documents in `.pdf` or `.txt` format  
✅ Ask questions in plain English  
✅ Answers generated using **Mistral 7B** via Hugging Face Inference API  
✅ Embedded document chunking with **FAISS**  
✅ Clean, minimal UI with Jinja2  
✅ Modular & extensible codebase  

---

## 💡 Tech Stack & Architecture

| Layer                | Description                                                                 |
|---------------------|-----------------------------------------------------------------------------|
| ⚙️ Backend           | [FastAPI](https://fastapi.tiangolo.com/) – Handles routing and logic       |
| 📄 Templating        | Jinja2 – Renders HTML pages                                                 |
| 🧠 LLM Integration   | Hugging Face Inference API – Mistral 7B for answers                         |
| 📚 Vector Store      | FAISS – Stores document embeddings and performs similarity search           |
| 🧾 RAG Pipeline      | 1. Chunk documents → 2. Embed with SentenceTransformer → 3. Match & query    |

---

## 📦 Installation & Setup

```bash
# 1. Clone the repository
git clone https://github.com/rahulbamnuya/legal-docs-chatbot.git
cd legal-docs-chatbot

# 2. Create a virtual environment
python -m venv venv
# Windows:
venv\Scripts\activate
# Linux/macOS:
source venv/bin/activate

# 3. Install required packages
pip install -r requirements.txt

# 4. Add your Hugging Face API Key
# Create a `.env` file in root:
echo HUGGINGFACEHUB_API_TOKEN=your_token_here > .env

# 5. Run the app
uvicorn main:app --reload
## 📁 Project Structure
.
├── main.py               # FastAPI app
├── templates/            # HTML templates (Jinja2)
│   ├── ask.html
│   └── upload.html
├── static/               # CSS files
├── utils.py              # Document parsing & embedding
├── vector_store/         # FAISS vector DB
├── requirements.txt
└── .env

## 🔐 Environment Variables

Create a `.env` file in the root directory with the following:


---

## 🧪 How It Works

- **Upload Document**: The app supports `.pdf` and `.txt` file uploads.
- **Chunking**: It splits documents into small readable sections.
- **Embedding**: Each section is embedded using SentenceTransformer and stored in FAISS.
- **Ask Questions**: Your query is embedded and compared to chunks.
- **Answer**: The most relevant chunk is sent to the Mistral 7B model with your question using the RAG strategy.

---

## 🧠 Future Improvements

- Add support for multi-document retrieval  
- Integrate Pathway SDK for streaming data pipelines  
- Extend support to image-based PDFs (OCR)  

---

## 📤 Submission Notes (for Hackathon)

✅ Uses Pathway-compatible RAG pipeline  
✅ LLM is used with contextual augmentation  
✅ Hosted on GitHub with detailed README  
✅ Demo video included  
✅ Modular and original project  
✅ `.env` and `venv/` excluded in `.gitignore`  

---

## 👨‍💻 Author

Made with ❤️ by **Rahul Bamaniya hh**
