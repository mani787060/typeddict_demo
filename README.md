# Python TypedDict Demo

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![Topic](https://img.shields.io/badge/Topic-Type%20Hints-orange)
![Generative AI](https://img.shields.io/badge/Generative%20AI-Structured%20Output-purple)

## Overview

This project demonstrates how to use Python's `TypedDict` to describe the expected structure of dictionary objects.

In Generative AI applications, language models often return information that needs to be organized into predictable fields. `TypedDict` helps developers document the expected keys and value types, making code easier to understand and maintain.

The current implementation uses a simple `Person` example with two fields: `name` and `age`.

## Objectives

- Understand Python's `TypedDict`.
- Define the expected keys and value types of a dictionary.
- Learn how type hints improve code readability.
- Explore the foundation of structured data representation in Python.
- Understand how typed dictionary schemas can be applied in LLM-based applications.

## Implementation

The project defines a `Person` type using `TypedDict`:

```python
from typing import TypedDict

class Person(TypedDict):
    name: str
    age: int

new_person: Person = {
    "name": "nitish",
    "age": "35"
}

print(new_person)
```

### How It Works

1. **Import `TypedDict`:** Makes the feature available from Python's `typing` module.
2. **Define the schema:** The `Person` class specifies that `name` should be a string and `age` should be an integer.
3. **Create a dictionary:** `new_person` stores the values using the expected keys.
4. **Print the result:** The dictionary is displayed in the terminal.

**Important:** In the current example, `"35"` is a string, not an integer. Python's `TypedDict` does not automatically validate or convert values at runtime. To match the declared type, use `35` without quotation marks.

## Expected Output

```text
{'name': 'nitish', 'age': '35'}
```

The output reflects the values exactly as they are stored in the dictionary.

## What Is TypedDict?

`TypedDict` is a Python typing feature that describes the expected structure of a dictionary.

For example:

- `name: str` indicates that the name should be a string.
- `age: int` indicates that the age should be an integer.

It helps static type checkers and compatible development tools identify potential type mismatches. However, it does not enforce those types automatically when the program runs.

## TypedDict and Pydantic

Both `TypedDict` and Pydantic can describe structured data, but they serve different purposes.

| Feature | TypedDict | Pydantic |
|---|---|---|
| Main purpose | Describe dictionary structure | Validate and parse data |
| Runtime validation | Not automatic | Supported |
| Type checking | Supports static type checking | Supports typed models and runtime validation |
| Automatic type conversion | No | Possible for supported fields and configurations |
| Typical use | Lightweight type hints | Data validation and structured application inputs |

In LLM applications, LangChain can use a `TypedDict` schema with supported models to guide structured output generation. This repository's current `app.py`, however, demonstrates only a plain Python dictionary and does not call an LLM.

## Technologies Used

- Python
- `typing.TypedDict`
- Python dictionaries

## Installation and Usage

### 1. Clone the repository

```bash
git clone https://github.com/mani787060/typeddict_demo.git
cd typeddict_demo
```

### 2. Run the script

If your Python file is named `app.py`, run:

```bash
python app.py
```

No external packages are required for the current example.

## Applications

`TypedDict` can be useful for describing data structures used in:

- API request and response objects
- Configuration dictionaries
- Data processing pipelines
- LLM input and output schemas
- Applications that benefit from static type checking

## Future Improvements

- Correct the age value to an integer.
- Add examples with optional and required dictionary fields.
- Demonstrate static type checking with tools such as mypy or Pyright.
- Integrate a `TypedDict` schema with LangChain's `with_structured_output()` method.
- Compare LLM structured output using `TypedDict` and Pydantic.

## Conclusion

This project introduces Python's `TypedDict` through a simple example. It demonstrates how developers can describe the expected structure of dictionaries and build a foundation for working with structured data in Python and Generative AI applications.

**Repository:** [typeddict_demo](https://github.com/mani787060/typeddict_demo)
