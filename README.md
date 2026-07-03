\# FUTURE\_ML\_03

Resume / Candidate Screening System



\# Resume / Candidate Screening System



\## Recommendation Interpretation



\### What the Recommendation Means



This system recommends the most suitable job descriptions for a resume by comparing the semantic meaning of resume content with job descriptions using Sentence Transformers.



Unlike traditional keyword matching, the model understands contextual similarity between resumes and job descriptions. This enables the system to recommend jobs even when different words express similar skills or experience.



Each recommendation is accompanied by a similarity score and a skill gap analysis, helping users understand:



\- Why a particular job is recommended

\- Which skills from the job description are already present in the resume

\- Which important skills are missing and should be learned or added



The recommendation process supports both:



\- Resume → Top Matching Jobs

\- Job Description → Top Matching Candidates



This makes the system useful for job seekers as well as recruiters.



\---



\# Project Overview



This project develops a Resume / Candidate Screening System that uses Sentence Transformers to generate semantic embeddings for resumes and job descriptions.



Cosine Similarity is used to compare embeddings and rank the most relevant matches. The project also performs skill matching by identifying matched and missing skills between resumes and job descriptions.



The system provides explainable recommendations through similarity scores, skill gap analysis, and multiple visualizations.



\---



\## Objectives



\- Build a semantic resume recommendation system



\- Recommend the Top-N matching jobs for a resume



\- Recommend the Top-N matching resumes for a job description



\- Perform skill gap analysis



\- Visualize recommendation results



\- Help job seekers improve resumes



\- Assist recruiters in identifying suitable candidates



\---



\## Tech Stack



\- Python



\- Pandas



\- NumPy



\- Sentence Transformers



\- Scikit-Learn



\- NLTK



\- Matplotlib



\- Seaborn



\- WordCloud



\- Joblib



\---



\## Dataset



The datasets are not included in this repository because they exceed GitHub's file size limits.



Download links are available inside:



```

data/README.md

```



After downloading, place the files in the `data/` folder.



Example:



```

data/

├── Resume.csv

└── JobDescription.csv

```



\---



\## Project Structure



```

Resume-Recommendation-System/



├── data/

│   ├── README.md

│

├── notebooks/

│

├── plots/

│

├── requirements.txt

│

└── README.md

```



\---



\## Methodology



\### Step 1: Data Preprocessing



Both resumes and job descriptions undergo preprocessing:



\- Lowercase conversion



\- Removal of punctuation



\- Removal of stop words



\- Text cleaning



\- Skill extraction



\---



\### Step 2: Sentence Embedding Generation



Each cleaned resume and job description is converted into dense vector embeddings using Sentence Transformers.



These embeddings capture semantic meaning rather than exact keyword matches.



\---



\### Step 3: Similarity Computation



Cosine Similarity is calculated between resume embeddings and job description embeddings.



Higher cosine similarity indicates greater semantic similarity.



\---



\### Step 4: Recommendation Ranking



The system sorts similarity scores in descending order.



The Top-N jobs (or resumes) with the highest similarity scores are returned as recommendations.



\---



\### Step 5: Skill Gap Analysis



For each recommended job:



\- Skills required by the job description are extracted.



\- Skills present in the resume are identified.



\- Missing skills are highlighted.



This helps users understand how to improve their resumes for better job matching.



\---



\# How Resumes Are Scored



Each resume is transformed into a semantic embedding using a pre-trained Sentence Transformer model.



Similarly, every job description is converted into its own embedding.



The similarity between a resume and a job description is computed using Cosine Similarity.



```

Cosine Similarity = (A · B) / (||A|| × ||B||)

```



Similarity values range between \*\*0 and 1\*\*.



Higher similarity indicates that the resume is more closely aligned with the job description.



The jobs are ranked according to these similarity scores.



\---



\# Candidates Ranking



Candidates rank higher because their resumes are semantically closer to the job description.



The ranking considers:



\- Technical skills



\- Programming languages



\- Tools



\- Domain knowledge



\- Work experience descriptions



\- Responsibilities



\- Overall contextual similarity



