# RAG-QnA

# PDF Question-Answering System

A sophisticated document analysis system that enables users to upload PDFs and ask questions about their content using RAG (Retrieval-Augmented Generation) and LLM technology.

## 🚀 Features

- **PDF Processing**: Upload and process multiple PDF documents (20-30 pages each)
- **Intelligent QA**: Ask questions and get accurate, context-aware responses
- **Citation Support**: Answers include relevant page numbers and sections as citations
- **Modern UI**: Clean, responsive chat interface for seamless interaction
- **Scalable Backend**: FastAPI-based backend with efficient PDF processing
- **Vector Search**: Advanced embedding-based document retrieval system

## 🛠️ Tech Stack

### Backend
- FastAPI (Python web framework)
- PyPDF2 (PDF processing)
- Sentence-Transformers (Text embeddings)
- ChromaDB (Vector database)
- LangChain (RAG pipeline)
- OpenAI API (LLM integration)

### Frontend
- Next.js/React
- TypeScript
- Tailwind CSS
- Axios (API client)

## 📋 Prerequisites

Before you begin, ensure you have the following installed:
- Python 3.8+
- Node.js 16+
- npm or yarn
- Git

## 🔧 Installation

1. **Clone the Repository**
```bash
git clone https://github.com/enigma-kun/pdf-qa-system.git
cd pdf-qa-system
```

2. **Backend Setup**
```bash
# Navigate to backend directory
cd backend

# Create virtual environment
python -m venv venv

# Activate virtual environment
# On Windows:
.\venv\Scripts\activate
# On Unix or MacOS:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Create .env file
cp .env.example .env
# Edit .env and add your OpenAI API key
```

3. **Frontend Setup**
```bash
# Navigate to frontend directory
cd frontend

# Install dependencies
npm install

# Create environment file
cp .env.example .env.local
```

## 🚀 Running the Application

1. **Start Backend Server**
```bash
cd backend
source venv/bin/activate  # or .\venv\Scripts\activate on Windows
uvicorn app.main:app --reload
```

2. **Start Frontend Development Server**
```bash
cd frontend
npm run dev
```

3. **Access the Application**
- Frontend: http://localhost:3000
- Backend API: http://localhost:8000
- API Documentation: http://localhost:8000/docs

## 📁 Project Structure

```
pdf-qa-system/
├── backend/
│   ├── app/
│   │   ├── api/          # FastAPI routes
│   │   ├── models/       # Pydantic models
│   │   ├── services/     # Business logic
│   │   └── utils/        # Helper functions
│   ├── tests/            # Backend tests
│   └── uploads/          # PDF storage
│
└── frontend/
    ├── src/
    │   ├── components/   # React components
    │   ├── pages/        # Next.js pages
    │   ├── services/     # API integration
    │   └── styles/       # CSS styles
    └── public/           # Static assets
```

## 🔍 Key Components

### Backend Services

1. **PDF Service**
   - Handles PDF upload and text extraction
   - Manages document chunking and preprocessing

2. **Embedding Service**
   - Generates text embeddings using Sentence-Transformers
   - Manages vector database operations

3. **QA Service**
   - Implements RAG pipeline
   - Handles question processing and answer generation

### Frontend Components

1. **File Upload**
   - Drag-and-drop PDF upload
   - File validation and progress tracking

2. **Chat Interface**
   - Real-time question-answering
   - Conversation history management
   - Citation display

## 🧪 Testing

1. **Backend Tests**
```bash
cd backend
pytest
```

2. **Frontend Tests**
```bash
cd frontend
npm test
```

## 📝 API Documentation

### Key Endpoints

1. **PDF Upload**
   - `POST /api/upload`
   - Accepts multiple PDF files
   - Returns upload confirmation

2. **Question Answering**
   - `POST /api/ask`
   - Accepts question in request body
   - Returns answer with citations

For detailed API documentation, visit http://localhost:8000/docs when the backend server is running.

## 🔒 Environment Variables

### Backend (.env)
```
OPENAI_API_KEY=your_openai_api_key
MAX_FILE_SIZE=10485760
ALLOWED_EXTENSIONS=.pdf
```

### Frontend (.env.local)
```
NEXT_PUBLIC_API_URL=http://localhost:8000/api
```

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👏 Acknowledgments

- OpenAI for their powerful language models
- Sentence-Transformers for text embedding capabilities
- The FastAPI and Next.js communities for excellent documentation

## 📧 Contact

Your Name - shubhamio.exe@gmail.com
Project Link: https://github.com/enigma-kun/pdf-qa-system
