# Thesis Supervisor Allocation Using Cosine Similarity and Genetic Algorithm

## About
This project develops an optimization approach for assigning first supervisors to undergraduate thesis students. It combines text-based research-topic matching with a genetic algorithm (GA) to balance student preferences, research relevance, and supervisor capacity.

The study compares different text representations and optimization scenarios to examine their effects on allocation quality and computational performance.

## Dataset
The analysis uses two administrative datasets:

- **Student data:** Research interests and up to three preferred supervisors per student.
- **Supervisor data:** Research interests, publication or research titles, supervisor identifiers, and maximum supervision capacity.

## Methods

### 1. Data Preprocessing
- Filtered supervisor preferences according to administrative eligibility.
- Handled missing research interests and incomplete supervisor preferences.
- Combined supervisor research interests and research titles into a single text field.
- Translated Indonesian research descriptions into English for text processing.
- Applied case folding, punctuation and number removal, text cleaning, and stopword removal.

### 2. Text Representation
- **TF-IDF:** Weighted terms based on their relative importance across student and supervisor descriptions.
- **N-gram comparison:** Evaluated unigram, bigram, and combined unigram-bigram representations.
- **Cosine Similarity:** Quantified the similarity between student research interests and supervisor research fields.

### 3. Genetic Algorithm Optimization
The GA assigns one supervisor to each student while minimizing penalties associated with:
- **Supervisor capacity:** Penalizes assignments that exceed the stated capacity.
- **Student preferences:** Gives different penalties to assignments outside the first, second, or third choice.
- **Research-topic relevance:** Penalizes assignments with lower cosine similarity scores.

The implementation compares eight scenarios based on generation count, capacity-penalty formulation, and penalty weights. Each scenario is evaluated using three text representations, resulting in 24 combinations.

### 4. Evaluation
- Supervisor workload and capacity violations
- Number of students assigned to their first, second, or third choice
- Number of assignments outside the listed preferences
- Average cosine similarity between student and supervisor research descriptions
- GA fitness values and computational time

## Academic Project
**Title:** Allocation of the First Supervisor for Students' Final Assignments Using Cosine Similarity and Genetic Algorithm Approaches  
**Project type:** Undergraduate thesis  
**Completion:** July 2026  
**Grade:** A

## Author
**Sandra Berliana Putri** - Statistics and Data Science graduate from IPB University.
