# DataGPT Assessment: Embedding Model for Efficient Dataset Querying

## Overview

The provided repository is an innovative solution designed to enhance data analysis and querying capabilities. Utilizing open-soruced Large Language Model - LLaMa2 finedtuned on SQL queries, the code enables users to perform complex queries on datasets using natural language, seamlessly interpreting both textual and numerical descriptors. This project showcases the development of a model tailored for a shipping dataset sample, demonstrating versatility in handling various data types and understanding ordinal relationships.

As per the requirements, we have adherred to OpenSource tools along with the model that has been fine-tuned on a publicly available dataset. 

The first step was to fine-tune the Code-Llama2 13b model on the SQL query dataset. The model was pruned to fp8 and quantized to INT8 to reduce the model size and make it more efficient for deployment. The training script is provided in the repository for reference. Training took around 4 hours on 2 NVIDIA A100 GPUs. The model was then evaluated during inference on the dataset provided and has shown promising results.

Model link: https://huggingface.co/shashwat1225/Text2sql-Llama2-13b

The following steps are provided to run the model at inference along with the prerequisites and the installation steps.


## Table of Contents

- [Features](#installation)
- [Installation](#installation)
- [Usage](#usage)
- [Scalability](#scalability)

## Features

1. Natural Language Processing: Convert textual queries into SQL queries for efficient data retrieval.
2. Flexible Data Handling: Capable of processing queries involving date, categorical, and numerical columns.
3. Advanced Query Interpretation: Understands ordinal text and searches, including handling synonyms, case insensitivity, and typographical errors.
4. Scalable Solution: Designed to be scalable, capable of handling larger datasets with multiple columns.


## Installation

### Prerequisites

Ensure Python (version 3.7 or later) and pip are installed. This project requires a GPU capable of ~10 tokens/second, similar to NVIDIA T4 or better GPU, for optimal performance.

### Setup

1. Clone the repository:

```bash
git clone 
```

2. Install the required packages:

```bash
pip install -r requirements.txt
```

## Usage

Instructions on how to use the project or examples of usage.

### Running the scripts

1. Data Preparation: Place your dataset in the project directory. Ensure it is formatted correctly as per the example CSV file.
2. Querying the Dataset: Use DataGPT-main.ipynb for interacting with the dataset using natural language queries.
3. Model Training and Fine-tuning (Optional): DataGPT-train.ipynb provides insights into the model's training process for further customization.

### Querying the Dataset

1. Input your query when prompted in DataGPT-main.ipynb. For example:
    
    ```python
    "Find the apparel products with delivery distances greater than 400 along with air transport."
    ```

2. The system will display the generated SQL query and execute it, presenting the results in a DataFrame format.

## Scalability

is designed with scalability in mind, capable of handling larger datasets efficiently. During the technical interview, the solution will be evaluated against a dataset of 100,000 rows and 50 columns, demonstrating its robustness and efficiency in real-world scenarios.
