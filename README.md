# LLM Chat Assistant with Dynamic Context Based on Query

This project implements a basic chatbot using OpenAI's Language Model (LLM). The chatbot dynamically retrieves context from external sources, such as APIs and documents, to answer user queries effectively.

## Requirements

- Python 3.x
- `openai` library
- `requests` library

## Installation
- Install dependencies
- Replace `api_key` in the code with your actual OpenAI API key.

### Step 1: Initialize OpenAI Client

Initialize the OpenAI client with your API key.

### Step 2: Define External Data Retrieval Function

Define functions to retrieve external data, such as `get_hotel_details`, which retrieves hotel details based on rating.
#### Note: Rating just used as filter.

### Step 3: Define Available Functions and Descriptions

Define available functions and their descriptions, specifying parameters required for each function.

### Step 4: Define Function to Get GPT Response

Define a function to get a response from the GPT-3.5 model, incorporating available functions and messages.

### Step 5: Define Function to Execute Function Calls

Define a function to execute function calls extracted from the GPT-3.5 response, calling the appropriate function with provided arguments.

### Steps 6-9: Execute Chatbot Interaction

Execute the chatbot interaction loop:
- **Step 6**: Generate a response from the GPT-3.5 model based on the user query.
- **Step 7**: Execute the function call extracted from the GPT-3.5 response.
- **Step 8**: Append messages and function responses to maintain conversation history.
- **Step 9**: Obtain the final response incorporating the function execution.
