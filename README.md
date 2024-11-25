# Local LLM

This repository showcases a simple demo application for interacting with a **Llama2** model locally using **LangChain** and **Streamlit**. The project leverages the **Ollama** library for running the Llama2 model and demonstrates how to track LangChain activities via LangSmith.

---

## Features
- **Local LLM Integration:** Utilize the **Llama2** model for generating responses.
- **Streamlit Interface:** An intuitive web UI for user interaction.
- **LangChain Integration:** Create structured prompts and output parsers using LangChain's framework.
- **LangSmith Tracking:** Monitor and log activity seamlessly with LangSmith's API.

---

## Prerequisites

1. **Python 3.8+** installed.
2. **Llama2 Model** configured locally via **Ollama**.
3. **Environment Variables:** Ensure you have a `.env` file with the following keys:
   - `LANGCHAIN_API_KEY`: Your LangChain API key.
   - Optionally, specify `LANGCHAIN_PROJECT` for custom project tracking.

---

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name
   ```

2. Create a virtual environment:
   ```bash
   python -m venv env
   source env/bin/activate  # On Windows: env\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Set up environment variables:
   Create a `.env` file in the project root and add your LangChain API key:
   ```
   LANGCHAIN_API_KEY=your-api-key
   ```

---

## Usage

1. Start the Streamlit application:
   ```bash
   streamlit run app.py
   ```

2. Open the app in your browser (usually at `http://localhost:8501`).

3. Input your question in the text box, and the Llama2 model will generate a response.

---

## How It Works

1. **Prompt Template:** The system uses a structured LangChain prompt template:
   - The system message provides instructions to the assistant.
   - The user input (`{question}`) is dynamically inserted into the template.

2. **LLM Integration:** The **Ollama** library powers the interaction with the local Llama2 model.

3. **Output Parsing:** The `StrOutputParser` ensures the output is in plain text format for display.

4. **LangSmith Tracking:** Activity and prompt details are logged automatically for monitoring and debugging.

---

## Example

**Input:**  
> "What is the capital of France?"

**Output:**  
> "The capital of France is Paris."

---

## Project Structure

```plaintext
.
├── app.py               # Main application script
├── requirements.txt     # Dependencies
├── .env                 # Environment variables
└── README.md            # Project documentation
```

---

## Dependencies

- [LangChain](https://github.com/hwchase17/langchain)
- [Streamlit](https://streamlit.io)
- [Ollama](https://ollama.ai)
- [Python-dotenv](https://pypi.org/project/python-dotenv/)

---

## Acknowledgments

- **LangChain Community:** For their amazing tools and resources.
- **Ollama:** For enabling seamless local LLM integration.

---

Feel free to fork, star, and contribute to this project. Pull requests are welcome! 🚀
