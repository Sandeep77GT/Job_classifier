# Job Recommendation System using Web Scraping and Unsupervised Learning

## Overview
This project implements an end-to-end job recommendation system that combines web scraping, natural language processing, and unsupervised machine learning to categorize job postings based on required skills and recommend relevant jobs to users.

The system scrapes job listings from the Karkidi platform, extracts key information, clusters jobs based on skill similarity, and matches new job postings to user preferences.

---

## Problem Statement
Job seekers often struggle to filter relevant opportunities from large volumes of listings. This project aims to:

- Automatically extract job postings from web sources
- Analyze and group jobs based on required skills
- Recommend relevant jobs based on user interests
- Reduce manual effort in job searching

---

## System Architecture

The system consists of the following components:

1. Web Scraping Module
2. Data Preprocessing
3. Feature Extraction (TF-IDF)
4. Skill-Based Clustering
5. Job Classification
6. Recommendation Engine

---

## Data Collection

Job data is scraped from:

- Source: https://www.karkidi.com

### Extracted Features:
- Job Title
- Company
- Location
- Experience
- Skills
- Job Summary

---

## Methodology

### 1. Web Scraping
- Uses `requests` and `BeautifulSoup`
- Extracts structured job data from HTML
- Supports multi-page scraping

---

### 2. Data Preprocessing
- Handles missing values
- Converts text to lowercase
- Cleans and standardizes skill fields

---

### 3. Feature Extraction
- TF-IDF Vectorization applied to job skills
- Custom tokenizer splits skills using commas
- Converts textual skill data into numerical vectors

---

### 4. Clustering

- Algorithm: Agglomerative Hierarchical Clustering
- Groups jobs into clusters based on skill similarity
- Number of clusters configurable (default = 5)

---

### 5. Classification Model

- Algorithm: Nearest Centroid Classifier
- Purpose: Assign new job postings to existing clusters
- Converts unsupervised clustering into a predictive system

---

### 6. Recommendation Engine

- Matches new job postings with user-selected cluster
- Filters jobs based on cluster similarity
- Displays relevant job opportunities

---

## Workflow

1. Scrape job data from the website
2. Preprocess extracted data
3. Convert skills into TF-IDF features
4. Cluster jobs into groups
5. Train centroid-based classifier
6. Scrape new job postings
7. Assign new jobs to clusters
8. Recommend jobs based on user interest

---

## Project Structure
├── scraper.py
├── clustering_model.py
├── recommendation.py
├── requirements.txt

---

## Installation

### 1. Clone the Repository
git clone https://github.com/your-username/job-recommendation-system.git

cd job-recommendation-system

### 2. Install Dependencies
pip install -r requirements.txt

---

## Running the Project
python main.py

---

## Model Details

- Feature Extraction: TF-IDF
- Clustering Algorithm: Agglomerative Clustering
- Classification Algorithm: Nearest Centroid
- Input Data: Job skills text
- Output: Cluster labels and recommended jobs

---

## Results

- Jobs are grouped into meaningful clusters based on skill similarity
- New job postings are accurately assigned to relevant clusters
- System successfully filters jobs based on user preference clusters

---

## Key Insights

- Skill-based clustering provides meaningful grouping of job roles
- TF-IDF effectively represents skill importance
- Hybrid approach (clustering + classification) improves usability
- System can adapt to new job postings dynamically

---

## Limitations

- Web scraping depends on website structure changes
- Limited to skills explicitly mentioned in job descriptions
- Requires manual selection of cluster for recommendations
- Sparse data may affect clustering quality

---

## Future Improvements

- Deploy as a web application using Streamlit
- Integrate user profiles for personalized recommendations
- Use advanced embeddings (Word2Vec, BERT)
- Automate cluster selection using similarity scoring
- Store and update job data in a database
- Add real-time notifications for new jobs

---

## Conclusion

This project demonstrates a practical approach to building a job recommendation system using web scraping and unsupervised learning. It highlights how clustering and classification can be combined to create intelligent, scalable recommendation systems.

---

## Author

Sandeep S L  
MSc Data Analytics (Computational Science)  
Digital University of Kerala  

---

## License

This project is open-source and available under the MIT License.
