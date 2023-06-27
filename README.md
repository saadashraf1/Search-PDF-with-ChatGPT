# GPT-powered Document Question Answering App

This is a Python code file for a GPT-powered document question answering application. The application utilizes the Langchain library and OpenAI's GPT language model to enable users to input prompts and receive relevant answers from a document.

## Dependencies

To run the code, you need to install the following dependencies:
- `os`: This module provides a way to access operating system functionalities.
- `langchain`: A library providing utility functions for working with language generation models.
- `streamlit`: A framework for building interactive web applications.
- `PyPDF2`: A library for working with PDF files.

You can install the required dependencies using `pip`:
```bash
pip install langchain streamlit PyPDF2
```

## Setup

1. Set your OpenAI API key:  
   In the code, replace `'enter your api key here'` with your actual OpenAI API key.

2. Load the PDF document:
   - Replace `'sample_pdf_file.pdf'` with the path to your desired PDF document.
   - Ensure that the document is correctly formatted and accessible.

## Running the Application

To run the GPT-powered Document Question Answering App, execute the following command:
```bash
streamlit run app.py
```

Once the application is running, a web interface will be displayed with a text input box labeled "Input your prompt here". Enter your prompt in this field.

The application utilizes Langchain and OpenAI's GPT language model to generate relevant answers from the provided document. It splits the document into pages using the PyPDFLoader and creates a Chroma vector store. The application then uses the vector store to perform document similarity search and generate responses based on the user's prompt.

The generated answers will be displayed on the screen. You can also expand the "Document Similarity Search" section to view the content of the most relevant page from the document.

## Customization

Feel free to modify the code to suit your needs:
- Adjust the temperature value (`temperature=0.1`) to control the creativity of the generated responses.
- Customize the UI using Streamlit's features to enhance the user experience.
- Replace the PDF document (`'sample_pdf_file.pdf'`) with your own document or utilize other document loaders available in Langchain.
