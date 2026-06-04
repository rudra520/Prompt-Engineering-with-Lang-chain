
# Prompt Engineering with LangChain 🚀

Welcome to the **Prompt Engineering with LangChain** repository! This project focuses on the programmatic management, optimization, and scaling of Large Language Model (LLM) inputs using dynamic templates. 

Inspired by advanced prompt engineering methodologies (including concepts from Simplilearn), this repository serves as a practical guide and codebase for moving beyond static text prompts into structured, reusable, and dynamic prompt architectures.

---

## 📌 Project Overview

Static prompts often fail when building production-grade AI applications. This repository demonstrates how to leverage **LangChain** to treat prompts as code—allowing you to dynamically inject variables, manage few-shot examples, and format outputs reliably.

### Key Focus Areas:
* **Dynamic Templating:** Separating prompt logic from application logic using LangChain's native template structures.
* **Programmatic Input Management:** Automating how data, context, and user inputs are synthesized before being sent to an LLM.
* **Advanced Prompt Techniques:** Implementing Zero-shot, Few-shot, and Chain-of-Thought prompting programmatically.

---

## 🛠️ Core Concepts Covered

### 1. Prompt Templates
The bread and butter of LangChain prompt engineering. We explore how to construct string templates with placeholders that can be filled dynamically at runtime.

```python
from langchain_core.prompts import PromptTemplate

template = "You are a helpful assistant. Explain the concept of {topic} in one sentence."
prompt = PromptTemplate.from_template(template)

# Dynamic formatting
final_prompt = prompt.format(topic="Retrieval-Augmented Generation")

```
### 2. Chat Prompt Templates
Working with Chat Models requires structured roles (system, human, ai). This section covers how to build dynamic conversational prompts.
```python
from langchain_core.prompts import ChatPromptTemplate

chat_template = ChatPromptTemplate.from_messages([
    ("system", "You are a sarcastic comedian writing a joke about {subject}."),
    ("human", "Tell me a joke about {topic}."),
])

```
### 3. Few-Shot Prompt Templates
Programmatically injecting examples into your prompts to guide the LLM's behavior and output format without fine-tuning.
## 🚀 Getting Started
### Prerequisites
Make sure you have Python 3.8+ installed. You will also need an API key from an LLM provider (e.g., OpenAI, Anthropic, or HuggingFace).
### Installation
 1. **Clone the repository:**
   ```bash
   git clone [https://github.com/YOUR_USERNAME/Prompt-Engineering-with-Lang-chain.git](https://github.com/YOUR_USERNAME/Prompt-Engineering-with-Lang-chain.git)
   cd Prompt-Engineering-with-Lang-chain
   
   ```
 2. **Set up a virtual environment:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use: venv\Scripts\activate
   
   ```
 3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   
   ```
 4. **Environment Setup:**
   Create a .env file in the root directory and add your API keys:
   ```env
   OPENAI_API_KEY=your_openai_api_key_here
   
   ```
## 📂 Repository Structure
```text
├── data/                  # Few-shot examples and datasets
├── notebooks/             # Jupyter notebooks for interactive learning (Simplilearn notes)
│   ├── 01_basic_templates.ipynb
│   └── 02_advanced_few_shot.ipynb
├── src/                   # Production-ready Python scripts
│   ├── __init__.py
│   └── prompt_manager.py  # Custom modules for dynamic prompt building
├── .env.example           # Example environment file
├── requirements.txt       # Project dependencies
└── README.md              # Project documentation

```
## 📈 Learning Roadmap & References
This repository is continuously updated as I progress through advanced prompt engineering concepts.
 * **Simplilearn:** Advanced Prompt Engineering Course framework.
 * **LangChain Documentation:** Prompt Templates Guide
## 🤝 Contributing
Contributions, issues, and feature requests are welcome! Feel free to check the issues page if you want to contribute to the learning roadmap.
## 📄 License
This project is licensed under the GPL License.
```
