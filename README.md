# Langgraph_Tutorial

Welcome to Langgraph_Tutorial!  
This repository is a practical guide for anyone new to the LangChain ecosystem, with a focus on LangGraph. As an example you will learn how to build a LinkedIn post generator agent that uses multi-threaded memory and web search.

## Repository

GitHub: [Langgraph_Tutorial](https://github.com/Abdulkadirklc/Langgraph_Tutorial)

## Features

- LangGraph agent workflow and memory management
- Google Gemini LLM integration (`langchain-google-genai`)
- DuckDuckGo web search (`ddgs`)
- Multi-threaded agent tasks with isolated memory
- Interactive approval for generated LinkedIn posts

## Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/Abdulkadirklc/Langgraph_Tutorial.git
cd Langgraph_Tutorial
```

### 2. Create and Activate Python Environment

Recommended (Conda):

```bash
conda create -n langgraph python=3.10 -y
conda activate langgraph
```

Or use venv:

```bash
python -m venv venv
venv\Scripts\activate  # Windows
source venv/bin/activate  # Mac/Linux
```

### 3. Install Dependencies

Run this in your terminal or as the first cell in the notebook:

```bash
pip install langgraph langchain-google-genai langchain-community ddgs langchain-core ipykernel
```

### 4. Add Kernel to Jupyter (if needed)

```bash
python -m ipykernel install --user --name langgraph --display-name "langgraph"
```

Select the "langgraph" kernel in Jupyter.

### 5. Set Up Google Gemini API Key

You need a Google Gemini API key.

**Option 1: Set as environment variable**

- Windows (PowerShell):
	```powershell
	$env:GOOGLE_API_KEY="your-gemini-api-key"
	```
- Mac/Linux:
	```bash
	export GOOGLE_API_KEY="your-gemini-api-key"
	```

**Option 2: Enter in Notebook**

If not set, the notebook will prompt you to enter your API key interactively.

## How to Run

1. Open `linkedin_content_generator.ipynb` in Jupyter.
2. Run all cells in order.
3. The notebook will:
		- Import libraries and set up the agent
		- Ask for your Google Gemini API key (if not set)
		- Build the agent workflow graph
		- Start two separate threads (tasks) for LinkedIn post generation
		- Pause for your approval before publishing each post

4. When prompted, type `yes` or `no` to approve or reject each generated post.


## Example Output

The notebook will display the agent graph and show interactive logs for each step, including web search, draft writing, editing, and publishing.
