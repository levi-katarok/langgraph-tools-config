# Minimal Reproduction of Passing Config To Tools In Langgraph

This project demonstrates a minimal reproduction of passing configuration to tools in Langgraph, a library for building language model applications.

## Overview

The project showcases a conversational AI system with multiple assistants, including a primary assistant and a booking assistant. It demonstrates how to:

1. Build a state graph using Langgraph
2. Pass configuration to tools
3. Handle different assistants and their specialized tools
4. Route conversations between assistants based on user input

## Prerequisites

- Python 3.11+
- pip

## Installation

1. Clone the repository
2. Create a virtual environment:
   ```
   python -m venv env
   source env/bin/activate  # On Windows, use `env\Scripts\activate`
   ```
3. Install the required packages:
   ```
   pip install -r requirements.txt
   ```

## Configuration

1. Create a `.env` file in the project root
2. Add your OpenAI API key:
   ```
   OPENAI_API_KEY=your_api_key_here
   ```

## Project Structure

The main components of the project are:

1. Primary Assistant
2. Booking Assistant
3. State Graph
4. Tools (e.g., `query_bookings`)

## Usage

The project is set up as a Jupyter notebook. To run it:

1. Start Jupyter Notebook:
   ```
   jupyter notebook
   ```
2. Open the `minimal-tool-config-case.ipynb` file
3. Run the cells

## Key Components

### Primary Assistant

The primary assistant is responsible for delegating tasks to specialized assistants.

### Booking Assistant

The booking assistant handles queries related to user bookings.

### State Graph

The state graph manages the flow of conversation between different assistants and tools.

### Query Bookings Tool

This tool demonstrates how to access configuration passed through the `RunnableConfig`.

## How It Works

1. The system initializes with a primary assistant.
2. Based on user input, it may delegate to specialized assistants (e.g., Booking Assistant).
3. Tools like `query_bookings` can access configuration passed through the `RunnableConfig`.
4. The state graph manages the flow between different assistants and tools.
