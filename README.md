# 🚀 StartupBuddy Backend

This is the backend for the **StartupBuddy** chatbot, developed using **FastAPI** and deployed on **Render**. It uses **Google Gemini API** for natural language processing and **Pinecone** for vector similarity search. The system is designed to respond intelligently to user queries using advanced language models and a memory buffer.

---

## 💠 Tech Stack

- **FastAPI** – High-performance Python web framework for APIs  
- **Uvicorn** – ASGI server for running FastAPI  
- **Pinecone** – Vector database for semantic search  
- **LangChain** – Manages chains and memory for LLM interactions  
- **Google Generative AI (Gemini)** – Provides embeddings and text generation  
- **python-dotenv** – For managing environment variables  

---

## 📁 Project Structure

```
startupbuddy-backend/
│
├── main.py               # Entry point for FastAPI app
├── pinecone_utils.py     # Pinecone initialization and utility functions
├── requirements.txt      # Python dependencies
├── Procfile              # Render deployment instruction
└── README.md             # Project documentation (this file)
```

---

## 🔧 Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/startupbuddy-backend.git
cd startupbuddy-backend
```

### 2. Install Dependencies

Make sure Python 3.9+ is installed. Then run:

```bash
pip install -r requirements.txt
```

### 3. Environment Variables

Create a `.env` file in the root directory with the following keys:

```
GOOGLE_API_KEY=your_google_api_key
PINECONE_API_KEY=your_pinecone_key
PINECONE_INDEX_NAME=your_index_name
```

---

## 🚀 Run the App Locally

```bash
uvicorn main:app --reload
```

Access the app at: `http://127.0.0.1:8000`  
Swagger Docs: `http://127.0.0.1:8000/docs`

---

## 🌐 Deployment (Render)

This backend is deployed on [Render](https://render.com).

### 👢 Files Used for Deployment

- `Procfile` – Tells Render how to run the app:
  ```
  web: uvicorn main:app --host=0.0.0.0 --port=10000
  ```

- `requirements.txt` – Contains all dependencies needed for deployment

---

## ✨ API Endpoints

| Method | Endpoint  | Description                        |
|--------|-----------|------------------------------------|
| POST   | `/chat`   | Sends a user query for processing  |
| POST   | `/embed`  | Converts text into vector embeddings |

_Note: You can expand this table with real endpoints from your `main.py`._

---


## 📦 Dependencies

Main libraries used (from `requirements.txt`):

```
fastapi
uvicorn[standard]
python-dotenv
pinecone
streamlit
langchain-google-genai
google-generativeai
```

---

## 📃 License

This project is for educational and internal use. Contact the author for licensing details.

---

## 👨‍💼 Author

Developed by [Balaji V].  
If you find this useful, feel free to star the repo and contribute!

