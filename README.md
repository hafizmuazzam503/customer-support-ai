# Customer Support AI Assistant

An AI-powered customer support application designed to handle customer inquiries, answer frequently asked questions, manage orders, recommend products, and maintain customer context through a web-based conversational interface.

The project combines a responsive frontend with a Python backend and a centralized AI Supervisor to provide a unified customer support experience.

## Key Features

- **Intelligent FAQ Responses:** Retrieves relevant information from a knowledge base to answer common customer questions.
- **Order Management:** Supports order creation and the storage of customer order information.
- **Customer Memory:** Maintains conversation history and customer context to support more personalized interactions.
- **Product Recommendations:** Suggests relevant products based on available product and business information.
- **Centralized AI Supervisor:** Uses a single Supervisor to coordinate FAQ retrieval, product suggestions, order handling, and customer memory.
- **Conversational Interface:** Provides a web-based chat experience for customers to interact with the assistant.
- **Backend API:** Connects the frontend to the AI processing and data-management services.
- **Semantic Knowledge Retrieval:** Uses vector-based retrieval to identify relevant information from stored knowledge and conversation data.

## System Architecture

The application follows a centralized architecture in which a single Supervisor processes incoming customer messages and coordinates the appropriate operations.

```text
Customer
   |
   v
Web Chat Interface
   |
   v
FastAPI Backend
   |
   v
AI Supervisor
   |
   +-- FAQ Retrieval
   |
   +-- Product Suggestions
   |
   +-- Order Management
   |
   +-- Customer Memory
   |
   v
Response Generation
   |
   v
Customer
```

PostgreSQL is used for structured application data, while ChromaDB supports semantic retrieval from the knowledge base and relevant conversation information.

## Technology Stack

| Component | Technology |
|---|---|
| Frontend | HTML, CSS, JavaScript |
| Backend API | Python, FastAPI |
| AI Orchestration | LangGraph |
| Language Model Integration | LangChain, Gemini API |
| Relational Database | PostgreSQL |
| Database ORM | SQLAlchemy |
| Vector Database | ChromaDB |
| Semantic Embeddings | Sentence Transformers |

## How It Works

1. A customer submits a message through the web interface.
2. The FastAPI backend receives the message and retrieves relevant customer context.
3. The central AI Supervisor determines the appropriate support operation.
4. The system retrieves relevant FAQ information, suggests products, handles order operations, or updates customer memory as needed.
5. The assistant generates a concise, context-aware response.
6. Conversation and relevant application data are persisted through the configured storage components.

## Project Structure

The project is organized into the following main components:

- `app/` — Application components and supporting functionality.
- `core/` — Core application logic and service integrations.
- `frontend/` — Web-based customer support interface.
- `.env.example` — Example environment configuration.
- `README_WEBSITE.md` — Additional website-related documentation.

## Configuration

1. Clone the repository.
2. Install the project's Python dependencies using its dependency manifest.
3. Configure the required environment variables using `.env.example` as a reference.
4. Set up the required PostgreSQL database and ChromaDB storage.
5. Configure the required AI provider credentials.
6. Start the backend and frontend according to the project's configuration.

Keep API keys, database credentials, and other sensitive configuration values out of source control.

## Project Goals

The goal is to build a practical, extensible customer support system that combines conversational AI, knowledge retrieval, customer context, and operational workflows within a single application.

By consolidating these capabilities under one Supervisor, the project aims to keep the architecture straightforward while supporting multiple customer service tasks.

## License

Add the appropriate license information before distributing the project publicly.
