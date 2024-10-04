# Legal documents Summarization using Langchain Map Reduce and RAG for summarization

This repo is built as a demo for the legal agreements summarization using Mapreduce 
Please insert your file and try the lab

## Prerequisites
Before running the notebook, make sure you have the following installed:

1. Python: Install the latest version of Python from the official website.
2. Replace the keys in the `azure.env` with your subscription keys. 

To replace the multi_page_table.pdf with your document, follow these steps:

1. Open the existing document.
2. Locate the multi_page_table section.
3. Replace the content of the multi_page_table.pdf path with the path of the existing document and change the name references
4. Save the changes.


## Steps
1. Clone the repository: 
    ```
    git clone <repository_url>
    ```

2. Navigate to the project directory:
    ```
    cd <project_directory>
    ```

3. Create a virtual environment (optional but recommended):
    ```
    python -m venv venv
    ```

4. Activate the virtual environment:
    ```
    .\venv\Scripts\activate
    ```

5. Install the required dependencies:
    ```
    pip install -r requirements.txt
    ```
6. Install Jupyter Notebook:
        ```
        pip install jupyter
        ```

7. Launch Jupyter Notebook:
    ```
    jupyter notebook
    ```

8. In your web browser, navigate to the notebook file (`summarize_rag.ipynb`) and open it.

9. Run the notebook cells one by one to execute the demo , replace the document location 

10. For Summarization by RAG use `summarize_rag.ipynb` . for Summarization by Map Reduce and Refine use `summarize_map_reduce.ipynb`.

That's it! You have successfully run the demo Python notebook in Windows PowerShell.
