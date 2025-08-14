# Employee-Review-Sentiment-Analyzer
1) Overview- This project analyzes thousands of employee reviews from platforms like Glassdoor and Indeed to generate actionable HR insights. Reviews are often unstructured, inconsistent, and written in free-flowing natural language, making them hard to quantify. Using Natural Language Processing (NLP) techniques, this project processes, cleans, and analyzes reviews to classify sentiments, extract recurring themes, and visualize trends for informed decision-making.

2) Problem Statement- Employee reviews contain valuable cultural and operational feedback, but:
They are unstructured and difficult to analyze at scale. Contain slang, spelling errors, and inconsistent grammar. Sentiments are often mixed (e.g., “Great learning but no work-life balance”).
Traditional HR tools cannot effectively process qualitative data. This leads to missed opportunities for improving retention, workplace culture, and employer branding.

3) Objectives- Convert raw, unstructured reviews into structured, analyzable datasets.Automatically classify each review’s sentiment (positive/neutral/negative).
Extract and rank key themes from Pros and Cons.Visualize sentiment trends over time for HR and management decision-making.

4) Data Preprocessing & Cleaning- Text Normalization: Lowercasing, punctuation removal, and whitespace cleanup. Noise Removal: Regex-based removal of special characters and numbers. Stopword Removal: Using NLTK stopword list to eliminate non-informative words.
Lemmatization: Reduced words to their base form for better analysis.
Vectorization: Used TF-IDF to convert text into numerical feature vectors. Identified top 100 keywords for Pros and Cons.

5) Sentiment Analysis- Used VADER (Valence Aware Dictionary and sEntiment Reasoner) from NLTK Works well on short, informal text (social media/review style).
Generates four scores: Positive, Negative, Neutral, and Compound (-1 to +1).
Compound score used for classification:
Positive: ≥ 0.05
Neutral: between -0.05 and 0.05
Negative: ≤ -0.05
Achieved 95% sentiment coverage, eliminating the need for manual labeling.

6) Feature Extraction & Visualization- Boxen Plots: Distribution of sentiment scores across companies.
Time-Series Charts: Year-wise sentiment changes linked to events or policy shifts.
WordClouds: TF-IDF weighted for Pros (e.g., flexible, culture) and Cons (pressure, management).
Keyword Frequency Tables: Quantified common topics and concerns.

7) Business Impact- HR can track employee satisfaction trends in real time.
Management can identify and address recurring workplace issues. Enables data-driven HR decisions for improving culture and retention.
Enhances employer branding through targeted improvements.
