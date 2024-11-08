# AI-Agent

# Groq Data Extraction Flask App

## Overview
A Flask-based web application that dynamically processes user queries with placeholders, replaces them with dataset entities, and retrieves data using the Groq API.

## Features
- **Dynamic Placeholder Replacement**
- **Groq API Integration**
- **User-Friendly Interface**
- **Secure API Key Management**
- **Robust Error Handling**

## Prerequisites
- Python 3.7+
- pip

## Installation

1. **Clone the Repository**
    ```bash
    git clone https://github.com/yourusername/groq-data-extraction-flask.git
    cd groq-data-extraction-flask
    ```

2. **Create & Activate Virtual Environment**
    ```bash
    python3 -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    ```

3. **Install Dependencies**
    ```bash
    pip install -r requirements.txt
    ```

## Configuration

1. **Set Environment Variables**
    ```bash
    export GROQ_API_KEY='your_groq_api_key'  # Unix/Mac
    set GROQ_API_KEY=your_groq_api_key       # Windows
    ```

2. **Prepare Dataset**
    - Ensure your dataset is loaded into the `df` DataFrame in `app.py`.

## Usage

1. **Run the Application**
    ```bash
    python app.py
    ```

2. **Access via Browser**
    - Navigate to `http://127.0.0.1:5000/` and submit your query with placeholders like `{Company}`.

### Example Query

- **{Company}**: Will be replaced with entries like "OpenAI", "Google", or "Microsoft".
- **{Tourism}**: Will be replaced with entries like "Eiffel Tower", "Great Wall", or "Statue of Liberty".
- **{Vitamins}**: Will be replaced with entries like "Vitamin C", "Vitamin D", or "Vitamin B12".


### How It Works

When you submit the above query through the application:

1. **Placeholder Detection**: The app identifies all placeholders within curly braces `{}`.
2. **Entity Replacement**: Each placeholder is replaced with corresponding unique values from the dataset.
3. **API Processing**: The customized queries are sent to the Groq API to retrieve relevant data.
4. **Results Display**: Extracted information for each entity-placeholder combination is displayed on the results page.

### Sample Output

For example, one of the processed queries might be:

The application will generate and display the extracted data based on this customized query.
