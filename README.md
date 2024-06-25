# code-project-unlimited

Hi there 👋

This first of many codes defines this Python application that uses BERT embeddings to validate the relevance of user responses to agent questions in conversations stored in an Excel file. Here’s a breakdown of how it works:

Main Components: ConversationRelevanceValidator Class:

Initialization: Sets up BERT tokenizer and model, defines data structures for storing results. load_data: Loads an Excel file and identifies columns containing agent questions and user responses. get_bert_embedding: Uses BERT to generate embeddings for text. compute_similarity: Computes cosine similarity between BERT embeddings of agent question and user response. validate_relevance: Concurrently computes similarity for each pair of agent question and user response in the loaded dataset. save_to_excel: Saves validation results (agent question, user response, similarity score, relevance) to an Excel file. GUI Class:

Initialization: Sets up a tkinter GUI with buttons and text widgets. create_widgets: Defines UI elements for file selection, threshold adjustment, result display, and buttons for validation and saving. load_file: Allows the user to select an Excel file for validation. update_threshold: Updates the relevance threshold based on user input. run_validation: Triggers validation of loaded data using ConversationRelevanceValidator. save_to_excel_handler: Allows the user to save validation results to an Excel file. How to Use: Select Excel File: Load your dataset where agent questions and user responses are stored. Adjust Threshold: Set the similarity threshold (between 0 and 1) to determine relevance. Validate Relevance: Compute similarity scores and determine relevance for each agent question and user response pair. Save to Excel: Export the validated results (including similarity scores and relevance) to an Excel file. Libraries Used: tkinter: For building the GUI. pandas: For data manipulation (loading Excel files). transformers (Hugging Face): For BERT model and tokenizer. scikit-learn: For cosine similarity calculation. numpy: For numerical operations. concurrent.futures: For parallel processing of similarity calculations. Considerations: Ensure your system has the necessary libraries installed (transformers, torch, scikit-learn, numpy) to run the application. The application assumes columns in the Excel file are appropriately labeled for agent questions and user responses. Error handling is implemented to manage potential issues with data loading, embedding computation, and file operations. This setup allows efficient validation of conversation relevance using advanced NLP techniques provided by BERT embeddings and cosine similarity. Adjustments and extensions can be made based on specific application needs.

--> https://github.com/Roy-Enriquez/code-project-unlimited.git # download / clone from git repository

Create a new virtual environment
python -m venv myenv

Activate the virtual environment
On Windows:
myenv\Scripts\activate

On macOS/Linux:
source myenv/bin/activate

pip install -r requirements.txt # Install dependencies

python relevantornot.py # Run the python script
