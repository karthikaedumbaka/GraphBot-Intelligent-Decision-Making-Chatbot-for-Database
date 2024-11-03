# VectorDB Management and Chatbot Interface
This project provides a comprehensive solution for managing a Vector Database (VectorDB) using document embeddings and interacting with a chatbot interface. It includes tools for preparing document embeddings, managing configurations, and a Gradio-based chatbot interface.

## Table of Contents
- Features
- Installation
- Configuration
- Usage
- Components
- Contributing


## Features

# Agent Decision-Making Graph:
- Utilizes a primary language model (LLM) integrated with various tools.
- Implements a state graph for decision-making, allowing conditional tool invocation and interaction flow between the chatbot and tools.
# Tool Configuration Management:
- Loads and manages configurations from a config file.
- Sets environment variables and configures tools such as SQL agents and search functionalities.
# VectorDB Preparation:
- Prepares a VectorDB by processing documents, splitting them into chunks, and embedding them using specified models.
- Supports configurations for different document types, such as Swiss Airline Policy and Stories.
# Chatbot Interface:
- Provides a Gradio-based interface for user interaction.
- Allows users to input text or upload documents for processing and response generation.
# Memory and Checkpoint Management:
- Utilizes a memory-saving mechanism to track and save checkpoints in the decision-making graph.
- Ensures efficient state management and tool invocation tracking.

# 1. Installation
```sh
git clone https://github.com/yourusername/yourproject.git
cd yourproject
```

# 2. Install dependencies: Ensure you have Python 3.7 or later. Install the required packages using pip:

```sh
pip install -r requirements.txt
```

# 3. Environment Variables: Create a .env file in the root directory and add your API keys:

```sh
OPENAI_API_KEY=your_openai_api_key
TAVILY_API_KEY=your_tavily_api_key
```

# Configuration
The project uses a YAML configuration file located at configs/tools_config.yml. This file contains settings for various components such as the Swiss Airline Policy RAG and Stories RAG. Ensure the paths and parameters are correctly set according to your environment.
# Usage
## Preparing the Vector Database
To prepare the VectorDB, run the _prepare_vector_db.py_ script:

```sh
python src/prepare_vector_db.py
```

This script will load documents, split them into chunks, embed them using the specified model, and store the embeddings in a persistent VectorDB directory.


# Running the Chatbot
To interact with the chatbot, run the _app.py_ script:

```sh
python src/app.py
```

This will start a Gradio interface where you can enter text or upload PDF files for processing.


# Contributing
Contributions are welcome! Please fork the repository and submit a pull request for any improvements or bug fixes.
