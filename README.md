# MarcoPolo AI Model

![Silk Road Logo](./assets/logo.jpg)

## Overview

This project implements a job recommendation system that analyzes job descriptions and recommends suitable jobs based on a user's skill set. It uses natural language processing (NLP) techniques to extract skills from job summaries and machine learning methods to match these skills with user-provided skills.

![Silk Road Logo](./assets/silkroad.jpg)


### "On every journey, the key is not just where you go, but how you grow along the way."
— Marco Polo

![Silk Road Mood Board](./assets/SilkRoadMoodBoard.png)





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

```json
{
    "user_skills": "javascript, node.js",
    "recommendations": [
        {
            "job_title": "full stack software engineer",
            "matching_skills": 1,
            "similarity_score": 0.71,
            "job_skills": [
                "java",
                "scala",
                "Node.js",
                "c++",
                "javascript"
            ]
        },
        {
            "job_title": "full stack developer",
            "matching_skills": 1,
            "similarity_score": 0.65,
            "job_skills": [
                "React",
                "java",
                "Node.js",
                "Angular",
                "c#",
                "javascript",
                "python"
            ]
        },
        {
            "job_title": "growth engineer",
            "matching_skills": 1,
            "similarity_score": 0.59,
            "job_skills": [
                "scripting",
                "React",
                "ply",
                "Node.js",
                "typescript",
                "ai",
                "javascript"
            ]
        },
        {
            "job_title": "software engineer automation - quality",
            "matching_skills": 1,
            "similarity_score": 0.55,
            "job_skills": [
                "Go",
                "java",
                "Node.js",
                "ruby",
                "php",
                "javascript",
                "python"
            ]
        },
        {
            "job_title": "software development engineer in test intern",
            "matching_skills": 1,
            "similarity_score": 0.51,
            "job_skills": [
                "scripting",
                "React",
                "css",
                "visual",
                "scala",
                "ply",
                "js",
                "Node.js",
                "ai",
                "html",
                "Git",
                "automation",
                "javascript",
                "python"
            ]
        }
    ]
}
```
- **user_skills**: The list of skills provided by the user.
- **recommendations**: A list of the top 3 job recommendations generated by the AI.
  - **job_title**: The title of the recommended job.
  - **matching_skills**: The number of skills from the user that match the job requirements.
  - **similarity_score**: A score representing the similarity between the user's skills and the job's required skills.
  - **job_skills**: A list of skills required for the job.

The AI generates and returns three different job recommendations based on:

1. **Matching Skills**: The number of skills that the user has which match the skills required for the job.
2. **Similarity Score**: A calculated score indicating how similar the user's skills are to the job's required skills, with higher scores indicating better matches.    

## Data Processing

### Extract Skills

The script processes job summaries to extract relevant skills and saves the results to `jobs_with_skills.csv`. It uses predefined skill lists and NLP techniques to identify and extract skills from job descriptions.

### Recommendation

The `recommend_jobs` function matches user-provided skills with job skills from the dataset and recommends the top N jobs. It calculates the similarity between user skills and job skills to generate the recommendations. The AI generates three different job recommendations for the user based on the highest matching skills and similarity scores.
