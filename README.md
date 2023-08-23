# OpenAI CHATGPT Chain of Reasoning

## Introduction
This repository contains a Jupyter notebook focused on the concept of a "chain of reasoning" with OpenAI's CHATGPT API. The notebook demonstrates how to provide structured instructions to the model, guiding it through a multi-step reasoning process to handle customer queries about specific products.

## Requirements
### Prerequisites
1. **Python Environment**: The code is written in Python and requires a Python 3.x environment.
2. **Python Libraries**: Ensure you have the following libraries installed in your system:
   - `os`
   - `openai`
   - `dotenv`
3. **OpenAI API Key**: You'll need an API key from OpenAI to interact with the service. Store it securely in an `.env` file or another secure location and make sure it's accessible to the notebook

## Code Explanation
### Setup and Initialization
- **Library Imports**: The necessary Python libraries for the code's operation are imported.
- **Environment Variable Loading:** The OpenAI API key is loaded from the local `.env` file using `dotenv`.

### Function Definitions
1. `get_completion_from_messages(messages, model="gpt-3.5-turbo", temperature=0, max_tokens=500)`: This function is designed to send a series of messages to the OpenAI model and receive a structured response. It takes into account:
    - `messages`:  A list of message objects containing a role (either "system" or "user") and content (the actual message).
    - `model`:  The OpenAI model to use (default is "gpt-3.5-turbo").
    - `temperature`: Adjusts the randomness of the model's output.
    - `max_tokens`: Limits the length of the model's response.

### Chain of Reasoning Implementation
- **System Message:** A detailed instruction set for the model is provided. This "system message" guides the model through five steps of reasoning, from identifying if a user's query is about a specific product to providing a user-friendly response.
- **User Queries:** Two example user queries are demonstrated:
    1. Comparing the prices of two products.
    2. Asking if TVs are sold.
For each query, the model's response showcases its step-by-step reasoning process, culminating in a direct answer to the user.

 ### Error Handling
A simple error-handling mechanism ensures that if there's an issue parsing the model's response, a friendly error message is displayed.

## Usage Tips
- The `system_message` is the core of the chain of reasoning. Adjusting it can guide the model's behavior differently.
- The `delimiter` is essential for separating each step in the model's reasoning. Ensure that user queries and system messages respect the delimiter structure.
- This approach can be expanded to handle a wider range of products or other multi-step reasoning tasks.
