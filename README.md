# MarcoPolo AI Model

## Overview

This project implements a job recommendation system that analyzes job descriptions and recommends suitable jobs based on a user's skill set. It uses natural language processing (NLP) techniques to extract skills from job summaries and machine learning methods to match these skills with user-provided skills.

## Files

- `Final copy.ipynb`: Jupyter Notebook with the final analysis and processing steps.
- `Indeed_10k.csv`: Original dataset containing job summaries and other details.
- `jobs_with_skills.csv`: Processed dataset with extracted skills from job summaries.
- `skills.csv`: List of relevant skills used for skill extraction.

## Setup

1. **Clone the Repository**

   ```bash
   git clone <repository-url>
   cd <repository-directory>

```

## Create and Activate a Virtual Environment

```bash
python -m venv venv
source venv/bin/activate  # On Windows use venv\Scripts\activate
```
## Install Dependencies
Ensure you have the following packages listed in requirements .
```
fastapi
uvicorn
pandas
scikit-learn
nltk
```

