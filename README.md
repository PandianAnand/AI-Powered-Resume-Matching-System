# AI-Powered Resume Matching System using Milvus

## Overview

This project is an AI-powered resume matching system that uses semantic search to identify the most relevant candidates for a given job description. Instead of relying on traditional keyword matching, the system converts resumes and job descriptions into vector embeddings and performs similarity search using Milvus, a vector database.

The project demonstrates how modern Natural Language Processing (NLP), sentence embeddings, and vector databases can be applied to solve a real-world recruiting problem.

---

## Features

- Load and preprocess over **2,700 resumes**
- Generate semantic embeddings using **Sentence Transformers**
- Store embeddings in **Milvus**
- Perform fast semantic similarity search
- Rank candidates based on relevance
- Display:
  - Match percentage
  - Resume ID
  - Resume category
  - Resume description
  - Semantically matched skills
- Interactive command-line interface
- User-selectable Top-K search results

---

## Technologies Used

| Component | Technology |
|-----------|------------|
| Programming Language | Python |
| Development Environment | Google Colab |
| Vector Database | Milvus |
| Embedding Model | sentence-transformers/all-MiniLM-L6-v2 |
| Machine Learning | Sentence Transformers |
| Data Processing | Pandas |
| Numerical Computing | NumPy |

---

## Project Workflow

1. Load resume dataset
2. Clean and preprocess resume text
3. Generate sentence embeddings
4. Store embeddings in Milvus
5. Accept a job description
6. Convert the job description into an embedding
7. Perform semantic similarity search
8. Rank candidates by similarity
9. Display the top matching resumes and matched skills

---

## Project Structure

```
AI-Resume-Matching-System/
│
├── Resume_Matching.ipynb
├── README.md
├── requirements.txt
└── screenshots/
    ├── dataset_loaded.png
    ├── cleaned_dataframe.png
    ├── embeddings_shape.png
    ├── milvus_database.png
    ├── hr_search_results.png
    ├── data_scientist_results.png
    └── command_line_interface.png
```

---

## Installation

Clone the repository

```bash
git clone https://github.com/PandianAnand/AI-Powered-Resume-Matching-System.git
```

Install dependencies

```bash
pip install pymilvus sentence-transformers pandas numpy torch
```

---

## Running the Project

Open the notebook in Google Colab and execute the cells in order.

Example search:

```python
job = """
Looking for a Human Resources specialist with experience in recruiting,
employee relations, and HR operations.
"""

display_results(search_resumes(job))
```

Or use the interactive command-line interface to enter any job description and choose the number of results to display.

---

## Example Output

```
Rank: 1

Client ID: 25676643

Match: 78.28%

Category: HR

Matched Skills

✓ HR Recruitment
✓ Human Resources Management
✓ Employee Relations
✓ HR Programs
✓ Strategic Recruitment Planning
✓ Orientation and Onboarding
```

The system returns the most semantically relevant resumes instead of simply matching keywords.

---

## Results

The completed system successfully:

- Processed over **2,700 resumes**
- Generated **384-dimensional semantic embeddings**
- Stored all embeddings in Milvus
- Performed semantic similarity search in real time
- Ranked resumes by relevance
- Extracted semantically related skills
- Supported multiple job descriptions across different industries
- Allowed users to specify the number of returned matches

---

## Future Improvements

Potential enhancements include:

- Hybrid search combining semantic and keyword matching
- Resume summarization using Large Language Models (LLMs)
- Streamlit or Flask web interface
- Experience and education weighting
- Candidate filtering by location, experience, or education
- Cross-encoder reranking for improved ranking accuracy
- REST API deployment
- Docker containerization
- Cloud deployment on AWS, Azure, or Google Cloud

---

## Screenshots

The repository includes screenshots demonstrating:

- Resume dataset loading
- Cleaned dataframe
- Embedding generation
- Milvus database
- Resume search results
- Command-line interface

---

## Author

**Pandian Anand**

AI Resume Matching System

Built using Python, Sentence Transformers, and Milvus.
