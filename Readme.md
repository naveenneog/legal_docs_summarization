# Legal Documents Summarization using LangChain  
   
## Brief Description  
   
This project demonstrates how to summarize legal documents using [LangChain](https://github.com/hwchase17/langchain) with two different techniques: Map-Reduce and Retrieval Augmented Generation (RAG). It includes Jupyter notebooks that guide you through the process of leveraging Azure OpenAI services and Azure Document Intelligence to generate concise summaries of lengthy legal texts.  
   
---  
   
## Features  
   
- **Summarize Legal Documents**: Automatically generate summaries of legal documents using advanced language models.  
- **Two Summarization Techniques**:  
  - **Map-Reduce Chain**: Breaks down the document into smaller chunks, summarizes each, and then combines them.  
  - **Retrieval Augmented Generation (RAG)**: Enhances summarization by retrieving relevant information from the document during the generation process.  
- **Interactive Jupyter Notebooks**: Step-by-step instructions with code examples.  
- **Azure Integration**: Utilizes Azure OpenAI services and Azure Document Intelligence for processing and analyzing documents.  
- **Sample Documents Provided**: Includes a set of legal documents for testing and experimentation.  
   
---  
   
## Installation Instructions  
   
### Prerequisites  
   
- **Python**: Version 3.8 or higher.  
- **Azure Accounts**:  
  - **Azure OpenAI Service**: Access to Azure OpenAI with an API key.  
  - **Azure Document Intelligence**: Formerly known as Azure Form Recognizer, with an API key.  
- **Git**: For cloning the repository.  
- **Jupyter Notebook**: For running the `.ipynb` files.  
   
### Steps  
   
1. **Clone the Repository**:  
  
   ```bash  
   git clone https://github.com/yourusername/legal_docs_summarization.git  
   cd legal_docs_summarization  
   ```  
   
2. **Create a Virtual Environment (Recommended)**:  
  
   ```bash  
   python -m venv venv  
   ```  
   
3. **Activate the Virtual Environment**:  
  
   - **Windows**:  
  
     ```bash  
     venv\Scripts\activate  
     ```  
  
   - **macOS/Linux**:  
  
     ```bash  
     source venv/bin/activate  
     ```  
   
4. **Install Required Dependencies**:  
  
   ```bash  
   pip install -r requirements.txt  
   ```  
   
5. **Set Up Azure Environment Variables**:  
  
   - Rename `azure.env.example` to `azure.env` if not already present.  
   - Open `azure.env` and replace the placeholder values with your actual Azure API keys and endpoints:  
  
     ```env  
     AZURE_OPENAI_API_KEY=your_azure_openai_api_key  
     AZURE_OPENAI_ENDPOINT=your_azure_openai_endpoint  
     AZURE_DOCUMENT_INTELLIGENCE_KEY=your_document_intelligence_key  
     AZURE_DOCUMENT_INTELLIGENCE_ENDPOINT=your_document_intelligence_endpoint  
     ```  
   
6. **Install Jupyter Notebook** (if not already installed):  
  
   ```bash  
   pip install jupyter  
   ```  
   
7. **Launch Jupyter Notebook**:  
  
   ```bash  
   jupyter notebook  
   ```  
   
8. **Run the Notebooks**:  
  
   - Open `summarize_map_reduce.ipynb` or `summarize_rag.ipynb`.  
   - Follow the instructions within each notebook.  
   
---  
   
## Usage Examples  
   
### Summarization with Map-Reduce Chain  
   
1. **Open the Notebook**:  
  
   Open `summarize_map_reduce.ipynb` in Jupyter Notebook.  
   
2. **Modify the Document Path**:  
  
   In the notebook, locate the cell where the document is loaded:  
  
   ```python  
   file1 = r'path_to_your_legal_document.pdf'  
   ```  
  
   Replace `'path_to_your_legal_document.pdf'` with the path to your own document.  
   
3. **Run the Cells**:  
  
   Execute each cell in order. The notebook will:  
  
   - Load and process your document using Azure Document Intelligence.  
   - Split the text into manageable chunks.  
   - Use LangChain's Map-Reduce chain to generate summaries.  
   - Produce a final summarized output.  
   
4. **View the Summary**:  
  
   At the end of the notebook, you'll see the generated summary of your legal document.  
   
### Summarization with Retrieval Augmented Generation (RAG)  
   
1. **Open the Notebook**:  
  
   Open `summarize_rag.ipynb` in Jupyter Notebook.  
   
2. **Modify the Document Path**:  
  
   Update the file path in the following cell:  
  
   ```python  
   loader = AzureAIDocumentIntelligenceLoader(file_path='path_to_your_legal_document.pdf', ...)  
   ```  
   
3. **Run the Cells**:  
  
   Execute each cell sequentially. This notebook will:  
  
   - Process your document and create embeddings.  
   - Store embeddings in a vector store for retrieval.  
   - Use the RAG approach to generate a summary by retrieving relevant chunks during generation.  
   
4. **View the Summary**:  
  
   The final output will display a context-aware summary of your legal document.  
   
---  
   
## Configuration Options  
   
- **API Keys and Endpoints**:  
  
  Ensure all Azure service keys and endpoints are correctly set in the `azure.env` file.  
   
- **Document Paths**:  
  
  Replace file paths in the notebooks with the path to your own documents. Ensure the documents are accessible and in a supported format (e.g., PDF).  
   
- **Text Splitting Parameters**:  
  
  Adjust the text splitting logic or parameters if your documents have specific formatting or structure.  
   
- **Model Selection**:  
  
  Modify the model parameters in the LangChain configurations if you have access to different models or require specific model capabilities.  
   
---  
   
## Contribution Guidelines  
   
We welcome contributions to enhance this project!  
   
- **Reporting Issues**:  
  
  Use the [Issues](https://github.com/yourusername/legal_docs_summarization/issues) tab to report bugs or suggest enhancements.  
   
- **Submitting Pull Requests**:  
  
  1. Fork the repository.  
  2. Create a new branch for your feature or bug fix:  
  
     ```bash  
     git checkout -b feature/your_feature_name  
     ```  
  
  3. Commit your changes with clear messages:  
  
     ```bash  
     git commit -m "Description of your changes"  
     ```  
  
  4. Push to your forked repository:  
  
     ```bash  
     git push origin feature/your_feature_name  
     ```  
  
  5. Open a pull request against the main branch with a detailed description of your changes.  
   
- **Coding Standards**:  
  
  - Follow PEP 8 styling guidelines.  
  - Write clear, concise code with comments where necessary.  
   
- **Testing**:  
  
  Ensure that all existing functionality remains intact and that your additions are tested.  
   
---  
   
## Testing Instructions  
   
- **Using Sample Documents**:  
  
  - The `Sample_docs` directory contains legal documents you can use to test the notebooks.  
  - Make sure the file paths in the notebooks point to these sample documents.  
   
- **With Your Own Documents**:  
  
  - Replace the file paths in the notebooks with the paths to your own legal documents.  
  - Ensure your documents are in a supported format and accessible from the notebook.  
   
- **Verifying Outputs**:  
  
  - Run all cells in the notebooks without encountering errors.  
  - Check that the summaries are generated and make sense in the context of the input documents.  
   
---  
   
## License  
   
This project is licensed under the [MIT License](LICENSE). You are free to use, modify, and distribute this software in accordance with the terms of the license.  
   
---  
   
## Acknowledgements/Credits  
   
- **[LangChain](https://github.com/hwchase17/langchain)**: For providing a powerful framework to build applications with LLMs.  
- **[OpenAI](https://openai.com/)**: For the GPT language models used in text summarization.  
- **[Azure OpenAI Services](https://azure.microsoft.com/en-us/services/cognitive-services/openai-service/)**: For hosting the language models.  
- **[Azure Document Intelligence](https://azure.microsoft.com/en-us/services/form-recognizer/)**: For document processing and OCR capabilities.  
- **Contributors**: Thanks to all contributors who have helped in improving this project.  
   
---  
   
*Feel free to raise any questions or issues. Happy summarizing!*