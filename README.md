# Structured LLM Outputs with TypedDict
[![Python](https://img.shields.io/badge/Python-3.9%2B-blue)](https://www.python.org/)
[![LangChain](https://img.shields.io/badge/Framework-LangChain-green)](https://www.langchain.com/)
[![Gemini](https://img.shields.io/badge/Model-Google%20Gemini-4285F4)](https://ai.google.dev/)

## 🏗️ Project Overview
This repository demonstrates how to extract **Structured Data** from LLMs using Python's native `TypedDict`. While Pydantic is excellent for complex validation, `TypedDict` offers a more lightweight approach for developers who prefer working with standard Python dictionaries while maintaining high levels of type-safety and IDE support.

---

## 🛠️ Key Technical Implementations

### 1. Native Schema Definition
* **Standard Python Types:** Using `TypedDict` to define the expected keys and value types (str, int, list, etc.) without external dependencies.
* **Optionality:** Leveraging `Required` and `NotRequired` (Python 3.11+) to tell the LLM which data points are mandatory.

### 2. Structured Extraction Pipeline
* **`with_structured_output` Integration:** Seamlessly binding the TypedDict class to the Gemini Pro model via LangChain.
* **Dictionary Transformation:** Automatically parsing the LLM's raw response into a dictionary that matches the defined schema.

### 3. Lightweight vs. Heavyweight Validation
* **Comparison:** Demonstrating the trade-offs between `TypedDict` (speed/simplicity) and `Pydantic` (strict validation/parsing).

---

## 💻 Tech Stack
* **Language:** Python 3.9+
* **Orchestration:** LangChain (`langchain-core`, `langchain-google-genai`)
* **Core Logic:** Python `typing.TypedDict`
* **Model:** Google Gemini Pro
* **Environment:** `python-dotenv`

