# 🔗 Chainlit Chatbot — Langchain & OpenAI Powered AI Assistant

An advanced conversational AI chatbot built with **Chainlit**, **LangChain**, and **OpenAI**. This project demonstrates chat profiles, custom system prompts, and interactive settings to dynamically adjust the AI's behavior in real-time.

---

## ✨ Features

- **Chat Profiles** — Switch between 3 predefined AI personas:
  - 🤖 *Normal*: General helpful assistant based on common knowledge
  - 📚 *Factful*: Strict adherence to verified facts and data
  - 🎨 *Creative*: Imaginative, storytelling, and light-hearted responses
- **Live Settings UI** — Adjust model parameters straight from the chat interface:
  - LLM Model selection (e.g., `gpt-3.5-turbo`)
  - Temperature slider (0.0 to 2.0)
  - Message streaming toggle
  - Memory window size
- **LangChain Memory** — Uses `ConversationBufferWindowMemory` to maintain context over configurable conversation lengths
- **Message Streaming** — Real-time token streaming using OpenAI's async streaming API

## 🛠️ Tech Stack

| Layer       | Technology                              |
|-------------|-----------------------------------------|
| Framework   | Chainlit                                |
| AI Pipeline | LangChain (langchain-core, langchain-openai) |
| Models      | OpenAI GPT API                          |
| Config      | Poetry, `pyproject.toml`                |

## 📁 Project Structure

```
chainlit-chatbot-2023/
├── app.py                  # Main Chainlit application logic
├── prompts.py              # System prompts for Factful, Normal, and Creative modes
├── chainlit.md             # Welcome screen markdown
├── pyproject.toml          # Poetry dependencies
├── poetry.lock             # Dependency lockfile
└── .chainlit/              # Chainlit config and translations
    ├── config.toml
    └── translations/en-US.json
```

## 🚀 Getting Started

### Prerequisites

- Python 3.9+
- [Poetry](https://python-poetry.org/)
- OpenAI API Key

### Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/chainlit-chatbot-2023.git
cd chainlit-chatbot-2023

# Install dependencies using Poetry
poetry install

# Set your OpenAI API key
export OPENAI_API_KEY="your-api-key-here"

# Run the Chainlit server
poetry run chainlit run app.py -w
```

The application will launch in your browser at `http://localhost:8000/`

## 💬 Usage

1. **Select a Profile**: Upon launching, you will be prompted to choose a chat profile (Normal, Factful, or Creative). You can change this at the start of any new chat.
2. **Configure Settings**: Click the settings icon to adjust the Model, Temperature, Window Size, or toggle Streaming.
3. **Chat**: Send messages and receive real-time streaming responses tailored to the active profile's system prompt.

---

> **Note:** This project was built in 2023 as part of a founder timeline, showcasing rapid AI prototyping using modern frameworks like Chainlit and LangChain.
