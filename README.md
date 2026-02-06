# FUTURE_ML_03

# Resume Screening & Candidate Ranking System

## Project Overview
Hiring teams often receive hundreds of resumes for a single job role, making manual screening slow, inconsistent, and error-prone.  
This project implements a **Machine Learning–based resume screening system** that automatically analyzes resumes, compares them with a job description, and ranks candidates based on role fit.

The system is designed as a **decision-support tool** to help recruiters prioritize candidates efficiently, not to replace human judgment.

---

## Objectives
The system aims to:
- Process unstructured resume text data
- Extract relevant skills using NLP techniques
- Compare resumes against a job description
- Score and rank candidates based on relevance
- Identify missing required skills for each candidate

---

## Technologies Used
- **Python**
- **Pandas & NumPy** – data handling
- **BeautifulSoup** – HTML cleaning
- **NLTK / spaCy** – text preprocessing
- **Scikit-learn**
  - TF-IDF Vectorization
  - Cosine Similarity
  - MultiLabelBinarizer
- **Matplotlib** – visualization

---

## Dataset
- Input data is provided as a CSV file containing:
  - `ID`: unique candidate identifier
  - Resume text (HTML or plain text)
- No personal names are used; candidates are tracked using IDs only.

---

## System Workflow
1. **Data Cleaning**
   - HTML tags and noise are removed from resume text
   - Text is normalized for consistent processing

2. **Skill Extraction**
   - A predefined skill vocabulary is matched against resumes
   - Skills are extracted from both explicit skill sections and full resume text

3. **Job Description Processing**
   - The job description is vectorized using TF-IDF
   - Resumes are compared semantically to the job description

4. **Scoring Logic**
   - Resume–job description similarity score
   - Required skill match score
   - Nice-to-have skill match score

5. **Final Ranking**
   - Weighted combination of similarity and skill scores
   - Candidates are ranked from highest to lowest role fit

---

## Scoring Formula
The final score is calculated as:

