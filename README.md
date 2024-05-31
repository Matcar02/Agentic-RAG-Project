# Agentic-RAG enhanced LLM
#### A tailored LLM to reduce hallucinations and improve factuality.

## Description
### The project, as part of my bachelor's thesis, intends to address some limitations of traditional LLMs, namely, knowledge cut-off and hallucinations. In this case study, I used GROQ, LangChain and Meta Llama3-8B to build the system, which consists of a workflow which verifies, grades and improves question answering generation. It can be applied to any structured dataframe or textual data (corpus); in my final work, it has been used on financial news data. More information is available on the paper ```Thesis_paper```.


## Installation
1. Clone the repository.
2. Create a conda environment using the requirements.yaml file with this command
```
conda env create -f requirements.yaml
```
3. Activate the requirements env:
```
conda activate rag_environment
```


## Project Structure (Tree)
The project has a very simple structure, but it is *incomplete*. Under the data folder, you should insert your docs (text, a csv, or any file format supported by LangChain parser) to process. Once embeddings and indeces are created, they should be stored in the 'Data' subfolder, so that they can be easily retrieved.
------------
```

├───Agentic-RAG-Project   <- Folder root
│   ├───Data  <- knowledge base data used for RAG, along with indeces and embeddings.
│   ├───main.ipynb  <- notebook containing code to execute
│   ├───requirements.yaml  <- packages to install
│   └───README.md

```
## Use
In order to use and test the code, please simply run the different chunks in the notebook either by running  ```main.ipynb``` or another python file you may want to use for orchestration. *Note that file paths in the notebook have to be defined!* If a csv is under the data folder, you may want to load the data using pandas, polars or huggingchat loaders. Below, a simple example (assuming main.ipynb does not change location):
```
df = pl.read_csv('../data/'your_file.csv')

```


## License 
The project is licensed under the MIT License.
