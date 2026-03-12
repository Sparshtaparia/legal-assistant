Based on your **actual project structure** and the fact that you are using **Groq LLM API** and **Tavily search API**, here is a **correct, professional README tailored to your repository**.

---

# ⚖️ Crew-AI Legal Assistant

An **AI-powered Legal Assistant** built using **multi-agent architecture** with **CrewAI**, designed to analyze legal scenarios and identify applicable **Indian Penal Code (IPC) sections**, retrieve **legal precedents**, and generate **legal drafts**.

The system uses **Retrieval-Augmented Generation (RAG)** with a **Chroma vector database**, powered by **Groq LLMs** and **Tavily web search**.

---

# 🚀 Features

### 🧠 Multi-Agent Legal Reasoning

The assistant is composed of specialized AI agents:

| Agent                 | Responsibility                                       |
| --------------------- | ---------------------------------------------------- |
| Case Intake Agent     | Understands and structures the user's legal scenario |
| IPC Section Agent     | Identifies applicable IPC sections                   |
| Legal Precedent Agent | Searches for relevant legal precedents               |
| Legal Drafter Agent   | Generates structured legal summaries or drafts       |

---

### 🔎 Semantic Legal Search

IPC laws are stored in a **vector database** enabling:

* semantic search
* contextual retrieval
* accurate legal references

---

### 🌐 Web-based Legal Research

Using **Tavily Search API**, the system can:

* retrieve recent legal information
* find relevant case law
* support precedent analysis

---

# 🏗️ System Architecture

```
User Query
     ↓
Case Intake Agent
     ↓
IPC Section Agent
     ↓
IPC Sections Search Tool
     ↓
Chroma Vector Database
     ↓
IPC JSON Dataset
```

Additional agents extend the pipeline:

```
Legal Precedent Agent → Tavily Search
Legal Drafter Agent → Structured Legal Output
```

---

# 🧰 Tech Stack

| Technology             | Purpose                        |
| ---------------------- | ------------------------------ |
| Python                 | Core language                  |
| CrewAI                 | Multi-agent orchestration      |
| LangChain              | Tool and retrieval integration |
| ChromaDB               | Vector database                |
| HuggingFace Embeddings | Semantic embeddings            |
| Groq API               | LLM inference                  |
| Tavily API             | Web legal search               |
| dotenv                 | Environment configuration      |

---

# 📂 Project Structure

```
CREW-AI LEGAL ASSISTANT
│
├── agents
│   ├── case_intake_agent.py
│   ├── ipc_section_agent.py
│   ├── legal_drafter_agent.py
│   └── legal_precedent_agent.py
│
├── tasks
│   ├── case_intake_task.py
│   ├── ipc_section_task.py
│   ├── legal_drafter_task.py
│   └── legal_precedent_task.py
│
├── tools
│   ├── ipc_sections_search_tool.py
│   └── legal_precedent_search_tool.py
│
├── ipc-json
│   └── ipc_sections.json
│
├── chroma_vectordb
│   └── (vector database files)
│
├── ipc_vectordb_builder.py
├── query_vectordb.py
│
├── crew.py
├── main.py
├── app.py
│
├── .env
├── requirements.txt
└── README.md
```

---

# ⚙️ Setup Instructions

## 1️⃣ Clone the Repository

```bash
git clone https://github.com/yourusername/crew-ai-legal-assistant.git
cd crew-ai-legal-assistant
```

---

# 2️⃣ Create Environment

Using Conda:

```bash
conda create -n legal-env python=3.11
conda activate legal-env
```

---

# 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

# 4️⃣ Configure Environment Variables

Create a `.env` file:

```env
GROQ_API_KEY=your_groq_api_key
TAVILY_API_KEY=your_tavily_api_key

IPC_JSON_PATH=./ipc-json/ipc_sections.json
PERSIST_DIRECTORY_PATH=./chroma_vectordb
IPC_COLLECTION_NAME=ipc_collection
```

---

# 🗄️ Build IPC Vector Database

Before running the system, generate the vector database.

```bash
python ipc_vectordb_builder.py
```

This will:

1. Load IPC sections from JSON
2. Convert them into embeddings
3. Store them inside ChromaDB

---

# ▶️ Run the Legal Assistant

```bash
python main.py
```

Or run the app interface:

```bash
python app.py
```

---

# 🧪 Example Input

```
A man broke into my house at night while my family was sleeping.
He stole jewelry and cash from our bedroom.
When I confronted him, he threatened me with a knife and ran away.
Which IPC sections apply?
```

---

# 📤 Example Output

```json
[
  {
    "section": "IPC Section 441",
    "section_title": "Criminal Trespass"
  },
  {
    "section": "IPC Section 379",
    "section_title": "Theft"
  },
  {
    "section": "IPC Section 506",
    "section_title": "Criminal Intimidation"
  }
]
```

---

# 🧠 Why Multi-Agent Design?

Using **CrewAI agents** allows the system to separate responsibilities:

* reasoning
* retrieval
* research
* drafting

This improves **accuracy, modularity, and scalability** of the legal AI system.

---

# ⚠️ Disclaimer

This project is intended **for educational and research purposes only**.

It **does not constitute legal advice**. Always consult a qualified legal professional for legal matters.

---

# 🔮 Future Improvements

* Add **CrPC and Evidence Act**
* Integrate **Indian Kanoon case law**
* Add **charge prediction models**
* Build **web UI for public interaction**
* Add **court judgment summarization**

---

# 👨‍💻 Author

**Sparsh Taparia**

AI • Software Engineering • Legal AI Systems

---

✅ This README now matches your **actual project architecture, agents, tools, APIs, and folder structure**.

---

If you want, I can also show you **3 improvements that will make this project look like a serious AI research project (the kind that impresses recruiters or professors)**.
