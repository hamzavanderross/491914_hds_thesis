## Epidemiological parameter extraction demonstration

# Overview
This directory aims to demonstrate an approach for extracting epidemiological parameters from full text medical articles using pre-trained LLMs and prompting.

# Directory Structure
### Folders

    data/: Contains all the data used and generated by the project.
        pdf_files/: Stores the original PDF downloaded from PubMed. Every article is openly available.
        text_files/: Contains the converted text files extracted from the PDFs.
        ground_truth/: Holds the ground truth data for parameter evaluation, serving as a reference for the accuracy of parameter extraction. T
        evaluation_sheets/: Contains sheets or documents that evaluate the extracted parameters against the ground truth data.

    examples/: contains examples of a single article extraction and a JSON file containing all results from different prompt extractions

    prompts/: contains the different prompts that will be used to prompt the LLM during extraction

    results/: where the JSON file will be saved to after extraction

### Notebooks

    pdf_to_text.ipynb:
        This notebook reads the PDF files from the data/pdf_files folder and extracts the text content, saving the output in the data/text_files folder.

    parameter_extraction.ipynb:
        This notebook extracts parameters from the article text files by building prompts and sending requests to the GPT API. The results are stored in a JSON file.
        The results will need to be checked later manually.

    ground_truth_evaluation.ipynb:
        This notebook evaluates the accuracy of the parameter extraction process by comparing the extracted data with the reference data in data/ground_truth. The results are recorded in data/evaluation_sheets for further analysis and refinement of the extraction process.

### Getting Started

Prerequisites
    Software to run Jupyter notebooks e.g. Jupyter, VSCode, Google Collab
    Python libraries: Pandas, OpenAI

Running the code:
    Each notebook is self-explanatory and guides you through each step. 
    An OPenAI API key is preferred but examples of LLM outputs have been provided if you do not have one.

### License
This project is licensed under the MIT License.