# AI Book Assistant (Telegram Bot with LangChain + Ollama)

This project is an intelligent Telegram chatbot that answers questions based on the content of a specific book. It uses [LangChain](https://github.com/langchain-ai/langchain) for building a Conversational Retrieval QA system, [Ollama](https://ollama.com/) for running local LLMs (specifically DeepSeek-R1), and [FAISS](https://github.com/facebookresearch/faiss) for efficient document retrieval. It turns any PDF into a smart conversational assistant directly on Telegram!


## Features

-  Telegram bot interface for real-time interaction
-  PDF-based document question answering (QA)
-  Powered by `deepseek-r1:1.5b` model from Ollama
-  Uses FAISS for semantic search across book chunks
-  Maintains conversational context via LangChain's `ConversationalRetrievalChain`
-  Provides accurate answers based only on the book—no hallucinations


##  How It Works

1. Loads and splits the book into chunks.
2. Embeds each chunk using DeepSeek-R1 and stores them in a FAISS vector store.
3. Starts a Telegram bot that listens for messages.
4. Uses LangChain's QA chain to:
   - Retrieve the most relevant text chunks.
   - Answer based on content found in the book only.
5. Maintains chat history to provide context-aware answers.



##  Installation

### 1. Install Dependencies

```bash
pip install langchain faiss-cpu telebot PyMuPDF langchain_community colab-xterm ollama