A candidate with more relevant skills and experience receives a higher similarity score and is ranked above others.



\---



\# Skill Gap Analysis



For every recommended job, the system compares the required skills with the skills identified in the resume.



Three outputs are generated:



\### Matched Skills



Skills present in both the resume and the job description.



Example:



\- Python



\- SQL



\- Machine Learning



\- TensorFlow



\---



\### Missing Skills



Skills required by the job but absent from the resume.



Example:



\- Docker



\- Kubernetes



\- Azure



\- Spark



\---



\### Recommendation Insight



A candidate with many matched skills and few missing skills receives a stronger recommendation.



The missing skills also serve as personalized suggestions for improving the resume and increasing compatibility with similar job roles.



\---



\## Features



\- Resume recommendation



\- Candidate recommendation



\- Semantic similarity search



\- Skill matching



\- Missing skill detection



\- Resume word cloud generation



\- Similarity score visualization



\- Recommendation ranking



\- Explainable AI recommendations



\---



\## Visualizations



The project includes exploratory data analysis (EDA) and recommendation analysis visualizations to better understand the datasets and model outputs.



\### Dataset Analysis



\- Job Title Distribution

\- Most Common Job Titles

\- Work Type Distribution

\- Qualification Distribution

\- Experience Distribution

\- Skills Word Count Distribution

\- Job Description Length Distribution

\- Responsibilities Length Distribution

\- Resume Category Distribution

\- Resume Length Boxplot



\### Text Analysis



\- Top 20 Bigrams



\### Recommendation Analysis



\- Top 5 Recommended Jobs for a Resume

\- Top 5 Resume Matches for a Job Description

\- Resume Skill Match Percentage

\- Skill Coverage Across Top Recommended Jobs (Matched vs Missing Skills)



\### Sample Output Visualizations



The repository contains sample recommendation outputs generated for different resumes, including:



\- Top 5 Recommended Jobs

\- Resume Skill Match Percentage

\- Skill Coverage Across Top Recommended Jobs



These visualizations demonstrate how the recommendation system explains its predictions through similarity scores and skill gap analysis.



\---



\### Resume Analysis



\- Top 20 Frequent Resume Words



\- Resume Statistics



\- Word Frequency Distribution



\---



\## Model Output



For every resume, the system generates:



\- Top matching job descriptions



\- Similarity scores



\- Ranking of recommendations



\- Matched skills



\- Missing skills



For every job description, the system generates:



\- Top matching candidates



\- Candidate similarity scores



\- Ranked candidate list



\---



\## Business Impact



The proposed solution benefits both job seekers and recruiters.



\### For Job Seekers



\- Find jobs matching their profiles



\- Identify missing skills



\- Improve resume quality



\- Increase interview opportunities



\### For Recruiters



\- Automatically rank resumes



\- Reduce manual screening time



\- Identify suitable candidates quickly



\- Improve recruitment efficiency



\---



\## How to Run



\### 1. Install dependencies



```bash

pip install -r requirements.txt

```



\### 2. Download the datasets



Follow the instructions in:



```

data/README.md

```



Place the datasets inside the `data/` folder.



\---



\### 3. Open the notebooks



Run the notebooks sequentially to reproduce the results.



\---



\## Requirements



Install all dependencies using:



```bash

pip install -r requirements.txt

```



\---



\## Future Improvements



\- Resume parsing from PDF



\- Real-time job recommendation web application



\- ATS compatibility scoring



\- Resume quality scoring



\- Personalized resume improvement suggestions



\- Deep skill extraction using Named Entity Recognition



\- Integration with online job portals



\---



\# Conclusion



This project demonstrates how Sentence Transformers and semantic similarity can significantly improve resume recommendation compared to traditional keyword-based approaches.



By combining semantic embeddings, cosine similarity, and skill gap analysis, the system provides accurate, explainable, and personalized recommendations for both job seekers and recruiters.



The generated visualizations further enhance interpretability by showing similarity scores, recommendation rankings, matched skills, and missing skills, making the recommendation process transparent and actionable.



\---



\## Author



\*\*OVIYAA A J\*\*



Future Interns — Machine Learning Track

