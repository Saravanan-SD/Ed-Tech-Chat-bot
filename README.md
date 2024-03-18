# Codebasics Q&A README

This repository contains code for setting up a question and answer system based on the Codebasics FAQ dataset. The system utilizes language models and vector stores for efficient retrieval of answers from the given dataset.

![Working](https://github.com/Saravanan-SD/Ed-Tech-Chat-bot/blob/main/Screenshot%202024-03-18%20183650.png)

## Installation
1. Clone this repository to your local machine.
2. Navigate to the project directory.
3. Install dependencies using `pip install -r requirements.txt`.
4. Set up your environment variables:
    - Create a `.env` file in the project directory.
    - Define `GOOGLE_API_KEY` in the `.env` file with your Google API key.
5. Ensure you have the necessary dataset. In this case, the dataset used is `codebasics_faqs.csv`.

## Usage
### 1. Creating the Vector Database
- Run the `create_vector_db()` function to generate a vector database from the FAQ dataset. This function reads data from `codebasics_faqs.csv`, creates embeddings using a Hugging Face model, and saves the vector database locally using FAISS.

### 2. Running the Streamlit App
- Run the Streamlit app using `streamlit run app.py`.
- Click on the "Create Knowledgebase" button to generate the vector database (if not already created).
- Input your question in the text field provided.
- The system will retrieve an answer based on the input question and display it on the interface.

## Components
### 1. Vector Database Creation
- The `create_vector_db()` function initializes the dataset loader, generates embeddings using a Hugging Face model, and saves the vector database locally.

### 2. Question and Answer Chain
- The `get_qa_chain()` function sets up a question and answer retrieval system using a combination of language models and vector stores. It initializes a Google Palm language model, sets up a prompt template for querying, and creates a retriever for querying the vector database.

### 3. Streamlit Interface
- The Streamlit app (`app.py`) provides a user-friendly interface for interacting with the question and answer system. It allows users to input their questions and retrieves answers using the configured chain.

## Additional Notes
- Ensure your environment variables are correctly set, especially the `GOOGLE_API_KEY`.
- Feel free to modify the prompt template or adjust parameters according to your requirements.
- For more detailed documentation on each component, refer to the inline comments in the code.

## Contact
Feel free to reach out with any questions, issues, or contributions! Happy coding! 🚀

- Email: [saravanansd634@gmail.com](mailto:saravanansd634@gmail.com)
- LinkedIn: [Saravanan S](https://www.linkedin.com/in/sdsaravanan/)
---



