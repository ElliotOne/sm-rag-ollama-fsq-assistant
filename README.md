# sm-rag-ollama-fsq-assistant

A Retrieval-Augmented Generation (RAG) FAQ assistant built with C# and Ollama, demonstrating local AI-powered question answering using company policy data. This console application performs keyword-based retrieval to find relevant context and generates responses via a chat interface with conversation history.

## Prerequisites

- [.NET 10.0 SDK](https://dotnet.microsoft.com/download/dotnet/10.0) or later
- [Ollama](https://ollama.ai/) installed and running locally
- A compatible model downloaded in Ollama (e.g., gpt-oss:20b)

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/sm-rag-ollama-fsq-assistant.git
   cd sm-rag-ollama-fsq-assistant
   ```

2. Restore NuGet packages:
   ```bash
   dotnet restore
   ```

## Setup

1. **Install and Start Ollama:**
   - Download and install Ollama from [ollama.ai](https://ollama.ai/)
   - Launch Ollama and pull the required model (e.g., `ollama pull gpt-oss:20b`)
   - Start the Ollama server (typically runs on http://localhost:11434)

2. **Verify Model Configuration:**
   - Ensure the model is loaded and the server is running on the expected endpoint
   - The application is configured to connect to `http://localhost:11434`

## Usage

Run the console application to start the FAQ assistant:

```bash
dotnet run --project RAGOllamaFAQAssistant
```

The application will enter a chat loop where you can ask company-related questions. Type 'Exit' to quit.

## Features

### RAG-Based Question Answering
Demonstrates Retrieval-Augmented Generation by loading company policy data, performing keyword-based retrieval to find the most relevant paragraph, and using it as context for AI-generated answers.

### Chat History Integration
Maintains conversation history to provide context-aware responses, allowing for follow-up questions and coherent dialogue.

### Streaming Responses
Outputs AI responses in real-time as they are generated, providing a smooth interactive experience.

### Local AI Inference
Utilizes Ollama for running AI models locally, ensuring privacy and offline capability.

## Dependencies

- OllamaSharp (for Ollama API client)
- Microsoft.KernelMemory v0.98.250508.3

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
