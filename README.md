# MarcoPolo AI Model

![Silk Road Logo](./Artboard%203%20copy%203.svg)

## Overview

This project implements a job recommendation system that analyzes job descriptions and recommends suitable jobs based on a user's skill set. It uses natural language processing (NLP) techniques to extract skills from job summaries and machine learning methods to match these skills with user-provided skills.

![Silk Road Logo](./silkroad.jpg)

## Files

- `Final copy.ipynb`: Jupyter Notebook with the final analysis and processing steps.
- `Indeed_10k.csv`: Original dataset containing job summaries and other details.
- `jobs_with_skills.csv`: Processed dataset with extracted skills from job summaries.
- `skills.csv`: List of relevant skills used for skill extraction.

## Setup

1. **Clone the Repository**

   ```bash
   git clone https://github.com/SilckRoad-MarcoPolo/SilkRoad_AI.git
   cd SilkRoad_AI
   ```

````

## Create and Activate a Virtual Environment

```bash
python -m venv venv
source venv/bin/activate  # On Windows use venv\Scripts\activate
````

## Install Dependencies

Ensure you have the following packages listed in requirements .

```
fastapi
uvicorn
pandas
scikit-learn
nltk
```

## Output Example

```

{
    "user_skills": "python, sql, data analysis",
    "recommendations": [
        {
            "job_title": "Software Engineer, ERP",
            "matching_skills": 2,
            "similarity_score": 0.37,
            "job_skills": [
                "sql",
                "python",
                "c"
            ]
        },
        {
            "job_title": "Software Engineer II - Java",
            "matching_skills": 2,
            "similarity_score": 0.34,
            "job_skills": [
                "shell",
                "algorithms",
                "database",
                "nosql",
                "python",
                "sql",
                "c",
                "Object-oriented programming",
                "Hadoop",
                "perl",
                "c++",
                "rest",
                "ai",
                "java",
                "data architecture"
            ]
        }
    ]
}
```

## Data Processing

### Extract Skills

The script processes job summaries to extract relevant skills and saves the results to `jobs_with_skills.csv`. It uses predefined skill lists and NLP techniques to identify and extract skills from job descriptions.

### Recommendation

The `recommend_jobs` function matches user-provided skills with job skills from the dataset and recommends the top N jobs. It calculates the similarity between user skills and job skills to generate the recommendations. The AI generates three different job recommendations for the user based on the highest matching skills and similarity scores.
