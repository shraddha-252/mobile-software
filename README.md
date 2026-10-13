# ✨ Nova AI — Voice Assistant

Nova AI is a web-based AI assistant designed to provide natural conversations through text and voice. The project aims to combine a modern chatbot interface, local Large Language Model (LLM) integration, and document-based question answering in one platform.

## 🚀 Features

* **User Authentication:** Login and registration using Django.
* **AI Chatbot:** Interactive chat interface for communicating with an AI assistant.
* **Local LLM Integration:** Designed to run language models locally using Ollama.
* **Voice Input:** Speech-to-text using browser speech recognition.
* **Voice Output:** Text-to-speech for spoken AI responses.
* **PDF Document Support:** Upload documents and retrieve relevant information using Retrieval-Augmented Generation (RAG).
* **Responsive UI:** Interface designed for desktop and mobile devices.
* **Progressive Web App (PWA):** Planned support for installing the application on compatible devices.

## 🛠️ Tech Stack

| Component           | Technology                            |
| ------------------- | ------------------------------------- |
| Frontend            | HTML, CSS, JavaScript                 |
| Backend             | Python, Django, Django REST Framework |
| Local LLM Runtime   | Ollama                                |
| AI Model            | Configurable local language model     |
| Document Processing | PyPDF                                 |
| Vector Database     | ChromaDB                              |
| Embeddings          | Sentence Transformers                 |
| Voice Features      | Web Speech API                        |
| Database            | SQLite for local development          |

## 📁 Project Structure

```text
nova-ai/
├── assistant/
│   ├── views.py
│   ├── llm.py
│   └── rag.py
├── config/
│   ├── settings.py
│   └── urls.py
├── templates/
│   ├── login.html
│   ├── register.html
│   └── index.html
├── static/
│   ├── css/
│   ├── js/
│   ├── manifest.json
│   └── service-worker.js
├── manage.py
├── requirements.txt
├── .env.example
└── README.md
```

*Note: The structure may change as development progresses.*

## ⚙️ Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
cd YOUR-REPOSITORY
```

Replace the repository URL with your actual GitHub repository URL.

### 2. Create a virtual environment

```bash
python -m venv .venv
```

Activate it on Windows:

```powershell
.\.venv\Scripts\Activate.ps1
```

### 3. Install dependencies

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### 4. Install Ollama

Download Ollama from https://ollama.com/download.

Pull a supported local language model:

```bash
ollama pull llama3.2:3b
```

Start the model:

```bash
ollama run llama3.2:3b
```

Check that Ollama is running before testing the Django chatbot integration.

### 5. Configure environment variables

Copy `.env.example` to `.env` and configure the required values, including the Django secret key and local model settings.

Do not commit `.env` or other files containing secrets to GitHub.

### 6. Run database migrations

```bash
python manage.py migrate
```

### 7. Start the development server

```bash
python manage.py runserver
```

Open the local application at:

http://127.0.0.1:8000/

## 🧠 How It Works

1. The user signs in to the application.
2. The user sends a message through the chatbot interface or uses voice input.
3. Django processes the request and communicates with the configured local LLM.
4. If document-based retrieval is enabled, relevant PDF content is retrieved to provide additional context.
5. The generated response is displayed in the chat interface.
6. If voice output is enabled, the browser can read the response aloud.

## 🔒 Security

* Keep passwords and API credentials out of source control.
* Use Django's authentication and CSRF protection.
* Restrict access to private conversations and uploaded documents.
* Configure HTTPS and production security settings before public deployment.
* Keep local model endpoints private unless secure remote access is explicitly configured.

## 🗺️ Development Roadmap

* [x] Initial login page design
* [x] Initial Django login and registration integration code
* [ ] Complete authentication integration
* [ ] Build the chatbot dashboard
* [ ] Integrate the local LLM
* [ ] Implement voice input and output
* [ ] Add PDF uploads and RAG-based question answering
* [ ] Save conversation history
* [ ] Improve mobile and PWA support
* [ ] Deploy with HTTPS and a custom domain

## 🎯 Project Goal

The goal of Nova AI is to create a personal AI assistant that supports text conversations, voice interactions, and document-based question answering while prioritizing local model execution and user privacy.

## 📌 Project Status

**Status:** In Development

The login interface is the initial development stage. Chatbot integration, document retrieval, and deployment will be implemented progressively.

## 📄 License

This project is intended for educational and development purposes. Add a license file if you plan to distribute or open-source the project.
