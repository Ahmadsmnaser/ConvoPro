# ConvoPro (Local ChatGPT Clone)

A local, private, and fully functional ChatGPT clone built with **Streamlit**, **Ollama**, **LlamaIndex**, and **MongoDB**. This application allows you to chat with various local LLMs using Ollama, while persisting your conversation history seamlessly via MongoDB.

## Features

- **Local LLM Execution**: Uses [Ollama](https://ollama.com/) to run open-source large language models completely locally. No data leaves your machine!
- **ChatGPT-like UI**: A familiar and intuitive chat interface built with Streamlit, complete with a sidebar for managing past conversations.
- **Persistent Chat History**: All conversations are stored in a local MongoDB database, allowing you to resume old chats anytime.
- **Dynamic Model Selection**: Easily switch between any installed Ollama model via a dropdown menu.
- **Auto-generated Titles**: Automatically generates concise and relevant titles for your conversations.

## Prerequisites

Before running the application, make sure you have the following installed:

1. **Python 3.10+**
2. **MongoDB**: Make sure you have a local MongoDB instance running (usually on `localhost:27017`).
3. **Ollama**: Install [Ollama](https://ollama.com/) and download at least one model (e.g., run `ollama run llama3` in your terminal).

## Installation

1. **Clone the repository:**
   ```bash
   git clone <your-repository-url>
   cd ConvoPro
   ```

2. **Create and activate a virtual environment (recommended):**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. **Install the dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Environment Variables:**
   Ensure you have a `.env` file in the root directory to specify configurations like `MONGO_URI` or `OLLAMA_URL` if they differ from the defaults.

## Usage

Start the Streamlit application by running the following command:

```bash
streamlit run main.py
```

Open your browser and navigate to the local URL provided by Streamlit (usually `http://localhost:8501`). You can select your preferred model from the dropdown menu and start chatting!

## Technologies Used

- [Streamlit](https://streamlit.io/): For the frontend web interface.
- [Ollama](https://ollama.com/): For local LLM inference.
- [LlamaIndex](https://www.llamaindex.ai/): For LLM orchestration.
- [MongoDB](https://www.mongodb.com/) / [PyMongo](https://pymongo.readthedocs.io/): For database and conversation persistence.
- [Pydantic](https://docs.pydantic.dev/): For settings and data validation.

## License

This project is open-source and available under the MIT License.
