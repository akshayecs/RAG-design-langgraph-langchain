# RAG Application with LangChain & LangGraph

A TypeScript-based Retrieval-Augmented Generation (RAG) project that combines **LangChain, LangGraph, OpenAI, and Tavily** to retrieve relevant information and generate AI-powered answers.

## Tech Stack

- TypeScript
- LangChain & LangGraph
- OpenAI API
- Tavily Search
- LangSmith (optional monitoring)

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/astrocodelp/langgraph-rag-example.git
cd langgraph-rag-example
```

### 2. Install Dependencies

Make sure Node.js and pnpm are installed.

```bash
npm install -g pnpm
pnpm install
```

### 3. Configure Environment Variables

Create a `.env` file in the project root:

```env
OPENAI_API_KEY=your_openai_api_key
TAVILY_API_KEY=your_tavily_api_key

# Optional: LangSmith tracing
LANGCHAIN_TRACING_V2=true
LANGSMITH_API_KEY=your_langsmith_api_key
LANGCHAIN_PROJECT=langgraph-rag-demo
LANGCHAIN_CALLBACKS_BACKGROUND=true
```

Add your own API keys before running the application.

### 4. Run the Application

```bash
pnpm start "What is LangChain?"
```

The application executes `graph.ts`, retrieves relevant information, and generates an answer using the RAG workflow.

## How It Works

The application follows a simple two-step workflow:

1. **Retrieve:** Finds relevant documents based on the user's question.
2. **Generate:** Uses the retrieved information to produce a contextual response.

## Project Structure

```text
├── graph.ts       # Main RAG workflow
├── graph.png      # Workflow visualization
├── package.json   # Dependencies and scripts
├── .env           # Environment configuration
└── README.md      # Project documentation
```

## Possible Improvements

- Add more documents to the knowledge base.
- Experiment with different embedding models.
- Customize retrieval strategies.
- Expose the RAG workflow through a REST API.
- Integrate additional data sources.

## Contributing

Suggestions and contributions are welcome. Feel free to fork the repository and submit a pull request.

## License

Released under the MIT License. See [LICENSE](LICENSE) for details.
