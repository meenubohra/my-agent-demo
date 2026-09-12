# Project Documentation

## Overview

**my-agent-demo** is a demonstration repository that showcases how an AI‑powered documentation agent can interact with a codebase using OpenAI tools. The project includes utilities for reading, searching, and updating files in a GitHub repository, illustrating best practices for automated documentation generation and maintenance.

## Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/my-agent-demo.git
   cd my-agent-demo
   ```
2. **Set up a Python virtual environment** (optional but recommended)
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows use `venv\Scripts\activate`
   ```
3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```
   > *If a `requirements.txt` file is not present, install the OpenAI SDK and any other required packages manually:* 
   ```bash
   pip install openai
   ```
4. **Configure your OpenAI API key**
   ```bash
   export OPENAI_API_KEY="your-openai-api-key"
   ```
   *(On Windows use `set` instead of `export`.)*

## Usage Examples

### Running the Documentation Agent
```bash
python agent.py  # Replace with the actual entry‑point script name
```
The agent will:
- Read existing files (e.g., `README.md`).
- Generate or update documentation files such as `DOCS.md`.
- Provide suggestions for improving project docs.

### Updating a File via the Agent
```python
from agents import DocumentationAgent
agent = DocumentationAgent()
agent.update_file('README.md', old_content, new_content)
```

### Searching the Codebase
```bash
# Search for a function name or keyword
search "DocumentationAgent"
```
The agent will return matching code snippets and file locations.

## Contribution Guidelines

1. **Fork the repository** and create a new branch for your feature or bug fix.
2. **Write clear commit messages** following the conventional commit style.
3. **Ensure documentation is up‑to‑date** – add or modify sections in `DOCS.md` as needed.
4. **Run any existing tests** (if applicable) and add new tests for new functionality.
5. **Submit a Pull Request** with a description of the changes and reference any related issues.

### Code Style
- Use **PEP 8** for Python code.
- Keep line lengths to **79 characters** where possible.
- Include docstrings for all public functions and classes.

## License

This project is licensed under the **MIT License**. See the `LICENSE` file for the full text.
